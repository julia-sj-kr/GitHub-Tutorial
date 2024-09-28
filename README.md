## GitHub-Tutorial

초보자가 Git과 GitHub를 사용하여 디렉토리를 원격 저장소에 업로드하는 과정을 이해하기 쉽게 설명하였다.<br>
명령 프롬프트의 코드를 정리하였으며 브랜치 병합과 같은 협동 기능은 생략하고 1인 개발자가 버전관리 용도로 쓰는것에 초점을 맞추었다.

---
### :small_orange_diamond: 최초에 디렉토리 단위로 깃에 올리는 프로세스<br>
추가로 업데이트할때는 해당하지 않음.

* GitHub에서 새 저장소를 생성하세요.
  1. GitHub에 로그인 후 오른쪽 상단의 "+" 버튼을 클릭하고 "New repository"를 선택하세요.
  2. 저장소 이름을 입력하고 "Create repository" 버튼을 클릭하세요.

* 디렉토리로 이동(본인 로컬 디렉토리 경로)<br>
``` cd C:\Users\405\Desktop\SpeechRecognizer``` 

* Git 초기화(깃 생성)<br>
``` git init``` 

* 원격 저장소 추가(본인 깃허브 주소)<br>
``` git remote add origin https://github.com/julia-sj-kr/VoiceRecognitionApp.git```

* 스테이지에 파일 올리기<br>
  `git add .` 명령어는 현재 디렉토리의 모든 변경된 파일을 추가합니다.<br>
  `git add MyFolder/` 명령어는 폴더를 지정하여 추가합니다. `MyFolder`는 폴더 이름이다.<br>
  `git add <파일명>` 명령어는 파일을 지정하여 추가합니다.


* 커밋하기<br>
  변경 사항을 커밋합니다. 커밋 메시지는 변경 내용에 대한 설명으로 설정할 수 있습니다.<br>
``` git commit -m "Initial commit"```

* 원격 저장소에 푸시<br>
  로컬 변경 사항을 원격 GitHub 저장소에 푸시합니다.<br>
``` git push -u origin master``` 

   git push -u origin master 에서 -u 옵션은 upstream 설정을 의미하며, 다음부터 git push만 사용해도 되도록 하는 설정입니다.<br>
   `master`는 사용하고 있는 브랜치 이름입니다.
---
### :small_orange_diamond: 기존 깃허브 repository에 로컬에 있는 새로운 자료를 추가하는 프로세스<br>

* 저장소 클론<br>
  저장소를 로컬로 클론합니다. 터미널을 열고 다음 명령어를 입력하세요.<br>
``` git clone https://github.com/julia-sj-kr/Network-communication.git```

* 로컬 저장소로 이동<br>
``` cd Network-communication```

* 드래그 앤 드롭으로 새로운 자료 추가<br>
  이제 로컬 디렉토리에 추가할 파일 또는 폴더를 넣습니다. 원하는 디렉토리에 복사하거나 이동하세요.

* 스테이지에 파일 올리기<br>
  `git add .` 명령어는 현재 디렉토리의 모든 변경된 파일을 추가합니다.<br>
  `git add MyFolder/` 명령어는 폴더를 지정하여 추가합니다. `MyFolder`는 폴더 이름이다.<br>
  `git add <파일명>` 명령어는 파일을 지정하여 추가합니다.

* 커밋하기<br>
  변경 사항을 커밋합니다. 커밋 메시지는 변경 내용에 대한 설명으로 설정할 수 있습니다.<br>
``` git commit -m "Add new file"```

* 원격 저장소에 푸시<br>
  로컬 변경 사항을 원격 GitHub 저장소에 푸시합니다.<br>
``` git push origin master``` 
---
### :small_orange_diamond: 변경 사항을 원격 저장소(깃허브 repository)에 푸시하는 프로세스<br>

* 변경 사항 확인하기<br>
  `git status` 현재 변경된 파일을 확인합니다.<br>
  `git status -s` 간략한 형식으로 상태를 보여줍니다.<br>
    - 출력 해석하기<br>
      - 수정된 파일: `M`이 앞에 붙은 파일들은 현재 작업 디렉토리에서 수정된 파일입니다.
      - 삭제된 파일: `D`가 앞에 붙은 파일들은 삭제된 파일입니다.
      - 추적되지 않는 파일: `??`가 앞에 붙은 파일들은 Git에 의해 추적되지 않는 새 파일들입니다. 파일이 새로 추가되었으나 Git에 의해 추적되지 않고 있다는 것을 의미합니다.

* 변경 사항 스테이징 하기<br>
  `git add .` 명령어는 현재 디렉토리의 모든 변경된 파일을 추가합니다.<br>

* 커밋하기<br>
  변경 사항을 커밋합니다. 커밋 메시지는 변경 내용에 대한 설명으로 설정할 수 있습니다.<br>
  ``` git commit -m "Fix: update MainActivity to improve UI"```

* 원격 저장소에 푸시<br>
  로컬 변경 사항을 원격 GitHub 저장소에 푸시합니다.<br>
``` git push origin master``` 
---
### :small_orange_diamond: 원격 저장소에 로컬에 없는 변경 사항이 있을때 처리하는 프로세스<br>

원격 저장소의 변경 사항을 먼저 가져와서 로컬과 동기화한 후, 다시 푸시하면 됩니다.
소개하는 방법은 2가지이니 상황에 맞게 사용하세요.

- **방법1. 재배치하기(rebase)**
  - 변경 사항 스테이징 하기<br>
  `git add .` 명령어는 현재 디렉토리의 모든 변경된 파일을 추가합니다.<br>
  
  * 커밋하기<br>
  변경 사항을 커밋합니다. 커밋 메시지는 변경 내용에 대한 설명으로 설정할 수 있습니다.<br>
  ``` git commit -m "Fix: update MainActivity to improve UI"```

  -  원격 저장소의 변경 사항 가져오기<br>
  변경 사항을 병합하는 대신, 내 로컬 변경 사항을 원격 변경 사항 위에 "재배치"하여 충돌을 최소화합니다.<br>
  ```git pull origin master --rebase```

  -  푸시하기<br>
  ``` git push origin master``` 

- **방법2. 병합하기**
  -  원격 변경 사항 가져오기<br>
  먼저, 원격 저장소의 변경 사항을 로컬로 가져옵니다.<br>
  `git pull origin master`<br>

  -  충돌 해결<br>
  > 예시 오류메시지:<br>
  https://chatgpt.com/share/01dbcc33-c5f1-4612-90af-daf88bbc4179<br>
  
  만약 `git pull` 중에 충돌이 발생한다면, 충돌을 해결해야 합니다. 충돌이 발생한 파일은 Git에서 표시됩니다.<br>
  해당 파일을 열고 충돌된 부분을 수정한 후, 변경 사항을 추가하고 커밋합니다.<br>
  `git add <수정한 파일>`<br>
  `git commit -m "Resolve merge conflicts"`
  
  -  다시 푸시하기<br>
  모든 충돌이 해결된 후, 다시 푸시 명령어를 실행합니다.<br>
  ``` git push origin master``` 

---
### :small_orange_diamond: 로컬 변경 사항을 무시하고 원격 저장소의 내용을 그대로 가져오는 프로세스<br>
아래 명령어를 사용하여 로컬 변경 사항을 강제로 덮어쓰면 됩니다.  

```
git fetch origin
git reset --hard origin/master
```
---
📝 이모지 모음: https://chatgpt.com/share/aa7321b5-d11d-420d-b471-55dcf5096941

