# 🎲블럭 퍼즐 - 2D 퍼즐 아케이드 게임[모바일]

<p align="center">
<img src="https://user-images.githubusercontent.com/105046055/220895809-6427c269-3998-4ec5-8050-114824fae69b.png" width="50%" height="50%">
</p>

<a href = "https://www.youtube.com/watch?v=4DA0OLcqXvs">> 플레이 테스트 영상 바로가기<br>
<a href = "https://github.com/guluming/BlockPuzzle_project">> 개발 Github 바로가기[private]<br>
 

## 💌 프로젝트 소개
👉 블럭 퍼즐은 테트리스에서 한층 진화한 형태의 아케이드 게임입니다. 

1️⃣ 가로 혹은 세로로 퍼즐판 채우면 점수를 얻을 수 있어요.

2️⃣ 연속으로 퍼즐판을 채우거나 한 번에 많은 블럭을 없애면 추가점수가!

3️⃣ 처음이라고 걱정하지 마세요! 첫 플레이시 친절한 튜토리얼도 제공!

4️⃣ 만약 클래식 모드를 마스터했다면 챌린지 모드에 도전해보세요![베타 버전 이후 ]

<br><br><br>
 
## ⏱ 프로젝트 기간
> 23.01.24 - 23.02.24 진행중 <베타 버전 배포>(5주++)

<br/>
 
## 🔀 블럭퍼즐 게임 시스템 흐름
<p align="center">
<img src="https://user-images.githubusercontent.com/105046055/220897172-5aefa547-3c3d-4a8f-a111-cd23c0c981fa.jpg" width="50%" height="50%">
</p><br><br><br>
  
## 🏹 SKILLS
### - PLATFORMS & LANGUAGE 
![csharp](https://img.shields.io/badge/-C%23-blue)
![unity](https://img.shields.io/badge/-unity-white)
<br>

### - COLLABORATION & TOOLS 
![Git](https://img.shields.io/badge/Git-F05032.svg?&style=for-the-badge&logo=Git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717.svg?&style=for-the-badge&logo=GitHub&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B.svg?&style=for-the-badge&logo=Slack&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E.svg?&style=for-the-badge&logo=Figma&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000.svg?&style=for-the-badge&logo=Notion&logoColor=white)
<br><br><br>
  
## 🛰️ FEATURES
> 1. 퍼즐판, 퍼즐 블록 Prefabs를 이용한 생성
- 생성 알고리즘을 통해서 1개의 Prefabs를 이용하여 여러 오브젝트 생성<br><br>

> 2. Unity Editor를 이용한 블록 데이터 생성
- 새로운 블록을 만들때마다 Unity Editor로 만든 Data로 블록 생성<br><br>
  
> 3. ScriptableObject를 통한 블록 텍스쳐 등록
- 블록 텍스쳐를 ScriptableObject를 통해 한 곳에 등록하여 관리
- 새로운 블록 텍스쳐 확장에 용이하도록 설계<br><br>
 
> 4. BinaryDataStream을 이용한 사용자 데이터 저장
- PlayerPrefs을 이용한 저장이 아니라 Json형태로 데이터를 만들어 BinaryData형태로 저장
- 게임 옵션, 게임 상태를 유저 상황에 맞게 저장
- 추후 서버를 사용하게 되면 저장경로만 바꾸어 사용자 데이터 반영구 보존 가능<br><br>
  
> 5. AppLovinMax를 이용한 광고 미디에이션 구현
- 광고 미디에이션 구현을 통해 광고 수익 극대화
- 특정 광고 플랫폼에 한정되지 않아 일시적으로 광고 게시가 중지 되어도 무관<br><br>
  
> 5. Firebase 패키지를 통한 앱 관리
- 앱내 비정상작동을 감지하여 버전에 따른 치명적인 버그 관리 가능
- Firebase에서 제공하는 푸시 메시지 기능을 사용하면 유저에게 지속적인 알림 가능<br><br><br>
 
 
## 🔥 TROUBLE SHOOTING

### 1️⃣ 프로젝트 빌드 중 "Gradle Build error" 발생
 
**문제:** 
 
프로젝트를 APK파일로 빌드중 "Gradle Build error"가 발생하고 빌드 실패
<br><br>
 
**원인:** 
 
유니티 프로젝트안에서 사용하는 여러 SDK를 설치할 때 Class가 중복으로 설치되어서 생기는 문제
<br><br>

**해결방안:**
 
에러 로그에 나타나는 중복되는 Class들이 있는 위치로가서 중복되는 Class들을

1개만 남기고 삭제하여 문제를 해결
<br><br><br><br>

### 2️⃣ AppLovin 설치 후에 "java.lang.UnsupportedOperationException: This feature requires ASM7" 발생
 
**문제**
 
AppLovin 패키지를 설치하고 프로젝트를 APK파일로 빌드중 해당 오류가 발생하고 빌드 실패
<br><br>

**원인**

프로젝트 빌드시 Publishing Settings중에 Minify의 설정 체크를 안해서 생긴 문제
<br><br>
 
**해결방안**

프로젝트 빌드시 Publishing Settings중에 Minify의 설정중에

Use R8, Release, Debug를 모두 체크 해야됨
