# 파일 명령어

## 1. 파일 생성 (touch)

```bash
touch [파일명]
```

- 새로운 빈 파일 생성 (기본 크기 0)

### 실행 예시

```bash
$ ls -al
total 0

$ touch file1

$ ls -al
-rw-r--r-- 1 user user 0 file1
```

---

## 2. 파일 읽기 및 쓰기 (cat)

```bash
cat [파일명]
```

- 파일 내용을 출력

### 파일 내용 작성

```bash
$ cat > file1 << EOF
Hello Linux!
EOF
```

### 실행 결과

```bash
$ cat file1
Hello Linux!
```

---

## 3. 파일 일부 읽기 (head, tail)

```bash
head -c [바이트] [파일명]
tail -c [바이트] [파일명]
```

- head: 파일 앞부분 출력
- tail: 파일 뒷부분 출력

### 실행 예시

```bash
$ head -c 5 file1
Hello

$ tail -c 5 file1
nux!
```

---

## 4. 파일 이동 (mv)

```bash
mv [원본] [대상]
```

- 파일 이동 또는 이름 변경

### 실행 예시

```bash
$ mv file1 dir1/file1
```

---

## 5. 파일 복사 (cp)

```bash
cp [원본] [대상]
```

- 파일 복사

### 실행 예시

```bash
$ cp file1 dir1/file1
```

---

## 6. 파일 삭제 (rm)

```bash
rm [파일명]
```

- 파일 삭제

### 실행 예시

```bash
$ rm file1
```

---

### 디렉터리 삭제

```bash
rm -rf [디렉터리]
```

- 디렉터리까지 삭제 가능 (주의)

```bash
$ rm -rf dir1
```

---

## 7. 핵심 정리
- touch: 파일 생성
- cat: 파일 읽기/쓰기
- head/tail: 파일 일부 확인
- mv: 이동 및 이름 변경
- cp: 파일 복사
- rm: 파일 삭제
