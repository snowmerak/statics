# **통합 디자인 시스템: TechFlow (Dark & Light)**

---
---

# **디자인 시스템: TechFlow Dark**

## **1. 디자인 철학 (Design Philosophy)**

- **정보 중심 (Information-Centric):** 사용자가 기술 문서의 핵심 내용에 집중할 수 있도록 불필요한 시각적 요소를 최소화하고, 콘텐츠의 가독성을 최우선으로 고려한다.
- **명확한 상호작용 (Clear Interaction):** 모든 인터랙티브 요소는 사용자가 그 기능을 직관적으로 예측할 수 있도록 명확한 시각적 단서(색상, 크기 변화 등)를 제공한다.
- **현대적 기술미 (Modern & Techy):** 개발자 대상의 콘텐츠에 어울리는 현대적이고 세련된 다크 모드 인터페이스를 통해 전문성과 신뢰감을 전달한다.

## **2. 핵심 원칙 (Core Principles)**

1.  **다크 모드 우선 (Dark Mode First):** 모든 컴포넌트는 다크 모드를 기본으로 설계하여 장시간 사용에도 눈의 피로를 줄인다.
2.  **강조색의 전략적 사용 (Strategic Use of Accent Color):** 주요 액션(CTA), 활성화 상태, 중요한 정보에만 강조색을 사용하여 사용자의 시선을 효과적으로 유도한다.
3.  **계층적 정보 구조 (Hierarchical Information):** 타이포그래피의 크기, 굵기, 색상 차이를 통해 정보의 중요도와 위계를 명확하게 구분한다.
4.  **일관된 여백과 간격 (Consistent Spacing):** 8px 기반의 그리드 시스템(Tailwind CSS의 기본 단위 활용)을 사용하여 시각적 안정감과 질서를 부여한다.

## **3. 색상 시스템 (Color System) - Dark**

