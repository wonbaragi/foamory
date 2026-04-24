# GitHub Pages 배포 메모

이 폴더는 GitHub Pages용 공개 문서 루트로 사용할 수 있습니다.

## 추천 URL 구조

- `https://<github-id>.github.io/<repo>/`
- `https://<github-id>.github.io/<repo>/privacy-policy.html`

## GitHub Pages 설정

1. 이 프로젝트를 GitHub 저장소로 push
2. GitHub 저장소의 `Settings -> Pages`
3. `Build and deployment`에서:
   - `Source`: `Deploy from a branch`
   - `Branch`: `main` 또는 사용하는 기본 브랜치
   - `Folder`: `/docs`
4. 저장
5. 배포 완료 후 발급된 URL 확인

## Google Play에 넣을 값

- 개인정보처리방침 URL:
  - `https://<github-id>.github.io/<repo>/privacy-policy.html`

## 출시 전 체크

- [privacy-policy.html](./privacy-policy.html) 안의 문의 이메일을 실제 운영 이메일로 변경
- 광고/결제/분석 SDK를 붙이면 개인정보처리방침과 Data Safety 문서를 함께 수정
