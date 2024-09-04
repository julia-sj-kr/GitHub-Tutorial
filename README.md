# GitHub-Tutorial
기초적인 깃허브 사용법

디렉토리 단위로 깃에 올리는 프로세스
최초 한번만 해당하고 추가로 업데이트할때는 해당하지 않음.

* 디렉토리로 이동(본인 로컬 디렉토리 경로)
>  cd C:\Users\405\Desktop\SpeechRecognizer

* Git 초기화(깃 생성)
> git init

* 원격 저장소 추가(본인 깃허브 주소)
> git remote add origin https://github.com/julia-sj-kr/VoiceRecognitionApp.git

* 파일 추가
> git add .

* 커밋
> git commit -m "Initial commit"

* 푸시<br>
  ###### git push -u origin master 에서 -u 옵션은 upstream 설정을 의미하며, 다음부터 git push만 사용해도 되도록 하는 설정입니다.<br>
> git push -u origin master

