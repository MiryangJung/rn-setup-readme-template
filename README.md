# rn-setup-readme-template

---

# 01. Environment‐Setup

## 공통
- Node.js 설치
  - `brew install node`
- watchman 설치
  - `brew install watchman`

## Android
- OpenJDK 설치
  - `brew tap homebrew/cask-versions && brew install --cask zulu17`
- JAVA_HOME 환경변수 설정

```
echo 'export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-17.jdk/Contents/Home' >> ~/.zshrc
source ~/.zshrc
```

## iOS
- CocoaPods 설치
  - `sudo gem install cocoapods`
 
---

# 02. Simulator Setup

## Android

[안드로이드 스튜디오](https://developer.android.com/studio) 설치

- SDK 설치
  - More Actions → SDK Manager
  - **Android 14 (UpsideDownCake)** 설치
    - _Show Package Details를 클릭해 세부 정보를 표시해 모두 설치_
  - SDK Tools 탭
    - Android SDK Build-Tools에서 **v34.0.0** 설치
- emulator 생성
  - More Actions → Virtual Device Manager
  - Create Device를 눌러 새 애뮬레이터를 생성
  - System Image : Tiramisu 33
  - Device: 원하는 디바이스 선택
    - Device 스토리지 용량을 2048mb 이상으로 설정
- ANDROID_HOME 환경 변수 설정

```
vi ~/.zshrc
```

```
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

```
source ~/.zshrc
```

## iOS

[Xcode](https://developer.apple.com/xcode) 설치

- 설치 후 Xcode의 경로를 지정하도록 커맨드 입력
  - `xcode-select --switch /Applications/Xcode.app`
- Xcode → Preferences → Locations → **Command Line Tools**가 선택되어 있는지 확인
