# Google Play Data Safety 초안

기준일: 2026-04-24  
대상 앱: 포머리 (Foamory)  
패키지명: `app.foamory.mobile`

이 문서는 **현재 앱 기능 기준**으로 작성한 Google Play Console 입력 초안입니다.

## 1. 현재 버전 기준 요약

현재 포머리는:

- 회원가입/로그인 없음
- 개발자 서버 전송 없음
- 광고 SDK 없음
- 결제 SDK 없음
- 분석 SDK 없음
- 사용자가 입력한 세차 일지/상품 정보는 **기기 내부 저장**
- 이미지 저장 기능을 위해 사진 저장 관련 권한만 요청 가능

따라서 현재 기준으로는 **사용자 데이터를 수집하거나 공유하지 않는 앱**으로 정리하는 방향이 맞습니다.

## 2. Play Console 입력 초안

### 데이터 수집 및 공유

- **Does your app collect or share any of the required user data types?**
  - `No`

### 보안 처리

- **Is all user data collected by your app encrypted in transit?**
  - `No` 또는 `Not applicable`
  - 이유: 현재 버전은 사용자 데이터를 서버로 전송하지 않음

- **Do you provide a way for users to request that their data is deleted?**
  - `Yes`
  - 이유: 사용자는 앱 내 수정/삭제 또는 앱 삭제를 통해 로컬 데이터를 제거 가능

## 3. 왜 "수집 안 함"으로 보는가

Google Play Data Safety 기준상:

- 데이터가 **기기 밖으로 전송되지 않고 온디바이스에서만 처리**되면 수집으로 보지 않을 수 있음
- 현재 포머리의 세차 일지, 메모, 사용자 추가 상품 데이터는 내부 저장소에만 저장됨
- 사진 저장 권한은 기능 수행용 권한일 뿐, 서버 수집이 아님

## 4. 개인정보처리방침과 맞춰야 하는 내용

Data Safety와 아래 문서는 서로 일치해야 합니다.

- [privacy-policy.html](./privacy-policy.html)

현재 문서와 Data Safety는 다음 기준으로 맞춰져 있습니다.

- 세차 일지 정보: 기기 내부 저장
- 사용자 추가 상품/브랜드 정보: 기기 내부 저장
- 사진 저장 권한: 이미지 저장 기능 제공용
- 제3자 제공 없음

## 5. 나중에 반드시 수정해야 하는 경우

아래 기능이 추가되면 이 초안을 그대로 쓰면 안 됩니다.

### 광고 SDK 추가 시

예: AdMob

가능성이 높은 변경:

- 광고 ID
- 기기 정보
- 앱 활동
- 진단 정보

이 경우:

- Data Safety를 `No`에서 `Yes`로 바꿔야 할 수 있음
- 개인정보처리방침에도 광고 SDK 사용 사실 반영 필요

### 인앱 결제 추가 시

예: Google Play Billing

대체로 결제 정보 자체는 Google Play가 직접 처리하지만,

- 구매 상태 저장 방식
- 계정 식별 여부
- 서버 검증 여부

에 따라 공개 내용이 달라질 수 있습니다.

### 분석 SDK 추가 시

예: Firebase Analytics, Crashlytics

이 경우 보통 다음 항목이 추가될 수 있습니다.

- 앱 활동
- 기기 또는 기타 식별자
- 크래시 로그
- 진단 정보

## 6. 운영 시 추천

출시 직전 체크:

1. 실제 앱에 광고/결제/분석 SDK가 없는지 다시 확인
2. AndroidManifest 권한과 포함 라이브러리 확인
3. 개인정보처리방침 URL 공개 상태 확인
4. Play Console Data Safety와 문서 문구 일치 여부 확인

## 7. 공식 참고

- Google Play User Data policy  
  https://support.google.com/googleplay/android-developer/answer/9888076

- Google Play Data Safety form  
  https://support.google.com/googleplay/android-developer/answer/10787469
