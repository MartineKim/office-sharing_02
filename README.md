[README.md](https://github.com/user-attachments/files/32738450/README.md)
# 공유오피스 비즈플러스 랜딩페이지

정적 HTML/CSS/JS 단일 파일(`index.html`)로 만들어진 비상주사무실 랜딩페이지입니다.
별도 빌드 과정 없이 그대로 GitHub Pages에 올릴 수 있습니다.

## GitHub에 올리는 방법

1. GitHub에서 새 저장소(repository)를 만듭니다. (예: `bizplus-site`)
2. 이 폴더의 `index.html`을 저장소 루트에 업로드합니다.
   - GitHub 웹사이트에서 "Add file → Upload files"로 드래그 앤 드롭 가능
3. 저장소 **Settings → Pages**로 이동합니다.
4. Source를 `Deploy from a branch`로 선택하고, Branch는 `main` / 폴더는 `/ (root)`로 설정 후 저장합니다.
5. 몇 분 뒤 `https://{깃허브아이디}.github.io/{저장소이름}/` 주소로 사이트가 공개됩니다.

## 반드시 채워야 할 부분

파일 안에 아래 항목들이 `(입력 필요)`로 표시되어 있으니 실제 정보로 교체해 주세요.

- [ ] 전화번호 (`위치`, `이용요금` 섹션)
- [ ] 사업자등록번호, 이메일 (`footer`)
- [ ] 지도 영역 — 네이버/카카오 지도 embed 코드로 교체 (`#location`)
- [ ] 오피스 사진 4장 — `.ph` 플레이스홀더를 `<img>` 태그로 교체 (`#gallery` 섹션)
- [ ] 이용 후기 — 실제 후기가 모이면 예시 문구를 교체

## 상담 신청 폼 연결

`#contact`의 폼은 현재 알림창만 뜨는 데모 상태입니다. 실제로 접수받으려면 다음 중 하나를 연결하세요.

- [Formspree](https://formspree.io) — `<form>`의 `action`에 발급받은 주소를 넣기만 하면 됩니다.
- Google Forms — 구글 폼을 만들고 iframe 임베드 혹은 fetch로 연동
- 자체 백엔드(Node.js, PHP 등)로 데이터 수신

## 요금 체계 안내

요금표는 더브릿지플러스와 동일한 체계(비상주 개인/법인 요금제, 상주 오피스 요금제)로 구성했습니다.
실제 계약 조건이 다르다면 `index.html`의 `<table class="price-table">` 부분 숫자만 수정하면 됩니다.
