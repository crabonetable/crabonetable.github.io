# 양평꽃게한상 홈페이지

GitHub Pages로 공개하는 한 페이지짜리 식당 홈페이지입니다. 디자인 콘셉트는 한지 바탕, 먹색, 로고의 꽃게색, 금색 테두리를 쓴 한정식집 분위기입니다.

## 파일 구성
| 파일 | 용도 |
|---|---|
| `index.html` | 홈페이지 전체 |
| `images/logo.png` | 투명 배경 로고 (밝은 바탕용) |
| `images/logo-light.png` | 글씨를 밝은색으로 바꾼 로고 (어두운 바탕용, 하단) |
| `images/crab.png`, `images/crab-light.png` | 꽃게 그림만 잘라 낸 아이콘 |
| `images/favicon.png` | 브라우저 탭 아이콘 |
| `images/logo-original.png` | 받은 로고 원본 |
| `images/menu-*.jpg` | 대표 음식·신메뉴 사진 (간장게장, 양념게장, 돈까스 포스터) |
| `images/gallery-*.jpg` | 머무는 공간 사진 (전경, 간장게장, 사인, 방송 출연, 돈까스) |

## 내용 수정하는 곳 (`index.html`)
| 바꿀 내용 | 찾을 단어 |
|---|---|
| 메뉴·가격 | `<!-- 차림표 -->` 아래 `<li>` 줄 |
| 대표 음식 카드 | `<!-- 대표 음식 -->` |
| 소개 문구 | `<!-- 이야기 -->` |
| 영업시간·휴무 | `<!-- 오시는 길 -->`, `<!-- 문의 -->`, 첫 화면 `statusText`, 맨 아래 `<script>`의 `open`, `last`, `close`, `day === 2` |
| 전화번호 | `tel:` 로 검색 |
| 사업자 정보 | `<!-- 사업자 정보` 주석을 풀고 채우기 |

## 사진 넣는 방법
1. `images` 폴더에 사진을 넣습니다. 예: `images/ganjang.jpg`
2. `index.html`에서 사진 자리를 찾습니다.
   ```html
   <div class="photo"><div class="ph">사진 준비 중</div></div>
   ```
3. 안쪽을 사진으로 바꿉니다.
   ```html
   <div class="photo"><img src="images/ganjang.jpg" alt="간장게장정식"></div>
   ```
   공간 사진은 `<div class="photo light">` 형태이며 같은 방법으로 바꿉니다.

사진은 가로 1600px 이하, 장당 500KB 이하로 줄여서 올리면 빨리 열립니다. 대표 음식 사진은 정사각형에 가까운 것이 잘 맞습니다.

## GitHub Pages로 공개하기
1. github.com에서 로그인 후 새 저장소(Repository)를 만듭니다. 이름 예: `crabonetable`, Public 선택
2. `Add file` → `Upload files`로 `index.html`과 `images` 폴더를 올리고 `Commit changes`
3. 저장소의 `Settings` → `Pages` → Source를 `Deploy from a branch`, Branch를 `main` / `(root)`로 지정 후 Save
4. 1~2분 뒤 `https://아이디.github.io/crabonetable/` 주소로 열립니다.

## 공개 후 할 일
- 네이버 플레이스 관리(스마트플레이스)에 홈페이지 주소 등록
- 네이버 서치어드바이저, 구글 서치콘솔에 사이트 등록
- (선택) 개인 도메인 연결: Settings → Pages → Custom domain
