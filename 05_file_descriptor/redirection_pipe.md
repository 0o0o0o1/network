# 파이프와 리다이렉션

## 1. 파이프 (Pipe)

파이프(`|`)는 이전 명령어의 출력을 다음 명령어의 입력으로 전달하는 기능이다.  
명령어가 아니라 셸에서 제공하는 기능이다.

---

### 기본 형태

```bash
명령어1 | 명령어2
```

- 명령어1의 출력 → 명령어2의 입력으로 전달

---

## 2. 파이프 실습

### 1. 파일 목록에서 특정 파일 찾기

```bash
$ ls | grep ".md"
```

- `ls`: 현재 디렉터리 파일 목록 출력  
- `grep ".md"`: `.md`가 포함된 파일만 필터링  
- 결과: `.md` 파일만 출력

---

### 2. 실행 중인 프로세스 검색

```bash
$ ps -ef | grep bash
```

- `ps -ef`: 현재 실행 중인 모든 프로세스 출력  
- `grep bash`: bash가 포함된 프로세스만 출력  
- 결과: bash 관련 프로세스 확인 가능

---

### 3. 파일 개수 확인

```bash
$ ls | wc -l
```

- `ls`: 파일 목록 출력  
- `wc -l`: 줄 개수 계산  
- 결과: 파일 개수 출력

---

### 4. 파이프 여러 개 연결

```bash
$ ps -ef | grep bash | wc -l
```

- `ps -ef`: 프로세스 목록 출력  
- `grep bash`: bash 프로세스만 필터링  
- `wc -l`: 개수 계산  
- 결과: bash 프로세스 개수 출력

---

## 리다이렉션 (Redirection)

리다이렉션(Redirection)은 입력과 출력의 방향을 재지정하는 기능이다.  
파이프와 마찬가지로 명령어가 아니라 셸에서 제공하는 기능이며,  
`<`, `>`, `<<`, `>>` 기호를 사용한다.

- `<`, `<<` : 입력 방향 재지정  
- `>`, `>>` : 출력 방향 재지정  

---

### 기본 동작

#### 출력 리다이렉션 (덮어쓰기)

```bash
$ echo "hello redirection" > redirection.txt
```

```bash
$ cat redirection.txt
hello redirection
```

- `>` : 기존 내용을 덮어쓰고 새로 작성

---

#### 출력 리다이렉션 (이어쓰기)

```bash
$ echo "hello redirection2" >> redirection.txt
```

```bash
$ cat redirection.txt
hello redirection
hello redirection2
```

- `>>` : 기존 내용 뒤에 추가

---

#### 입력 리다이렉션

```bash
$ cat < redirection.txt
```

```bash
hello redirection
hello redirection2
```

- `<` : 파일 내용을 명령어의 입력으로 전달

---

## 특수한 리다이렉션

### 표준 에러 리다이렉션

```bash
[A] 2> [B]
```

- A의 표준 에러(stderr, fd 2)를 B로 출력

---

### 표준 에러를 표준 출력으로

```bash
[A] 2>&1
```

- 표준 에러를 표준 출력(stdout, fd 1)으로 합침

---

### Here Document

```bash
[A] > [B] << [C]
```

- 문자열 C가 입력될 때까지 내용을 입력으로 전달  
- C는 결과에 포함되지 않음
