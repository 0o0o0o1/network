# 디렉터리 명령어

## 1. 현재 경로 확인 (pwd)

```bash
pwd
```

- `pwd` (print working directory)
- 현재 작업 중인 디렉터리의 절대 경로를 출력

### 실행 예시

```bash
$ pwd
/c/Users/CKIRUser/linux/02_file_directory
```

---

## 2. 디렉터리 이동 (cd)

```bash
cd [경로]
```

- `cd` (change directory)
- 디렉터리 경로를 변경할 때 사용

### 상대 경로 이동

```bash
$ pwd
/c/Users/CKIRUser/linux/02_file_directory

$ cd ../

$ pwd
/c/Users/CKIRUser/linux
```

- `../` : 상위 디렉터리로 이동

---

### 절대 경로 이동

```bash
$ cd ~

$ pwd
/c/Users/CKIRUser

$ cd /c/Users/CKIRUser/linux

$ pwd
/c/Users/CKIRUser/linux
```

- `~` : 홈 디렉터리
- `cd`만 입력해도 홈 디렉터리로 이동

---

## 3. 디렉터리 목록 확인 (ls)

```bash
ls [옵션] [경로]
```

- `ls` (list)
- 파일 및 디렉터리 목록 출력
- 경로를 생략하면 현재 디렉터리를 기준으로 동작

### 실행 예시

```bash
$ ls -al
drwxr-xr-x 1 CKIRUser 197121 0 Apr 12 16:19 .
drwxr-xr-x 1 CKIRUser 197121 0 Apr 12 16:19 ..
drwxr-xr-x 1 CKIRUser 197121 0 Apr 12 16:19 .git
drwxr-xr-x 1 CKIRUser 197121 0 Apr 12 16:06 01_shell
drwxr-xr-x 1 CKIRUser 197121 0 Apr 12 16:14 02_file_directory
```

### 출력 형식

```text
파일종류/권한/하드링크수/소유자/그룹/크기/수정일/이름
```

---

## 4. 디렉터리 생성 (mkdir)

```bash
mkdir [디렉터리명]
```

- `mkdir` (make directory)
- 새로운 디렉터리를 생성

### 실행 예시

```bash
$ ls -al
drwxr-xr-x 1 user user 0 Apr 12 01_shell
drwxr-xr-x 1 user user 0 Apr 12 02_file_directory

$ mkdir dir1

$ ls -al
drwxr-xr-x 1 user user 0 Apr 12 01_shell
drwxr-xr-x 1 user user 0 Apr 12 02_file_directory
drwxr-xr-x 1 user user 0 Apr 12 dir1
```

---

## 5. 디렉터리 삭제 (rmdir)

```bash
rmdir [디렉터리명]
```

- `rmdir` (remove directory)
- **비어있는 디렉터리만 삭제 가능**

### 실행 예시

```bash
$ ls -al
drwxr-xr-x 1 user user 0 Apr 12 dir1

$ rmdir dir1

$ ls -al
# dir1 삭제됨
```

---

## 6. 핵심 정리
- pwd: 현재 디렉터리 경로 확인
- cd: 디렉터리 이동 (상대/절대 경로)
- ls: 디렉터리 목록 확인
- mkdir: 디렉터리 생성
- rmdir: 빈 디렉터리 삭제
