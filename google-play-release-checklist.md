# Google Play 출시 체크리스트

기준일: 2026-04-24  
앱: 포머리 (Foamory)

## 1. 앱 파일

- [ ] 릴리즈 AAB 준비
  - [foamoryApp-release.aab](../foamoryApp/build/outputs/bundle/release/foamoryApp-release.aab)
- [ ] 내부 테스트 트랙 업로드
- [ ] 실제 기기 설치 테스트

## 2. 스토어 자료

- [ ] 앱 이름 확정
- [ ] 짧은 설명 입력
- [ ] 긴 설명 입력
- [ ] 앱 아이콘 확인
- [ ] 스크린샷 업로드
  - [store-assets/google-play/phone](/Users/225766/Documents/project/carwash/store-assets/google-play/phone)
- [ ] Feature Graphic 업로드
  - [feature-graphic.png](/Users/225766/Documents/project/carwash/store-assets/google-play/feature/feature-graphic.png)

## 3. 개인정보 / 정책

- [ ] 개인정보처리방침 이메일 실제 값으로 변경
- [ ] 개인정보처리방침 공개 URL 준비
- [ ] Google Play Data Safety 입력
- [ ] 앱 콘텐츠 설문 완료
- [ ] 광고 포함 여부 체크
- [ ] 타겟 연령층 설정

## 4. 현재 앱 기준 Data Safety 방향

- 사용자 데이터 수집/공유: `No`
- 이유: 현재 버전은 사용자 데이터를 서버로 전송하지 않고 기기 내부에만 저장

주의:

- 광고 SDK(AdMob) 추가 시 재작성 필요
- 인앱결제 추가 시 재검토 필요
- Firebase Analytics / Crashlytics 등 분석 SDK 추가 시 재작성 필요

## 5. GitHub Pages 공개

- [ ] 저장소 push
- [ ] `docs/` 폴더로 GitHub Pages 활성화
- [ ] 아래 URL 확인
  - `https://<github-id>.github.io/<repo>/privacy-policy.html`

## 6. 출시 전 최종 점검

- [ ] 앱 실행 문제 없음
- [ ] 권한 요청 문구 확인
- [ ] 스토어 문구와 실제 앱 기능 일치
- [ ] 개인정보처리방침과 Data Safety 문구 일치
- [ ] 문의 이메일 수신 가능 여부 확인

## 7. 관련 문서

- [GitHub Pages 메모](./README.md)
- [개인정보처리방침](./privacy-policy.html)
- [Data Safety 초안](./google-play-data-safety-draft.md)
- [스토어 등록 문구 초안](./google-play-store-listing-draft.md)
