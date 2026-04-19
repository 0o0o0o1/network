# 환경 변수 확인 및 변경

## 1. 환경 변수 확인 (env)

env는 **environment**의 약자로 현재 환경 변수를 출력하거나,  
새로운 환경 변수를 설정하여 프로그램을 실행할 때 사용한다.

```bash
env [옵션] [NAME=VALUE] [명령어]
```

### 주요 옵션

| 옵션 | 설명 |
|------|------|
| -i | 기존 환경 변수를 무시하고 새로 설정 |
| -u | 지정한 환경 변수 제거 |

---

### 전체 환경 변수 확인

```bash
$ env
```

- 현재 설정된 모든 환경 변수 출력

---

## 2. 환경 변수와 PATH

환경 변수 중 **PATH**는 실행 파일을 찾는 경로를 저장한다.

```bash
$ env -i PATH=/ sh
```

```bash
env: 'sh': No such file or directory
```

- PATH에 실행 파일 경로가 없으면 명령어를 찾지 못함

---

```bash
$ env -i PATH=/bin sh
```

```bash
sh-5.2$
```

- PATH에 `/bin`이 포함되어 있어 정상 실행됨

---

## 3. 환경 변수 설정 (export)

export는 현재 셸에서 새로운 환경 변수를 생성할 때 사용한다.

```bash
export [KEY=VALUE]
```

---

### 예시

```bash
$ export HELLO="hello environ!"
```

```bash
$ env | grep HELLO
HELLO=hello environ!
```

---

### 값 확인

```bash
$ echo $HELLO
hello environ!
```

- `$변수명` 형태로 값 접근 가능

---

## 4. 환경 변수 삭제 (unset)

unset은 현재 셸의 환경 변수를 삭제할 때 사용한다.

```bash
unset [KEY]
```

---

### 예시

```bash
$ unset HELLO
```

```bash
$ echo $HELLO
```

```bash
$ env | grep HELLO
```

- 환경 변수가 삭제된 것을 확인할 수 있음

---

## 5. 핵심 정리

- env: 환경 변수 확인 및 설정
- export: 환경 변수 생성
- echo: 변수 값 확인
- unset: 환경 변수 삭제
- PATH: 실행 파일 탐색 경로
