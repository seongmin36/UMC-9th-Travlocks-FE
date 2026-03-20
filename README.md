<p align="center">
  <img src="https://github.com/dinah05/email-template/blob/main/assets/travlocks_logo.png?raw=true" alt="Travlocks Logo" width="220" />
</p>

# Travlocks Web

**UMC 9th Project**

<br/>

<div>

  ## ✈️ Travlocks : 여행 일정을 빠르게, 직관적으로, 재미있게!

  > **블록을 쌓듯 여행 일정을 만드는 새로운 방식의 웹 서비스 Travlocks**의 프론트엔드 저장소입니다.
</div>

<br/>

<div>

## 📌 Travlocks는 이런 서비스예요

Travlocks는
**AI를 활용해 여행 일정을 빠르고 직관적으로 설계할 수 있도록 돕는 블록형 여행 일정 웹 서비스**입니다.

- 텍스트 입력이나 복잡한 리스트 작성이 아닌,
- 블록을 쌓듯 직관적으로 여행 일정을 구성해
- 여행 설계의 **인지적 부담**을 줄이는 것에 집중합니다.

> "여행을 '짜는' 게 아닌 '쌓는' 즐거움을 유저에게"

</div>

<br/>

<div>

## 🚀 로컬 실행

> 배포 링크: [travlocks.com](https://travlocks.com)


```bash
pnpm install
pnpm dev
# http://localhost:5173
```

**서버 없이 확인 가능한 기능:**
- 인트로 애니메이션 (스플래시 → 비행기 전환)
- 블록 드래그 & 스냅 연결
- Undo/Redo (Cmd+Z / Cmd+Y)
- 인증 UI 플로우

**백엔드 필요:**
- AI 동선 최적화
- 소셜 로그인 (OAuth)

</div>

<br/>

<div>

  ## 💻 기술 스택

| **역할**             | **종류**                                                                                                                                                                                                                                                                                                                        | **선정 이유**                                                                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Library              | <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=white">                                                                                                                                                                                                                            | 컴포넌트 기반 구조로 재사용성과 유지보수성이 높아 개발 효율을 극대화 가능                                                                    |
| Programming Language | <img src="https://img.shields.io/badge/typescript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>                                                                                                                                                                                                                 | 정적 타입을 제공하여 코드의 안정성과 가독성을 높이고, 개발 중 오류를 사전에 방지할 수 있어 유지보수에 유리                                   |
| Styling              | <img src="https://img.shields.io/badge/tailwindcss-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">                                                                                                                                                                                                                | 유틸리티 클래스 기반의 스타일링으로 반복되는 CSS 코드 작성을 줄이고, 빠르고 일관된 UI 구현 가능                                              |
| Data Fetching        | <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=Axios&logoColor=white">                                                                                                                                                                                                                            | 직관적인 API 사용법과 자동 JSON 변환 기능으로 비동기 통신이 간편                                                                             |
| State Management     | <img src="https://img.shields.io/badge/TanStackQuery-FF4154?style=for-the-badge&logo=reactquery&logoColor=white"> <img src="https://img.shields.io/badge/Zustand-black?style=for-the-badge&logoColor=white">                                                                                                                    | 서버 상태는 TanStack Query의 캐싱과 동기화 기능을 통해 효율적으로 관리하고, 전역 상태는 Zustand를 활용해 최소한의 보일러플레이트로 관리 가능 |
| Routing              | <img src="https://img.shields.io/badge/ReactRouter-CA4245?style=for-the-badge&logo=ReactRouter&logoColor=white">                                                                                                                                                                                                                | SPA에 최적화된 라우팅 기능 제공, 선언적 방식으로 라우트를 쉽게 구성 가능                                                                     |
| Formatting           | <img src="https://img.shields.io/badge/eslint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white"> <img src="https://img.shields.io/badge/prettier-000000?style=for-the-badge&logo=prettier&logoColor=F7B93E"> <img src="https://img.shields.io/badge/stylelint-263238?style=for-the-badge&logo=stylelint&logoColor=white"> | 코드 스타일을 통일하고 잠재적인 오류를 사전에 방지하여 협업 시 효율성을 높임                                                                 |
| Package Manager      | <img src="https://img.shields.io/badge/pnpm-F69220?style=for-the-badge&logo=pnpm&logoColor=white">                                                                                                                                                                                                                              | 빠른 설치 속도와 안정적인 패키지 관리 기능으로 프로젝트 환경 설정에 용이                                                                     |
| Deployment           | <img src="https://img.shields.io/badge/vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">                                                                                                                                                                                                                          | Git 연동 기반의 자동 배포, 프론트엔드 프로젝트에 최적화된 환경 제공으로 빠른 개발 및 배포 사이클 지원                                        |
| Bundler              | <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=Vite&logoColor=white">                                                                                                                                                                                                                              | 빠른 서버 시작과 모듈 번들링 성능으로 개발 생산성을 향상                                                                                     |

</div>

<br/>

<div>

## 📂 핵심 구조

```
src/
├── feature/block-builder/   # 블록 편집 핵심 로직 (apis, components, hooks, ui, types)
├── pages/                   # 라우팅 페이지
└── shared/                  # 전역 공통 모듈
    ├── apis/                # Axios 인스턴스 + Interceptor
    ├── hooks/               # queries, mutations
    ├── stores/              # Zustand 전역 상태
    └── utils/               # 유틸 함수
```

> 비즈니스 로직(`feature`)과 재사용 모듈(`shared`)을 엄격히 분리하여, 기능 확장 시 영향 범위를 최소화하고 유지보수성을 높였습니다.

</div>

<br/>

<div>

## 🙋🏻‍♀️ Travlocks의 FE Developer를 소개합니다!

| <a href="https://github.com/jinhyo0"><img src="https://avatars.githubusercontent.com/u/150879545?v=4" width="120px;" alt=""/></a> | <a href="https://github.com/seongmin36"><img src="https://avatars.githubusercontent.com/u/202721995?v=4" width="120px;" alt=""/></a> | <a href="https://github.com/onebone"><img src="https://avatars.githubusercontent.com/u/3233503?v=4" width="120px;" alt=""/></a> | <a href="https://github.com/codmoni"><img src="https://avatars.githubusercontent.com/u/160315926?v=4" width="120px;" alt=""/></a> |
| --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 김진효                                                                                                                            | 조성민                                                                                                                               | 정윤철                                                                                                                          | 황무원                                                                                                                            |

</div>

<br/>

<div>

## 조성민 [@seongmin36](https://github.com/seongmin36)

인트로 애니메이션부터 인증 플로우 전반, 그리고 서비스의 핵심인 블록 편집 페이지까지 담당했습니다.

---

### 인트로 & 홈화면

> `Framer Motion` `AnimatePresence` `Zustand` `Singleton Pattern`

<table>
<tr>
<td align="center"><b>스플래시 → 비행기 인트로</b></td>
<td align="center"><b>홈화면</b></td>
</tr>
<tr>
<td>

https://github.com/user-attachments/assets/22983ecb-49e8-48b2-9b0a-57b8e297c537

</td>
<td>

https://github.com/user-attachments/assets/4332e6a0-15e2-4518-b451-52d62cbd2642

</td>
</tr>
</table>

Travlocks는 '여행을 떠난다'는 느낌을 진입 순간부터 전달하는 것이 중요했습니다. `motion/react(Framer Motion)`의 `AnimatePresence` + `exit` prop을 핵심으로 스플래시 2단계와 비행기 인트로 애니메이션을 구현했습니다.

**라이브러리 선택 근거**

단순히 "애니메이션 라이브러리라서 편하다"는 이유가 아니라, intro/outro · inView · hover 같은 UI 인터랙션 모션이 반복적으로 필요한 상황에서 `initial/animate/exit`, `whileHover`, `whileInView` 같은 **선언형 API로 모션 구현을 한 패턴으로 통일**할 수 있다는 점을 먼저 세웠습니다.

React에서 조건부 렌더링 시 컴포넌트가 빠지는 순간 DOM이 즉시 제거(unmount)되기 때문에, 퇴장(outro) 애니메이션을 안정적으로 재생하려면 **DOM을 잠깐 유지했다가 애니메이션 종료 후 제거하는 Presence 흐름**을 직접 설계해야 합니다. `AnimatePresence` + `exit`는 이 문제를 라이브러리 레벨의 표준 패턴으로 제공합니다.

**삽질 — 버블·퍼즐 깜빡임 버그**

새로고침 시 메인 화면 버블과 퍼즐이 화면 상단에서 잠깐 반짝이는 현상이 발생했습니다. `delaySec`가 0~8.5초 사이 랜덤 값이라 지연 시간이 길수록 잘못된 위치에 더 오래 노출되었습니다.

원인은 Framer Motion이 `initial` prop이 없으면 `y: 0`을 기본값으로 첫 프레임을 렌더링하는 것이었습니다. 실제 시작 위치인 `startY`(화면 하단 밖: `h + size + extra`)가 아닌 `y: 0`에 버블 하단이 노출되는 것이었고, React 렌더링 사이클과 Framer Motion 애니메이션 시작 사이의 **타이밍 차이**가 근본 원인이었습니다.

```tsx
// Before — initial 없이 animate만 정의, 첫 프레임에 y: 0 위치가 노출됨
<motion.div animate={{ y: [-startY, -(h + size)] }} transition={{ delay: delaySec }} />

// After — initial을 명시해 지연 시간 동안도 올바른 위치 유지
<motion.div
  // reduce: 기기의 '동작 줄이기(Reduce Motion)' 접근성 설정 — true면 initial을 빈 객체로 두어 애니메이션 생략
  initial={reduce ? {} : { y: startY }}
  animate={{ y: [-startY, -(h + size)] }}
  transition={{ delay: delaySec }}
/>
```

한 줄짜리 수정으로 깜빡임을 완전히 제거했습니다. **"animate만으로는 첫 프레임에서 예상치 못한 위치에 보일 수 있고, 특히 지연 시간이 있는 애니메이션에서는 initial이 필수다"** 는 교훈을 얻었습니다.

**스플래시 타이밍 이슈**

스플래시 상태를 sessionStorage 조건 분기만으로 제어하다가 `SplashExit`가 2번 렌더링되고, 애니메이션 도중 가드가 재계산되어 라우팅이 흔들리는 타이밍 문제가 발생했습니다. `useState` + `useEffect`로 sessionStorage를 동기화하는 구조에서 렌더링이 시작된 뒤 다음 렌더링에서 또 조건을 체크해 중복 렌더링이 발생하는 구조적 문제였습니다.

Zustand store에 `showSplash`, `hasSeenSplash`, `isAnimating`을 단일 상태 원천으로 모으고, `completeSplash` 액션에서 sessionStorage 저장과 세 상태를 **원자적으로** 업데이트해 해결했습니다. `isAnimating` 플래그를 추가해 애니메이션 진행 중에는 리다이렉트 판단 자체를 억제했습니다.

- 스플래시 종료 후 새로고침 시 DOM이 재노출되는 문제 → 애니메이션 완료 상태를 세션 단위로 관리해 해결
- `SplashExit` 중복 렌더링 → Zustand 단일 상태 원천으로 원자적 업데이트

**로딩 애니메이션 프리로드**

Lottie 파일이 컴포넌트 마운트 시점에 fetch되어 배경과 텍스트는 즉시 표시되지만 정작 로딩 애니메이션만 늦게 나타나는 아이러니한 UX 문제가 있었습니다.

`main.tsx` 초기화 시점에 `preloadLottie`를 즉시 실행해 `URL.createObjectURL`로 Blob URL을 생성하고 모듈 스코프 변수에 캐싱하는 **싱글톤 패턴**으로 해결했습니다. Lottie fetch가 컴포넌트 마운트 이후에 시작되던 것을 앱 초기화 시점으로 앞당겨, 앱 렌더링과 병렬로 백그라운드에서 로드되므로 사용자가 체감하는 지연을 제거했습니다.

---

### 인증 플로우 — AuthLayout 통합

> `React Router Outlet Context` `XSS Prevention` `Axios Interceptor`

<table>
<tr>
<td align="center"><b>로그인</b></td>
<td align="center"><b>소셜 로그인 / 온보딩</b></td>
</tr>
<tr>
<td>

https://github.com/user-attachments/assets/61036b24-4312-4aec-9996-ad81572b46b9

</td>
<td>

https://github.com/user-attachments/assets/1b75e19e-c066-4823-8de8-4f9aee8603f3

</td>
</tr>
</table>

초기에는 로그인 · 회원가입 · 비밀번호 재설정 3개 페이지가 각자 독립적인 레이아웃을 갖고 있었습니다. 인증 페이지가 추가될수록 로고 위치나 카드 스타일이 미묘하게 달라질 것을 우려해, 3개 페이지의 레이아웃을 단일 `AuthLayout`으로 통합했습니다. 자식 컴포넌트가 `Outlet context`로 헤더 문구를 동적으로 주입할 수 있게 설계해, 레이아웃은 고정하되 콘텐츠는 유연하게 유지했습니다.

```tsx
// AuthLayout.tsx — Outlet context로 헤더를 동적 주입
const AuthLayout = ({ memberRoutes = false }: AuthLayoutProps) => {
  const [header, setHeader] = useState<AuthLayoutHeader>(DEFAULT_HEADER);

  const ctx = {
    header,
    setAuthHeader,    // 헤더 전체 교체
    updateAuthHeader, // 부분 업데이트
    resetAuthHeader,  // 기본값 복원
  } satisfies AuthLayoutOutletCtx;

  return (
    // key 변경 시 자식 컴포넌트가 완전히 재마운트됩니다.
    // form 입력값 초기화가 의도된 동작이므로 인증 페이지에서는 이 방식을 택했습니다.
    <div key={location.pathname} className="... animate-fade-in">
      {/* 로고, subtitle, description, AuthNavButton */}
      <Outlet context={ctx} />
    </div>
  );
};
```

`key={location.pathname}`을 활용해 경로 변경 시마다 컴포넌트가 재마운트되며 fade-in 애니메이션이 자동으로 트리거됩니다. 별도의 애니메이션 상태 관리 없이 페이지 전환 효과를 구현한 것이 핵심입니다.

**accessToken 보안 강화 — localStorage → 메모리 저장소**

`localStorage`에 accessToken을 저장하면 악성 스크립트가 `localStorage.getItem`으로 토큰을 탈취하는 XSS 공격에 취약합니다. 메모리 기반 저장소로 전환하고 refreshToken은 httpOnly Cookie로 관리하는 구조로 개선했습니다.

**삽질 — 인터셉터 무한루프**

login API가 실패하면 응답 인터셉터가 401로 판단해 토큰 갱신을 시도하고, refresh 자체가 실패하면 다시 refresh를 시도하는 무한루프가 발생했습니다.

`CustomAxiosRequestConfig`에 `skipTokenRefresh` 플래그를 추가하고 인터셉터에서 `originalRequest.skipTokenRefresh`가 true이면 즉시 reject하는 조건 분기로 해결했습니다. login과 refresh API 호출 시 모두 이 플래그를 설정합니다.

---

### Troubleshooting — 소셜 로그인 & 딥링크

> `OAuth` `React Router handle / useMatches` `Generic Type Guard`

**비밀번호 재설정 플로우**

<table>
<tr>
<td align="center"><b>재설정 링크 요청</b></td>
<td align="center"><b>이메일 인증</b></td>
<td align="center"><b>비밀번호 변경</b></td>
</tr>
<tr>
<td>

https://github.com/user-attachments/assets/edfbccd4-0f88-425c-af77-49af2d540efa

</td>
<td>

https://github.com/user-attachments/assets/843dc2ce-8292-47e8-b0e8-a3fc8564875a

</td>
<td>

https://github.com/user-attachments/assets/b4830c46-6377-405b-8bbc-7c5af9f1141a

</td>
</tr>
</table>

소셜 로그인과 비밀번호 재설정 딥링크는 외부 서비스가 개입하는 구간이라 오류가 생겨도 원인을 파악하기 어려웠습니다.

**소셜 로그인 리다이렉트 에러**

OAuth 콜백 처리 시 서버 응답의 `status` 필드로 신규 유저(ONBOARDING)와 기존 유저를 분기해 각각 다른 경로로 라우팅합니다. 초기에는 리다이렉트 URL이 잘못 설정돼 콜백 자체가 도달하지 못하는 문제가 있었고, 환경별 redirect URI를 명확히 분리해 해결했습니다.

```ts
// useSocialLoginCallback.ts
onSuccess: (data) => {
  const { accessToken, status } = data.data;
  login(accessToken);
  // 신규 유저는 온보딩, 기존 유저는 홈으로 분기
  navigate(status === 'ONBOARDING' ? '/onboarding' : '/', { replace: true });
}
```

**삽질 — 비밀번호 재설정 딥링크 이중 차단**

`/password-reset?token=...` 딥링크로 직접 접근했을 때 **스플래시 로직이 `/`로 강제 이동**시키고 **인증 체크가 `/login`으로 강제 이동**시키는 이중 차단이 발생했습니다. 단순히 경로 하나를 추가하는 문제가 아니라 기존 구조 자체의 한계였습니다.

`DefaultLayout`에서 스플래시·인증·리다이렉트를 한 번에 처리하던 구조는 조건문이 누적될수록 역추적이 어렵고, `AUTH_PAGES` 배열에 문자열로 경로를 하드코딩하던 방식은 타입 안전성도 없었습니다.

React Router의 `handle` 메타데이터와 `useMatches`를 조합해 각 라우트 정의에 `skipSplash`와 `skipSessionGate` 플래그를 선언적으로 붙이고, 중첩 라우트의 부모·자식 모두를 OR 조건으로 병합하는 `reduce` 패턴으로 해결했습니다.

```ts
// RouteHandle 인터페이스 — 라우트별 가드 정책을 타입 안전하게 선언
interface RouteHandle {
  skipSplash?: boolean;
  skipSessionGate?: boolean;
}

// useRouteGuard — useMatches로 현재 매칭된 모든 라우트의 handle을 병합
// [핵심] OR로 병합: 부모·자식 중 어느 한 라우트에만 skipSplash=true여도 가드 해제 → 중첩 라우트 구조에서 안전
const flags = matches.reduce<RouteHandle>((acc, m) => ({
  skipSplash: acc.skipSplash || (m.handle as RouteHandle)?.skipSplash,
  skipSessionGate: acc.skipSessionGate || (m.handle as RouteHandle)?.skipSessionGate,
}), {});
```

`useRouteGuard`로 리다이렉트 판단 로직을 한 곳에 모아 `DefaultLayout`은 정책 결과만 받아 렌더링에 집중하도록 역할을 분리했습니다.

**API 에러 핸들링 중복 제거**

`postPasswordResetLink`, `postPasswordReset`, `getPasswordResetToken` 세 함수 모두에 거의 동일한 try-catch 블록과 에러 메시지 추출 로직이 반복되고 있었습니다. API 레이어에서 비즈니스 로직인 에러 메시지 변환까지 처리하는 레이어 책임 분리 위반이기도 했습니다.

`extractErrorMessage` · `isSuccessResponse` · `isErrorResponse`, 세 가지 제네릭 타입 가드 함수를 `apiErrorHandler.ts` 유틸리티로 분리해 에러 처리 로직 변경 시 한 곳만 수정하면 되는 구조를 만들었습니다.

---

### 블록 편집 페이지 — 스냅 & Undo·Redo

https://github.com/user-attachments/assets/e6809360-ba65-42ae-b535-fd7ae6d9f688

> `dnd-kit` `Zustand` `useRef Stack` `structuredClone` `queueMicrotask`

블록을 퍼즐처럼 연결하는 UX는 Travlocks의 정체성과 직결됩니다. 단순히 가까운 위치에 붙이는 것이 아니라 블록마다 `socket`(홈)과 `plug`(돌기) 방향이 있고, 서로 반대 방향끼리만 연결될 수 있습니다. 이를 위해 `snapToTail`을 직접 설계했습니다.

```ts
// snapToTail.ts — socket·plug 방향 검사 후 최근접 스냅 위치 계산
export function snapToTail({ drag, tail, threshold = 30 }): TailSnapResult {
  for (const socket of tail.connectors.filter(c => c.type === 'socket')) {
    for (const plug of drag.connectors.filter(c => c.type === 'plug')) {
      // 엣지 방향이 정반대인 쌍만 유효
      if (!areOppositeDirections(socketDir, plugDir)) continue;

      const d = dist(socketCenter, plugCenter);
      if (d > threshold) continue; // 30px 이내일 때만 스냅

      // [핵심] drag 블록의 절대 위치 보정: plug 중심이 socket 중심과 정확히 겹치도록
      // drag.x + (socket 캔버스 좌표 - plug 캔버스 좌표) = plug가 socket에 완벽히 정렬되는 drag 좌표
      best = { x: drag.x + (socketCenter.x - plugCenter.x), ... };
    }
  }
  return best ?? { canSnap: false, ... };
}
```

**삽질 — dnd-kit + zoom 좌표 계산 오류**

zoom 인/아웃 후 블록을 재배치했을 때 마우스 위치와 블록 움직임이 일치하지 않는 문제가 발생했습니다. 콘솔에서 `startX: 230` 상황에서 `candidate.x: -1720`처럼 완전히 잘못된 음수 좌표가 나오는 현상을 직접 확인했습니다.

`e.delta`는 드래그 시작점부터의 마우스 이동 거리인데, 스크롤 변화가 delta에 포함될 수 있고 `transform: scale()` 컨테이너 내부에서 드래그 시 추가 계산 오류가 발생하기 때문이었습니다. `clampInBoard`에서 `x = startX + deltaX / zoom` 계산 시 delta 값이 `-1950`처럼 비정상적으로 커져 `230 + (-1950) = -1720` 같은 음수 좌표가 발생했습니다.

delta 기반 계산을 버리고 `e.active.rect.current.translated` 기반의 실제 화면 위치를 사용하는 `calcBoardPointFromActiveRect`로 좌표 계산 로직을 **완전히 교체**해 해결했습니다. 클로저 트랩 문제(`useCallback`에 캡처된 `puzzleBlocks`가 최신 상태가 아닌 문제)는 `puzzleBlocksRef`와 `zoomRef`를 `useRef`로 선언하고 `useEffect`로 항상 최신 상태를 동기화해 해결했습니다.

**DAY별 블록 상태 완전 분리 — Zustand 전역화**

상태가 `BlockPage → BlockEditor → BlockEditorContent → hooks`로 내려가며 props drilling과 상태/로직 결합이 커질 우려가 있었고, DAY 전환 시 편집 내용이 섞이는 문제가 발생할 수 있었습니다.

Zustand store로 편집 상태를 전역화해 DAY/블록 상태를 컴포넌트 트리에서 props drilling 없이 접근할 수 있게 만들었습니다. `blocksByDay`를 `Record<number, Block[]>`로 유지한 이유는 업데이트·재사용·직렬화 코드가 단순하고 서버 연동 시 변환 비용이 적기 때문입니다. `useBlockDrag`는 상태를 직접 소유하지 않고 드래그 결과만 커밋하도록 책임을 분리해 **props drilling 최소화, DAY별 상태 완전 분리, 드래그 훅 책임 분리** 세 가지 효과를 동시에 얻었습니다.

**Undo·Redo 설계**

QA에서 "블록을 잘못 쌓았을 때 되돌릴 방법이 없다"는 피드백이 나왔습니다. 블록 상태는 Zustand 스토어에 있어 React 상태로 히스토리를 관리하기 까다로웠고, `useRef` 기반의 스택 구조로 해결했습니다.

```ts
// useBlockHistory.ts — useRef 스택으로 렌더링 없이 히스토리 관리
const MAX_HISTORY = 50; // 메모리 초과 방지

const push = (snapshot: Block[]) => {
  pastRef.current.push(snapshot);
  if (pastRef.current.length > MAX_HISTORY) pastRef.current.shift();
  futureRef.current = []; // 새 액션 발생 시 redo 스택 초기화
  syncFlags(); // canUndo / canRedo 상태만 setState로 업데이트
};
```

히스토리 스택 자체는 `useRef`로 관리해 push/pop이 리렌더를 유발하지 않고, UI에 필요한 `canUndo` · `canRedo` 플래그만 `useState`로 노출했습니다. (`ref`는 값이 바뀌어도 리렌더를 유발하지 않기 때문에 버튼 활성화 상태 반영에는 반드시 `useState`여야 합니다.)

undo/redo 시 서버 동기화가 충돌하지 않도록 `isSyncPausedRef`로 동기화를 일시 억제하고, `queueMicrotask`로 플래그를 복원합니다. `setTimeout(fn, 0)`은 다음 태스크 큐로 밀려 불필요한 지연이 생기는 반면, `queueMicrotask`는 현재 콜스택이 비워진 직후 실행되어 상태 반영과 플래그 복원 사이의 간격을 최소화합니다. 단, React 배치 업데이트 타이밍과 충돌 가능성을 인지하고 `isSyncPausedRef`를 `useRef`로 관리해 렌더링과 분리했습니다. `structuredClone`으로 스냅샷 간 참조를 완전히 분리해 히스토리 오염을 방지했습니다.

> **Cmd+Z / Cmd+Y / Cmd+Shift+Z** 단축키도 동시에 지원합니다.

---

### AI 동선 최적화

https://github.com/user-attachments/assets/ff5506e3-2d55-478d-a63c-d103898c48c8

> `getAllSnapPositionsToTail` `Geometry` `Randomization`

여행 동선을 수동으로 조율하는 것이 번거롭다는 문제를 해결하기 위해 AI 자동 정렬 기능을 도입했습니다.

**삽질 — orderNo만 바꾸면 화면에 아무 변화가 없다**

AI API 응답의 `orderNo`만 업데이트하고 실제 캔버스 좌표는 그대로여서 사용자가 정렬 결과를 시각적으로 전혀 확인할 수 없었습니다. AI가 블록 순서를 최적화해준다는 핵심 가치 제안이 무색해지는 상황이었습니다.

단순 세로 배치를 첫 번째로 시도했다가 plug/socket 구조에서 블록들이 맞닿지 않고 기존 드래그 스냅과 달라 시각적으로 단조롭다는 것을 깨달았습니다. 기존 드래그용 `snapToTail`은 threshold 기반이라 거리가 멀면 null을 반환해 자동 배치에 부적합했습니다.

`getAllSnapPositionsToTail`을 새로 작성해 threshold 없이 **모든 socket-plug 쌍의 후보 위치를 반환**하도록 만들었습니다. plug 중심이 socket 중심과 정확히 겹치도록 드래그 위치를 계산하는 공식은 다음과 같습니다.

```ts
// plug 중심이 socket 중심과 정확히 겹치도록 블록 위치 계산
candidate = {
  x: tail.x + socketLocal.x - plugLocal.x,
  y: tail.y + socketLocal.y - plugLocal.y,
};
```

후보 위치가 여러 개일 때 `Math.random()`으로 선택합니다. 결정론적 배치(예: 최소 y 좌표 우선)도 검토했으나, 블록 형태가 비대칭이어서 항상 같은 레이아웃이 나오면 시각적으로 단조롭다는 판단 하에 현재 방식을 채택했습니다. 단, 사용자가 배치를 확정하면 해당 좌표가 저장되므로 재정렬 전까지는 일관성이 유지됩니다. 스냅 불가 시에도 `prevBlock.x + prevBlock.w + 20`으로 폴백 배치하는 안전망을 마련했습니다.

AI API가 반환한 `orderNo` 기준으로 블록 순서를 재배치하고, `getAllSnapPositionsToTail`을 활용해 재배치된 블록들을 퍼즐처럼 이어붙인 위치로 자동 재계산합니다. 정렬 결과가 편집 캔버스에 즉시 반영되어 사용자는 버튼 하나로 최적화된 동선을 확인할 수 있습니다.

</div>
