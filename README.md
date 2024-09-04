## GitHub-Tutorial

초보자가 Git과 GitHub를 사용하여 디렉토리를 원격 저장소에 업로드하는 과정을 이해하기 쉽게 설명하였다.<br>
명령 프롬프트의 코드를 정리하였으며 브랜치 병합과 같은 협동 기능은 생략하고 1인 개발자가 버전관리 용도로 쓰는것에 초점을 맞추었다.

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

* 파일 추가<br>
``` git add .```

  git add . 명령어는 현재 디렉토리의 모든 변경된 파일을 추가합니다.

* 커밋<br>
``` git commit -m "Initial commit"```

* 푸시<br>
``` git push -u origin master``` 

   git push -u origin master 에서 -u 옵션은 upstream 설정을 의미하며, 다음부터 git push만 사용해도 되도록 하는 설정입니다.<br>
   `master`는 사용하고 있는 브랜치 이름입니다.