| 역할 (Role)             | 설명                                   | 색상 (Tailwind/Hex)                           |
| :---------------------- | :------------------------------------- | :-------------------------------------------- |
| **배경 (Background)** | 페이지의 기본 배경색                   | `bg-slate-900` (#0f172a)                      |
| **표면 (Surface)** | 카드, 모달 등 콘텐츠가 올라가는 표면   | `bg-slate-800` (#1e293b)                      |
| **테두리 (Border)** | 컴포넌트 구분 및 경계선                | `border-slate-700` (#334155)                  |
| **기본 텍스트 (Primary Text)** | 제목 등 주요 텍스트                    | `text-white` / `text-slate-100`               |
| **본문 텍스트 (Body Text)** | 설명 등 일반 텍스트                    | `text-slate-300` / `text-slate-400`           |
| **강조색 (Primary Accent)** | CTA, 활성 링크, 아이콘 등              | `text-cyan-400` / `bg-cyan-400` (#22d3ee)     |
| **강조색 (Hover)** | 강조색 요소에 마우스 오버 시           | `text-cyan-300` / `bg-cyan-300` (#67e8f9)     |
| **그라데이션 텍스트** | Hero 영역 등 특별한 강조               | `from-indigo-300 to-cyan-400`                 |

## **4. 타이포그래피 (Typography) - Dark**

- **기본 글꼴:** Noto Sans KR
- **스케일:**
    - **Hero Title (H1):** `text-4xl` ~ `text-6xl`, `font-black`, `tracking-tighter`
    - **Section Title (H2):** `text-3xl` ~ `text-4xl`, `font-bold`
    - **Component Title (H3):** `text-xl` ~ `text-2xl`, `font-bold`
    - **Body (본문):** `text-base` (16px), `font-normal`, `text-slate-300`
    - **Caption (설명):** `text-sm`, `text-slate-400`
    - **Code (코드/명령어):** `font-mono`

## **5. 레이아웃 및 간격 (Layout & Spacing) - Dark**

- **컨테이너:** `container mx-auto`를 사용하여 콘텐츠를 중앙에 배치하고, `px-4 sm:px-6 lg:px-8`로 반응형 좌우 여백을 설정한다.
- **섹션 간격:** 각 주요 섹션은 `py-16` ~ `py-20`의 상하 여백을 가진다.
- **그리드 간격:** 컴포넌트 그리드에는 `gap-8`을 기본으로 사용한다.
- **내부 여백:** 카드 등 컴포넌트의 내부 여백은 `p-6` 또는 `p-8`을 사용한다.

## **6. 컴포넌트 라이브러리 (Component Library) - Dark**

#### **Button (버튼)**
- **설명:** 사용자의 주요 행동을 유도하는 요소.
- **스타일 (Primary CTA):** `bg-cyan-400 text-slate-900 font-bold py-3 px-8 rounded-full`
- **상태:**
    - **Hover:** `bg-cyan-300`
    - **Transition:** `transition-colors`
- **사용 예시:** "바로 시작하기" 버튼

#### **Card (카드)**
- **설명:** 관련 정보를 그룹화하여 보여주는 모듈형 컨테이너.
- **스타일:** `bg-slate-800 rounded-lg border border-slate-700 p-6`
- **상태:**
    - **Hover:** `transform: translateY(-5px)` 또는 `scale(1.02)`, `border-color: var(--accent-color)` (선택적)
    - **Transition:** `transition-all duration-300`
- **사용 예시:** "문제점", "핵심 철학" 섹션의 각 항목

#### **Tab (탭)**
- **설명:** 연관된 콘텐츠를 여러 뷰로 나누어 보여줄 때 사용.
- **스타일 (기본):** `text-slate-400 border-b-2 border-transparent py-2 px-4 font-semibold`
- **상태:**
    - **Hover:** `text-white`
    - **Active:** `text-cyan-400 border-cyan-400`
    - **Transition:** `transition-colors`
- **사용 예시:** "솔루션" 섹션의 기능 구분

#### **Code Block (코드 블록)**
- **설명:** 코드나 터미널 명령어를 보여주기 위한 서식.
- **스타일:** `<pre>` 태그 사용. `bg-slate-900 p-4 rounded-lg text-slate-300 overflow-x-auto`
- **강조:** 명령어 프롬프트 등 특정 부분은 `text-cyan-300` 사용 가능.

#### **Interactive Diagram (인터랙티브 다이어그램)**
- **설명:** 복잡한 구조나 워크플로우를 시각적으로 표현하는 요소. HTML과 CSS로 구현한다.
- **스타일 (레이어/노드):** `bg-slate-700 p-4 rounded-lg`
- **스타일 (연결선):** `border` 또는 `::before`, `::after` 가상 요소를 활용. `border-color: var(--border-color)` (여기서 `--border-color`는 `border-slate-700`에 해당)
- **상태:**
    - **Hover/Active:** `bg-slate-600`, `border-cyan-400`
    - **Transition:** `transition-all`
- **사용 예시:** 아키텍처 레이어, Git 브랜치 트리, K3d 워크플로우

## **7. 인터랙션 및 애니메이션 (Interaction & Animation) - Dark**

- **기본 전환:** `transition-all`, `transition-colors`, `duration-300`을 기본으로 사용하여 부드러운 상태 변화를 제공한다.
- **호버 효과 (Hover Effect):** 카드, 버튼 등 인터랙티브 요소에는 미세한 크기 변화 (`hover:scale-1.02`, `hover:-translate-y-1`)나 그림자 효과를 주어 피드백을 제공한다.
- **스크롤 애니메이션:** `scroll-behavior: smooth`를 사용하여 페이지 내부 링크 이동을 부드럽게 처리한다.

## **8. 프롬프트 활용 가이드 (Guide for Prompt Usage) - Dark**

> 다음은 "TechFlow Dark" 디자인 시스템을 기반으로 새로운 웹 페이지 생성을 요청할 때 사용할 수 있는 프롬프트 템플릿입니다.
>
> ---
>
> **[역할]**
> 당신은 "TechFlow Dark" 디자인 시스템에 매우 능숙한 전문 프론트엔드 개발자입니다.
>
> **[과업]**
> 아래에 제공된 [마크다운 문서 제목] 문서를 기반으로, "TechFlow Dark" 디자인 시스템의 원칙과 컴포넌트를 사용하여 완전한 단일 페이지 인터랙티브 웹 애플리케이션(HTML)을 생성해 주세요.
>
> **[핵심 요구사항]**
>
> 1.  **디자인 시스템 준수:**
>     - **색상:** 배경(slate-900), 표면(slate-800), 텍스트(slate-300), 강조(cyan-400) 등 "TechFlow Dark"의 색상 팔레트를 정확히 사용해 주세요.
>     - **타이포그래피:** Noto Sans KR 글꼴과 정의된 타이포그래피 스케일(Hero, H2, Body 등)을 준수해 주세요.
>     - **레이아웃:** 8px 기반의 간격 시스템과 반응형 컨테이너를 적용해 주세요.
>
> 2.  **컴포넌트 활용:**
>     - 문서의 각 섹션에 가장 적합한 컴포넌트(카드, 탭, 코드 블록 등)를 디자인 시스템에서 선택하여 적용해 주세요.
>     - 복잡한 프로세스나 계층 구조는 텍스트로 나열하는 대신, HTML/CSS 기반의 **인터랙티브 다이어그램**으로 시각화해 주세요.
>
> 3.  **인터랙션:**
>     - 모든 인터랙티브 요소에는 `hover` 및 `active` 상태에 대한 시각적 피드백이 있어야 합니다.
>     - 상태 변화는 부드러운 전환 효과(`transition`)를 포함해야 합니다.
>
> 4.  **기술 제약:**
>     - **SVG, 이미지 파일, 외부 라이브러리(Chart.js 제외) 사용을 금지합니다.** 모든 시각적 요소는 Tailwind CSS와 순수 HTML/CSS로 구현해야 합니다.
>     - 최종 결과물은 단일 HTML 파일이어야 합니다.
>
> **[제공될 문서]**
> ```markdown
> [여기에 변환할 마크다운 콘텐츠를 붙여넣기]
> ```

---
---

# **디자인 시스템: TechFlow Light**

## **1. 디자인 철학 (Design Philosophy)**

- **정보 중심 (Information-Centric):** 사용자가 기술 문서의 핵심 내용에 집중할 수 있도록 불필요한 시각적 요소를 최소화하고, 콘텐츠의 가독성을 최우선으로 고려한다.
- **명확한 상호작용 (Clear Interaction):** 모든 인터랙티브 요소는 사용자가 그 기능을 직관적으로 예측할 수 있도록 명확한 시각적 단서(색상, 크기 변화 등)를 제공한다.
- **현대적 청량감 (Modern & Clean):** 개발자 대상의 콘텐츠에 어울리는 현대적이고 깔끔한 라이트 모드 인터페이스를 통해 전문성과 명확성을 전달한다.

## **2. 핵심 원칙 (Core Principles)**

1.  **라이트 모드 우선 (Light Mode First):** 모든 컴포넌트는 라이트 모드를 기본으로 설계하여 밝고 쾌적한 사용 환경을 제공한다.
2.  **강조색의 전략적 사용 (Strategic Use of Accent Color):** 주요 액션(CTA), 활성화 상태, 중요한 정보에만 명확한 강조색을 사용하여 사용자의 시선을 효과적으로 유도한다.
3.  **계층적 정보 구조 (Hierarchical Information):** 타이포그래피의 크기, 굵기, 색상 차이를 통해 정보의 중요도와 위계를 명확하게 구분한다.
4.  **일관된 여백과 간격 (Consistent Spacing):** 8px 기반의 그리드 시스템(Tailwind CSS의 기본 단위 활용)을 사용하여 시각적 안정감과 질서를 부여한다.

## **3. 색상 시스템 (Color System) - Light**

| 역할 (Role)             | 설명                                   | 색상 (Tailwind/Hex)                               |
| :---------------------- | :------------------------------------- | :------------------------------------------------ |
| **배경 (Background)** | 페이지의 기본 배경색                   | `bg-slate-50` (#f8fafc) 또는 `bg-gray-100` (#f3f4f6) |
| **표면 (Surface)** | 카드, 모달 등 콘텐츠가 올라가는 표면   | `bg-white` (#ffffff)                              |
| **테두리 (Border)** | 컴포넌트 구분 및 경계선                | `border-gray-300` (#d1d5db)                       |
| **기본 텍스트 (Primary Text)** | 제목 등 주요 텍스트                    | `text-slate-900` (#0f172a)                        |
| **본문 텍스트 (Body Text)** | 설명 등 일반 텍스트                    | `text-slate-700` (#334155)                        |
| **강조색 (Primary Accent)** | CTA, 활성 링크, 아이콘 등              | `text-blue-600` (#2563eb) / `bg-blue-600`         |
| **강조색 (Hover)** | 강조색 요소에 마우스 오버 시           | `text-blue-500` (#3b82f6) / `bg-blue-500`         |
| **그라데이션 텍스트** | Hero 영역 등 특별한 강조               | `from-sky-500 to-blue-600`                        |

## **4. 타이포그래피 (Typography) - Light**

- **기본 글꼴:** Noto Sans KR
- **스케일:**
    - **Hero Title (H1):** `text-4xl` ~ `text-6xl`, `font-black`, `tracking-tighter`
    - **Section Title (H2):** `text-3xl` ~ `text-4xl`, `font-bold`
    - **Component Title (H3):** `text-xl` ~ `text-2xl`, `font-bold`
    - **Body (본문):** `text-base` (16px), `font-normal`, `text-slate-700`
    - **Caption (설명):** `text-sm`, `text-slate-500`
    - **Code (코드/명령어):** `font-mono`

## **5. 레이아웃 및 간격 (Layout & Spacing) - Light**

- **컨테이너:** `container mx-auto`를 사용하여 콘텐츠를 중앙에 배치하고, `px-4 sm:px-6 lg:px-8`로 반응형 좌우 여백을 설정한다.
- **섹션 간격:** 각 주요 섹션은 `py-16` ~ `py-20`의 상하 여백을 가진다.
- **그리드 간격:** 컴포넌트 그리드에는 `gap-8`을 기본으로 사용한다.
- **내부 여백:** 카드 등 컴포넌트의 내부 여백은 `p-6` 또는 `p-8`을 사용한다.

## **6. 컴포넌트 라이브러리 (Component Library) - Light**

#### **Button (버튼)**
- **설명:** 사용자의 주요 행동을 유도하는 요소.
- **스타일 (Primary CTA):** `bg-blue-600 text-white font-bold py-3 px-8 rounded-full`
- **상태:**
    - **Hover:** `bg-blue-500`
    - **Transition:** `transition-colors`
- **사용 예시:** "바로 시작하기" 버튼

#### **Card (카드)**
- **설명:** 관련 정보를 그룹화하여 보여주는 모듈형 컨테이너.
- **스타일:** `bg-white rounded-lg border border-gray-200 shadow-sm p-6` (그림자 효과는 선택적)
- **상태:**
    - **Hover:** `transform: translateY(-5px)` 또는 `scale(1.02)`, `border-color: var(--accent-color)` (선택적), `shadow-md`
    - **Transition:** `transition-all duration-300`
- **사용 예시:** "문제점", "핵심 철학" 섹션의 각 항목

#### **Tab (탭)**
- **설명:** 연관된 콘텐츠를 여러 뷰로 나누어 보여줄 때 사용.
- **스타일 (기본):** `text-slate-600 border-b-2 border-transparent py-2 px-4 font-semibold`
- **상태:**
    - **Hover:** `text-slate-900`
    - **Active:** `text-blue-600 border-blue-600`
    - **Transition:** `transition-colors`
- **사용 예시:** "솔루션" 섹션의 기능 구분

#### **Code Block (코드 블록)**
- **설명:** 코드나 터미널 명령어를 보여주기 위한 서식.
- **스타일:** `<pre>` 태그 사용. `bg-slate-100 p-4 rounded-lg text-slate-800 overflow-x-auto border border-slate-200`
- **강조:** 명령어 프롬프트 등 특정 부분은 `text-blue-700` 사용 가능.

#### **Interactive Diagram (인터랙티브 다이어그램)**
- **설명:** 복잡한 구조나 워크플로우를 시각적으로 표현하는 요소. HTML과 CSS로 구현한다.
- **스타일 (레이어/노드):** `bg-gray-50 p-4 rounded-lg border border-gray-200`
- **스타일 (연결선):** `border` 또는 `::before`, `::after` 가상 요소를 활용. `border-color: var(--border-color)` (여기서 `--border-color`는 `border-gray-300`에 해당)
- **상태:**
    - **Hover/Active:** `bg-blue-50`, `border-blue-500`
    - **Transition:** `transition-all`
- **사용 예시:** 아키텍처 레이어, Git 브랜치 트리, K3d 워크플로우

## **7. 인터랙션 및 애니메이션 (Interaction & Animation) - Light**

- **기본 전환:** `transition-all`, `transition-colors`, `duration-300`을 기본으로 사용하여 부드러운 상태 변화를 제공한다.
- **호버 효과 (Hover Effect):** 카드, 버튼 등 인터랙티브 요소에는 미세한 크기 변화 (`hover:scale-1.02`, `hover:-translate-y-1`)나 그림자 효과를 주어 피드백을 제공한다.
- **스크롤 애니메이션:** `scroll-behavior: smooth`를 사용하여 페이지 내부 링크 이동을 부드럽게 처리한다.

## **8. 프롬프트 활용 가이드 (Guide for Prompt Usage) - Light**

> 다음은 "TechFlow Light" 디자인 시스템을 기반으로 새로운 웹 페이지 생성을 요청할 때 사용할 수 있는 프롬프트 템플릿입니다.
>
> ---
>
> **[역할]**
> 당신은 "TechFlow Light" 디자인 시스템에 매우 능숙한 전문 프론트엔드 개발자입니다.
>
> **[과업]**
> 아래에 제공된 [마크다운 문서 제목] 문서를 기반으로, "TechFlow Light" 디자인 시스템의 원칙과 컴포넌트를 사용하여 완전한 단일 페이지 인터랙티브 웹 애플리케이션(HTML)을 생성해 주세요.
>
> **[핵심 요구사항]**
>
> 1.  **디자인 시스템 준수:**
>     - **색상:** 배경(slate-50 또는 gray-100), 표면(white), 텍스트(slate-700), 강조(blue-600) 등 "TechFlow Light"의 색상 팔레트를 정확히 사용해 주세요.
>     - **타이포그래피:** Noto Sans KR 글꼴과 정의된 타이포그래피 스케일(Hero, H2, Body 등)을 준수해 주세요.
>     - **레이아웃:** 8px 기반의 간격 시스템과 반응형 컨테이너를 적용해 주세요.
>
> 2.  **컴포넌트 활용:**
>     - 문서의 각 섹션에 가장 적합한 컴포넌트(카드, 탭, 코드 블록 등)를 디자인 시스템에서 선택하여 적용해 주세요.
>     - 복잡한 프로세스나 계층 구조는 텍스트로 나열하는 대신, HTML/CSS 기반의 **인터랙티브 다이어그램**으로 시각화해 주세요.
>
> 3.  **인터랙션:**
>     - 모든 인터랙티브 요소에는 `hover` 및 `active` 상태에 대한 시각적 피드백이 있어야 합니다.
>     - 상태 변화는 부드러운 전환 효과(`transition`)를 포함해야 합니다.
>
> 4.  **기술 제약:**
>     - **SVG, 이미지 파일, 외부 라이브러리(Chart.js 제외) 사용을 금지합니다.** 모든 시각적 요소는 Tailwind CSS와 순수 HTML/CSS로 구현해야 합니다.
>     - 최종 결과물은 단일 HTML 파일이어야 합니다.
>
> **[제공될 문서]**
> ```markdown
> [여기에 변환할 마크다운 콘텐츠를 붙여넣기]
> ```