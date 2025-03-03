
# 🏟 Baseball Archive

## ⚾️ 프로젝트 목적

**Baseball Archive**은 야구 직관 경험을 기록하고 공유할 수 있는 웹 애플리케이션입니다. 야구 팬들은 경기장에서의 특별한 순간들을 저장하고, 과거 직관 기록을 되돌아보며, 다른 팬들과 소통할 수 있습니다. 야구 팬이라면 한 시즌 동안 여러 경기를 직관하고 싶겠지만, 시간이 지나면 어떤 경기를 직관했는지, 누구와 함께했는지, 어떤 기억이 남았는지 흐려지기 마련입니다. 그런 직관 경험을 관리하고 쉽게 회상할 수 있도록 도와줍니다.

<br/>

## ⚾️ 프로젝트 일정

2024.08.05 ~ 2024.08.26

<br/>

## ⚾️ 팀 구성 및 역할

<table width="100%">
  <tbody>
     <tr>
      <td colspan="3" align="center"><b>FE</b></td>
      <td colspan="3" align="center"><b>BE</b></td>
    </tr>
      <tr>
      <td align="center">
        <a href="https://github.com/yeonjoo8231">
          <img src="https://avatars.githubusercontent.com/u/77268860?v=4" width="100px;" alt="김연주"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/ja-gypsophila">
          <img src="https://avatars.githubusercontent.com/u/128439902?v=4" width="100px;" alt="김장훈"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/PARKJEONGJOON">
          <img src="https://avatars.githubusercontent.com/u/99483101?v=4" width="100px;" alt="박정준"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/gixxla">
          <img src="https://avatars.githubusercontent.com/u/131466335?v=4" width="100px;" alt="김이원"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/bang-wol">
          <img src="https://avatars.githubusercontent.com/u/102708198?v=4" width="100px;" alt="방수빈"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/hyoeun0001">
          <img src="https://avatars.githubusercontent.com/u/83484611?v=4" width="100px;" alt="최효은"/>
        </a>
      </td>   
    </tr>
    <tr>
      <td align="center"><b><a href="https://github.com/yeonjoo8231">김연주</a></b></td>
      <td align="center"><b><a href="https://github.com/ja-gypsophila">김장훈</a></b></td>
      <td align="center"><b><a href="https://github.com/PARKJEONGJOON">박정준</a></b></td>
      <td align="center"><b><a href="https://github.com/gixxla">김이원</a></b></td>
      <td align="center"><b><a href="https://github.com/bang-wol">방수빈</a></b></td>
      <td align="center"><b><a href="https://github.com/hyoeun0001">최효은</a></b></td>
    </tr>
  </tbody>
</table>

<br/>

## ⚾️ 시스템 아키텍처

<img width="600" alt="architecture" src="https://github.com/user-attachments/assets/38656672-6c58-48fe-8fc6-93c3773465bb" />

<br/>

## ⚾️ ERD 

<img width="600" alt="ERD" src="https://github.com/user-attachments/assets/ded34456-15e9-432f-ae63-49ae654704ad" />

### 테이블 정보
- **user(사용자)**  
  - Firebase Authentication을 통해 `uid` 생성 → PK로 사용
  - 닉네임, 프로필 사진, 응원 팀 정보 저장

- **baseball_team(야구 팀)**  
  - 모든 야구 팀 정보 저장

- **baseball_ranking(야구 순위)**  
  - 팀 순위, 경기 수, 승패, 승률 저장

- **baseball_schedule(경기 일정)**  
  - 홈팀/원정팀, 구장 등 크롤링한 경기 일정 저장

- **archive(직관 기록)**  
  - 직관 기록, 점수, 날씨, 사진, 공개 여부 저장

- **board(자유게시판)**  
  - 경기 관련 게시글 작성 가능

- **like(좋아요)**  
  - `like_archive`, `like_board`로 분리해 직관 기록, 게시글 좋아요 관리

- **comment(댓글)** 
  - `comment_archive`, `comment_board`로 분리해 댓글 관리

  
<br/>

> **☄️ 왜 Firebase와 PostgreSQL을 함께 사용하나요?**  
Firebase는 OAuth 로그인 및 인증 관리에 최적화되어 있음. PostgreSQL에서는 사용자의 추가 정보(닉네임, 응원 팀 등)를 관리하여 보안성과 확장성 확보.

> **☄️ 왜 경기 일정을 미리 크롤링해서 DB에 저장하나요?**  
API 호출할 때마다 크롤링을 실행하면 속도가 느려지고 서버 부하가 커짐. 따라서 미리 저장된 데이터를 조회하는 방식으로 성능 최적화.

<br/>

## ⚾️ API

- API 상세 내용은 아래 노션 문서에서 확인할 수 있습니다.

  [🔗 API 문서 바로가기](https://statuesque-ink-11b.notion.site/API-1ab511911fb980dcb191f2f9b22f8747)

<br/>


## ⚾️ 프로젝트 시연

### 회원가입 및 로그인

https://github.com/user-attachments/assets/f3414cbe-37a3-43b3-abe1-29f15e500994

### 직관 기록하기

https://github.com/user-attachments/assets/73be580d-e1d4-4a2a-bdc9-a901d8c5b2cf

### 커뮤니티 및 직관 기록 보기

https://github.com/user-attachments/assets/11210149-98d9-4b58-946d-ccb867d0978b


### 경기 일정 및 순위 확인

https://github.com/user-attachments/assets/a9240402-bfa7-4237-842c-8a8ccfe9dd34

