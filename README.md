# FoodDeliveryApp
인프런(Inflearn) 배달앱 클론코딩 [with React Native](https://www.inflearn.com/course/%EB%B0%B0%EB%8B%AC%EC%95%B1-%EB%A6%AC%EC%95%A1%ED%8A%B8-%EB%84%A4%EC%9D%B4%ED%8B%B0%EB%B8%8C)
Repository [FoodDeliveryApp](https://github.com/rahee-do/food-delivery-app)
Notion [Roadmap](https://www.notion.so/cfaf7ee4a8a34341a3f9206094a49c65?v=b1c7436c439742f6bff9302452e6f35c)

# React Native 환경 설정
brew 설치 확인
설치 안되어 있을 경우, [여기](https://brew.sh/index_ko)에서 설치하기
```shell
$ which brew
> /opt/homebrew/bin/brew
```
brew 로 node 와 watchman 설치하기
```shell
$ brew install node
$ brew install watchman
```
안드로이드 개발에 필요한 JAVA V11 설치하기
```shell
$ brew install --cask adoptopenjdk/openjdk/adoptopenjdk11
```
앱 스토어에서 xcode 도 설치해주기 (IOS 개발에 필요, 용량이 커서 최소 15GigaByte 이상 필요)  
android studio [여기](https://developer.android.com/studio?gclid=Cj0KCQjwnvOaBhDTARIsAJf8eVNyE6yjxH668iexDdBaQboI0MNPzKDfhtMFAvsvv3Z1xwsIY76tviQaAt5lEALw_wcB&gclsrc=aw.ds)에서 설치하기
- Android SDK (V30 설치, 라이브러리 중에 V30에 의존성 있음)
- Android SDK Platform
- Android Virtual Device

android 관련 환경 변수 설정
```shell
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```
환경 변수 설정 완료 확인 명령어
```shell
$ which adb
> /Users/사용자ID/Library/Android/sdk/platform-tools/adb
```
환경 변수 전체 확인 커멘드
`cat` 명령은 지정된 파일의 내용을 보여준다.
`cat /etc/shells` 명령은 etc 디렉토리에 있는 shells 파일의 내용을 보여달라는 의미이다.
```shell
$ cat ~/.zshrc
> HOMEBREW_HOME= /opt/homebrew
> MYSQL_HOME= /usr/local/mysql
> export PATH=${PATH}:${HOMEBREW_HOME}/bin:${MYSQL_HOME}/bin

> export ANDROID_SDK_ROOT=/Users/사용자ID/Library/Android/sdk
> export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
> export PATH=$PATH:$ANDROID_SDK_ROOT/tools
> export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin
> export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools

> export NVM_DIR="$HOME/.nvm"
>  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && . "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
>  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && . "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```
CocoaPods 설치하기
`sudo` 명령어로 실행 시 비밀번호 입력이 필요하다.
```shell
sudo gem install cocoapods
```

# React Native 프로젝트 생성
Creating a new application !
```shell
npx react-native init AwesomeProject
```

## React Native 전역 설치
```shell
npm i -g react-native 
```
```shell
npx react-native init FoodDeliveryApp --template react-native-template-typescript
```

## 배달 주문 API 연동 이후 실행 명령어
shell 에 food-delivery-app-master 폴더 내 back 로 진입한 뒤, `npm start` 로 연결 후,
해당 프로젝트 경로에서 `npm run android` 를 실행시켜줘야 데이터가 들어온다.
