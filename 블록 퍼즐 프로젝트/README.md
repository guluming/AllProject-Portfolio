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

<br><br>
 
## ⏱ 프로젝트 기간
> 23.01.24 - 23.02.24 진행중 [베타 버전 배포](5주++)

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
- ㅃㅃㅃㅃㅃㅃㅃㅂ<br><br>

> 2. Unity Editor를 이용한 블록 데이터 생성
- ㅃㅃㅃㅃㅃㅃㅃㅃㅃㅃㅃ<br><br>
  
> 3. 대결 등록/수락/신청
- 팀을 생성한 사용자의 경우 대결 등록을 통해 대결 신청을 받을 수 있음
- 대결등록을 하고 신청이 들어온 상대의 연락처를 통해 경기 일정 조정
- 대결 등록을 한 상대의 정보를 보고 대결 신청 가능<br><br>
  
> 4. 경기 종료/경기 결과/ 경기 인원/ 경기 히스토리(팀, 개인)
- 경기 종료 시 경기결과 입력 후 상대팀에게 해당 결과 확인
- 경기결과 확인 후 각 팀은 해당 경기에 참여한 인원 및 MVP등 추가적인 경기결과 입력
- 경기 결과 및 경기에 참여한 인원, 교체 선수, MVP, 분위기 메이커 등등 선정하여 등록 가능
- 등록된 경기 히스토리의 경우 언제든 조회 가능<br><br>
  
> 5. 팀 정보 조회/ 팀 경기 히스토리/ 개인 경기 히스토리/ 개인 정보 조회
- 팀 정보 상세 조회시 팀의 전적, 멤버, 경기 히스토리등 해당 팀과 관련된 여러 추가적인 정보 확인 가능
- 개인 정보 상세 조회시 포지션별 점수, 전적, 참여했던 경기 히스토리등 추가적인 정보 확인 가능<br><br>
  
> 6. 팀 랭킹 조회/선수 랭킹 조회/ 개인 랭킹
- 팀의 경우 승점과 승률을 기준으로 상위 10개팀을 순위별로 조회
- 개인의 경우 설정한 포지션별로 포지션 점수 상위 10명을 순위별로 조회
- 로그인한 사용자의 개인의 순위와 자신이 참여하고 있는 팀들 순위를 따로 조회 가능<br><br><br>
 
 
## 🔥 TROUBLE SHOOTING

### 1️⃣ DB 사용 중 "too many to connections" 발생
 
**문제:** 
 
 EC2 서버를 켜 놓은 지 1시간이 경과하자 too many to connections 에러가 발생하고 
 
 서버가 먹통 되는 문제가 발생
 
**원인:** 
AWS RDS MariaDB에서 최대로 연결할 수 있는 커넥션 수가 31로 적게 설정되어 있었고, 
 
31이 모두 차 버리자 더 이상 커넥션을 연결할 수 없어서 생긴 문제로 원인 추정

**해결방안:**
 
최대로 연결할 수 있는 커넥션 수를 300으로 확장하고, 커넥션이 유지되는 최대 시간이 
 
기본 값으로(86,400초)로 설정되어 있어서 일정 시간 동안 커넥션이 연결되는 수를 계산하여 
 
커넥션이 유지되는 최대 시간을 설정할 수 있는 wait_timeout 파라미터 값과 
 
interactive_timeout 파라미터 값을 설정 후 적용
 

### 2️⃣ DB 사용 중 "HttpHostConnectException" 발생
 
**문제**

부하 테스트 중 HttpHostConnectException 발생 

**원인**

아파치 톰캣의 기본 쓰레드 할당 값이 200 정도로 설정되어 있었고 지정된 수 이상이면 

서버에서 timeout이 발생하는 것으로 확인
 
**해결방안**
 
프로덕션 서버에서 해당 오류가 발생하면
 
서버 쪽의 max_connection과 max_thread 값을 수정하여 대처하면 된다는 것을 확인
