# 파일 시스템 정리

## 1. 파일과 디렉토리 개념
- **파일(File)**: 데이터를 저장하는 기본 단위  
- **디렉토리(Directory)**: 파일이나 다른 디렉토리를 담는 폴더 역할

# 파일 시스템 정리

## 1. 파일과 디렉토리 개념
- **파일(File)**: 데이터를 저장하는 기본 단위  
- **디렉토리(Directory)**: 파일이나 다른 디렉토리를 담는 폴더 역할

## 2. 파일 시스템의 역할
- 저장장치(하드디스크, SSD)에서 데이터를 효율적으로 관리하고 접근할 수 있도록 도와줌  
- 파일과 디렉토리 구조를 계층적으로 관리(트리 구조)

## 3. 경로(Path)의 종류
- **절대경로(Absolute Path)**: 루트 디렉토리(`/` 또는 드라이브 문자)부터 시작하는 경로  
  예) `/home/user/docs/file.txt`  
- **상대경로(Relative Path)**: 현재 위치를 기준으로 하는 경로  
  예) `docs/file.txt`

## 4. 주요 디렉토리 (Linux 기준)
- `/` : 루트 디렉토리, 모든 파일의 최상위 위치  
- `/home` : 사용자 개인 파일 저장 공간  
- `/etc` : 시스템 설정 파일  
- `/var` : 가변 데이터 파일 (로그, 캐시 등)  
- `/usr` : 응용 프로그램과 라이브러리  

## 5. 파일 권한과 소유권
- Linux 파일은 소유자(user), 그룹(group), 기타(others)에 대해 읽기(r), 쓰기(w), 실행(x) 권한을 가짐  
- `ls -l` 명령어로 권한 확인 가능  

## 6. 파일 시스템 기본 명령어
- `ls` : 현재 디렉토리 목록 보기  
- `cd` : 디렉토리 이동  
- `pwd` : 현재 위치 경로 출력  
- `mkdir` : 새 디렉토리 만들기  
- `rm` : 파일 삭제  
- `touch` : 새 파일 생성  

## 7. 실습: 파일 및 디렉토리 기본 명령어

### 목표  
- 파일과 디렉토리 생성, 이동, 삭제를 연습한다.

### 실습 과정

```bash
mkdir test-dir          # 디렉토리 생성
cd test-dir             # 디렉토리 이동
touch example.txt       # 빈 파일 생성
ls                      # 파일 목록 확인 (example.txt 보여야 함)
rm example.txt          # 파일 삭제
cd ..                   # 상위 디렉토리 이동
rmdir test-dir          # 빈 디렉토리 삭제

---

> **참고 자료**  
> - Linux Filesystem Hierarchy Standard (FHS)  
> - [Linux Command Tutorial](https://linuxcommand.org/)