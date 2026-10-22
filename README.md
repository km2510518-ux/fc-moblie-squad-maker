# FC Squad Lab — FC Mobile Squad Builder

PC와 모바일에서 사용할 수 있는 팬 제작 스쿼드 메이커입니다. Vite + React로 만들었으며 무료 정적 호스팅에 배포할 수 있습니다.

## 포함 기능

- 반응형 PC / 모바일 UI
- 4-3-3 공격, 4-2-4, 4-3-3 수비, 4-2-3-1, 3-5-2, 4-1-2-1-2 포메이션
- 선수 검색, 시즌 필터, 포지션 필터
- 선수 카드 직접 추가 / 편집 / 삭제
- 시즌별 카드 테마: TOTY, UTOTY, TOTS, HOL, UCL, ICON, HERO, BASE
- OVR 및 간단한 강화 단계 표시
- 팀 OVR 계산
- localStorage 자동 저장
- 스쿼드 보드 PNG 이미지 저장

## 로컬에서 실행하기

Node.js 20 이상 권장.

```bash
npm install
npm run dev
```

터미널에 표시되는 로컬 주소를 브라우저에서 엽니다.

프로덕션 빌드 확인:

```bash
npm run build
npm run preview
```

## 무료 공개 배포: Vercel

1. GitHub 계정을 만들고 새 저장소를 만듭니다.
2. 이 프로젝트 파일 전체를 저장소에 업로드합니다.
3. https://vercel.com 에서 GitHub로 로그인합니다.
4. **Add New → Project**를 누르고 저장소를 가져옵니다.
5. Framework Preset은 `Vite`, Build Command는 `npm run build`, Output Directory는 `dist`로 설정합니다. 대부분 자동 감지됩니다.
6. **Deploy**를 누릅니다. 완료되면 `https://프로젝트이름.vercel.app` 형식의 공개 주소가 발급됩니다.
7. GitHub에 변경 사항을 올리면 Vercel이 다시 배포합니다.

## 대안: Netlify

1. https://www.netlify.com 에서 로그인합니다.
2. GitHub 저장소를 연결합니다.
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Deploy site를 실행합니다.

## 중요 안내

- 이 프로젝트의 초기 선수 목록은 **기능 확인용 예시 데이터**입니다. 실제 게임의 공식 선수 DB나 실시간 시세와 연결되어 있지 않습니다.
- 선수 데이터와 스쿼드 편집 내용은 현재 브라우저의 `localStorage`에 저장됩니다. 같은 기기·브라우저에서는 유지되지만 다른 기기와 자동 동기화되지 않습니다.
- OVR 강화 계산은 단순 표시용으로 `기본 OVR + 강화 단계`를 사용합니다. 실제 FC Mobile의 계산식과 다를 수 있습니다.
- 카드 그래픽은 시즌 분위기를 표현한 자체 CSS 디자인이며 공식 카드 이미지나 EA의 상표 자산을 포함하지 않습니다.
- 실제 선수 데이터, 공식 카드 이미지, 실시간 시장 가격을 사용하려면 이용 조건과 데이터 공급원을 별도로 확인해야 합니다.
- PNG 저장은 브라우저에서 처리합니다. 인터넷 연결 없이도 핵심 편집 기능은 동작하지만 Google Fonts는 연결 상태에 따라 기본 글꼴로 표시될 수 있습니다.

## 기술 스택

- React 18
- Vite 6
- lucide-react
- html-to-image
