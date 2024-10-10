# Git

---

### Git vs. GitHub

<table style='text-align: center'>
    <tr>
        <th style='text-align: center'>Git</th>
        <th style='text-align: center'>GitHub</th>
    </tr>
    <tr>
        <td colspan="2">버전 관리 시스템</td>
    </tr>
    <tr>
        <td>로컬 및 원격 저장소 관리</td>
        <td>웹 기반 원격 저장소 서비스</td>
    </tr>
    <tr>
        <td>원격 저장소와 동기화 가능</td>
        <td>협업 및 코드 공유 기능 제공</td>
    </tr>
</table>

---

### **로컬 → GitHub**

```bash
git push -u origin main
```

위 명령어를 통해 현재 로컬 브랜치의 기본 원격 브랜치로 `origin/main`이 설정됨과 동시에,  
원격 저장소로 파일들을 동기화한다.  
해당 명령어를 입력한 후에는 `git push`만 입력해도 자동으로 `origin/main`으로 파일들이 동기화 된다.

---

### **GitHub → 로컬**

```bash
git pull origin main
```

로컬 브랜치의 기본 원격 브랜치가 설정되어 있다면,  
`git pull`만 입력해도 원격 브랜치로부터 파일을 동기화할 수 있다.

---

### **로컬 브랜치와 원격 브랜치에서 각각 commit을 한 경우**

1. `git pull --rebase`을 이용해 원격 브랜치의 변경 사항을 먼저 로컬 브랜치로 동기화한다.  
   `--rebase` 옵션을 사용하면 로컬 커밋을 최신 원격 변경 사항 위로 재배치한다.
2. 이후, `git push`를 통해 로컬 브랜치의 변경 사항을 원격 브랜치에 반영한다.

---

### **Git flow**

1. 프로젝트 리포지토리를 내 계정으로 Fork하기
2. Fork한 리포지토리를 로컬로 Clone
3. 로컬 브랜치의 기본 원격 브랜치 설정 (Fork한 리포지토리 내 추가 브랜치)
4. 로컬에서 새로운 브랜치 생성
5. 작업 내용을 로컬에서 Commit한 후 원격 브랜치로 Push
6. 원본 프로젝트 리포지토리의 변경 사항을 Fetch
7. 변경 사항에 따라 충돌이 발생한 경우, 충돌 해결
8. 충돌 해결 후 다시 원격 브랜치로 Commit & Push
9. 원본 프로젝트 리포지토리로 Pull Request 생성

---

### **Semantic Versioning**

버전은 세 개의 숫자로 표현되며, 각 숫자는 `.`으로 구분됩니다.  
각각의 숫자는 다음과 같은 의미를 가집니다:

- **Major**: 주 버전. 호환되지 않는 변경 사항이 있을 때 증가합니다.
- **Minor**: 부 버전. 호환되는 새로운 기능이 추가될 때 증가합니다.
- **Patch/Fix**: 패치 버전. 호환되는 버그 수정이 있을 때 증가합니다.

---

### **git tag**

커밋이 많아지게 되면 `git log`를 통해 원하는 커밋 내역을 찾기가 어려울 수 있다.  
이 때, 특정 커밋을 북마크 하듯이 tag를 사용할 수 있다.

|  태그 종류  |               태그 용도               |
| :---------: | :-----------------------------------: |
| lightweight |           특정 커밋을 기록            |
|  annotated  | 작성자 정보 및 날짜, 메시지 등을 기록 |

주로 release된 버전을 기록하여 저장하며 이러한 태그를 lightweight 태그로 구분한다.

- HEAD가 가리키는 커밋에 태그 달기(lightweight)

```bash
git tag v1.0.0
```

- HEAD가 가리키는 커밋에 태그 달기(annotated)

```bash
git tag -a v1.0.0
```

입력 시, 텍스트 편집기가 오픈되며 편집기를 통해 상세 내용을 작성할 수 있다.  
또는 아래 세 가지 명령어 중 하나를 쓰면 간편하게 상세 내용을 작성할 수 있다.

```bash
# 1.
git tag -a v1.0.0 -m "태그 상세 내용"
# 2.
git tag v1.0.0 -am "태그 상세 내용"
# 3.
git tag v1.0.0 -m "태그 상세 내용"
```

- 태그 확인

```bash
git tag
```

- 태그 상세 내용 확인

```bash
git show v1.0.0
```

- 특정 커밋에 태그 달기

```bash
git tag v1.0.1 (해시코드)
```

- 원하는 태그 패턴으로 필터링하여 검색하기

```bash
git tag -l "v1.*"
```

- 태그 삭제

```bash
git tag -d v1.0.0
```

---