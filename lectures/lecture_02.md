# Node.js 버전관리

### Node.js 버전관리가 필요한 이유

모든 프로젝트가 버전이 최신은 아니다. 프로젝트마다 버전을 변경할 수 있어야 한다.

다운로드 방식으로 버전을 맞추려면, node.js 홈페이지 들어가서 다운로드 탭에서 버전을 선택해 다운로드 한다.


### Node Version Manager

https://github.com/nvm-sh/nvm

설치 절차
VSCode의 내장 터미널을 bash로 실행하고 아래 명령어를 입력합니다.
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
설치가 완료되면 터미널에서 아래 명령어로 nvm 명령어를 시스템 레벨에 추가합니다.
    vi ~/.bashrc
    # vi로 연 .bashrc 파일에 "i" 키를 입력하여 쓰기 모드로 진입합니다.
    # 그리고 나서 아래 내용을 추가하고 ":"를 입력한 다음 "wq"를 입력하여 저장 후 종료합니다.
    export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

이제 터미널에 nvm 명령어를 입력하면 인식이 되는지 확인합니다.
인식되면 아래의 명령어로 Node.js를 설치합니다.
    nvm install 10.16
설치가 끝나면 아래의 명령어로 Node.js 버전을 변경합니다.
    nvm use 10.16
설치한 이후 아래 명령어로 Node.js 버전이 잘 설정되었는지 확인합니다.
    node -v



