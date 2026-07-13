# Codyssey — AI 기반 브랜드 광고 패키지 (미션 B1-2)

> **"막막했던 사람도, AI와 함께라면 누구나 원하는 것을 만들어낼 수 있다."**
> 자기주도형 AI 자동화 교육 프로그램 **Codyssey**의 10초 브랜드 티저 광고 제작 프로젝트.
> 슬로건: **Anyone Can Make It**

---

## 1. 프로젝트 개요

- **미션**: GenAI 기초 2 — 멀티모달 콘텐츠 제작 (B1-2)
- **목표**: 기획 의도 → 프롬프트 → 결과물 → 통합 편집으로 이어지는 **전체 제작 파이프라인을 스스로 설계**하고, AI 생성물을 주된 소스로 **10초 이내 브랜드 광고**를 완성한다.
- **최종 산출물 (2종)**
  1. 스토리보드(기획) 문서 — `codyssey_storyboard.pdf`
  2. 광고 영상 — `final/codyssey_ad_final.mp4` (10초 이내)

> 이 README는 스토리보드 문서의 모든 내용을 포함하며, 여기에 제작 과정·의사결정·문제 해결·자기평가를 더한 **프로젝트 전체 기록 문서**입니다.

---

## 2. 리포지토리 구조

```
B1-2/
├── final/
│   └── codyssey_ad_final.mp4          # 최종 광고 영상 (제출본)
├── source/
│   ├── video/
│   │   ├── scene1.mp4                 # 씬1 (Kling)
│   │   ├── scene2.mp4                 # 씬2 (Google Flow)
│   │   ├── scene3.mp4                 # 씬3 (Google Flow)
│   │   └── scene4.mp4                 # 씬4 (Hailuo AI)
│   ├── narration/
│   │   ├── 01_코드_앞에서_멈춰_있나요.mp3
│   │   ├── 02_AI가_아이디어를_현실로.mp3
│   │   ├── 03_누구나_만들_수_있습니다.mp3
│   │   └── 04_지금_코디세이와_시작하세요.mp3
│   ├── bgm/
│   │   └── Skyline Promise.mp3        # BGM (Suno)
│   ├── logo/
│   │   ├── codyssey_chrome_logo.jpg   # 메탈릭 크롬 로고 (Meta AI 생성)
│   │   ├── codyssey_chrome_logo.webp
│   │   ├── codyssey_logo.png          # 정식 로고
│   │   └── codyssey_logo.jpg
│   └── result/
│       ├── codyssey_ad_v1.mp4         # 편집 중간 버전
│       └── codyssey_ad_v2.mp4         # 편집 중간 버전
└── README.md
```

---

## 3. 브랜드 아이덴티티

| 항목 | 내용 |
|---|---|
| **브랜드명** | Codyssey (코디세이) |
| **타겟** | 자동화·프로그램 제작을 배우고 싶은 **성인 누구나** (비전공자 포함) |
| **톤앤매너** | 미래적 · 교육적 · 따뜻하고 희망적 |
| **USP (차별점)** | AI를 활용해 누구나 원하는 자동화·프로그램을 스스로 만드는 **자기주도형 교육 프로그램** |
| **핵심 메시지** | "누구나, AI와 함께라면 원하는 것을 만들 수 있다." |
| **슬로건** | **Anyone Can Make It** |

---

## 4. 캠페인 정의

- **광고 목적**: 인지 + 전환 — 교육 프로그램 인지도 확보 및 참여(수강) 유도
- **광고 타입**: 10초 이내 티저/홍보 숏폼
- **핵심 메시지 (1문장)**: "막막했던 사람도, AI와 함께라면 누구나 원하는 것을 만들어낼 수 있다."
- **서사 구조 (기승전결)**:
  문제 제시(혼자 막막함) → 전환(협업·AI로 해결) → 확신(누구나 가능) → 브랜드 각인(로고)

---

## 5. 제작 파이프라인

기획 의도가 최종 영상으로 구현되기까지의 흐름과, 각 단계에서 **왜 그렇게 의사결정했는지**를 정리한다.

1. **기획·스토리보드 확정** — 브랜드/캠페인 정의 후 4씬 스토리보드를 먼저 문서로 확정.
   → *이유: 영상 생성은 크레딧 소모가 크므로, 씬 구성을 미리 굳혀 재생성·낭비를 줄이기 위함.*
2. **프롬프트 설계** — 씬별 목표에 맞춰 구도·피사체·배경·조명·화질 키워드를 조합.
   → *이유: "운 좋은 결과"가 아니라 의도한 그림을 얻기 위해 프롬프트를 통제.*
3. **영상 생성** — 씬별로 서로 다른 비디오 생성 AI를 사용.
   → *이유(중요): 단일 도구 크레딧 부족 문제를 회피하기 위해 씬별로 도구를 분산(§10 참조).*
4. **오디오 제작** — 내레이션(클로바더빙 TTS) + BGM(Suno) 생성. 일부 씬은 효과음을 프롬프트로 직접 통제(§7).
   → *이유: 시각뿐 아니라 청각까지 AI로 정교하게 설계하고 톤을 통일하기 위함.*
5. **통합 편집 (CapCut)** — 컷 편집, 자막, 오디오 레벨·싱크, 로고 씬 배속으로 10초에 맞춤.
   → *이유: AI 생성물을 주된 소스로 유지하되, 편집 툴은 "통합" 용도로만 제한적으로 사용.*
6. **인코딩·산출** — 1080p / 30fps / H.264·AAC / 16:9로 최종 내보내기.

---

## 6. 씬 구성 (Scene Breakdown)

### 6.0 요약

| 구분 | 씬 1 | 씬 2 | 씬 3 | 씬 4 |
|---|---|---|---|---|
| 역할 | 기 (문제) | 승 (전환) | 전 (확신) | 결 (브랜드) |
| 길이 | 약 3.3초 | 약 2.4초 | 약 2.3초 | 약 2.0초 |
| 목표 메시지 | 혼자서는 막막한 현실 | AI·동료와 함께 해결 | 누구나 만들 수 있다는 확신 | 브랜드/슬로건 각인 |
| 내레이션 | 코드 앞에서, 멈춰 있나요? | AI가, 아이디어를 현실로. | 누구나, 만들 수 있습니다. | 지금, 코디세이와 시작하세요. |
| 비디오 도구 | Kling | Google Flow | Google Flow | Hailuo AI (+Meta AI 로고) |
| 오디오 | 효과음(내장)+내레이션 | 내레이션 | 효과음(내장)+내레이션 | 내레이션 |

> BGM(Suno · *Skyline Promise*)은 전 씬에 은은하게 공통 적용. 내레이션은 네이버 클로바더빙(TTS)으로 제작.

### 6.1 씬 1 — 막막함 (혼자 마주한 벽)

- **씬 길이**: 약 3.3초
- **목표 메시지**: 혼자서는 막막했던 현실을 한 컷으로 각인시킨다.
- **화면 구성**: 구도 = 미디엄샷, 인물 측·후면과 모니터 강조 / 피사체 = 지친 직장인 1인 / 배경 = 어두운 사무실, 반복되는 코드·데이터 화면 / 조명 = 파란빛 모니터광 / 텍스트 = 없음
- **내레이션**: "코드 앞에서, 멈춰 있나요?" *(낮고 무거운 톤)*
- **사용 도구와 목적**:
  - 비디오: **Kling** — 어둡고 시네마틱한 실내 인물 묘사와 미묘한 모션 표현에 강해서 채택
  - 오디오: 효과음(생성 내장), 내레이션(클로바더빙)
- **입력 프롬프트 (원문 · KR)**:
  > 어두운 사무실에서 모니터를 바라보는 지친 직장인, 화면에는 반복되는 데이터와 코드가 가득함, 무겁고 피곤한 분위기, 파란빛 조명, 영화적 구도, 고화질
- **출력 결과 요약**: 지치고 무거운 분위기의 도입 컷 확보 (문제 제시).
- **결과 파일**: `source/video/scene1.mp4`, `source/narration/01_코드_앞에서_멈춰_있나요.mp3`

### 6.2 씬 2 — 전환 (함께라면 풀린다)

- **씬 길이**: 약 2.4초
- **목표 메시지**: AI와 동료가 함께하면 문제가 풀린다는 전환을 보여준다.
- **화면 구성**: 구도 = 미디엄-와이드, 살짝 팬하는 핸드헬드 / 피사체 = 모니터 앞 1인 + 주변 협업자 2인 이상(혼성) / 배경 = 밝은 개방형 오피스, 창문 자연광 / 텍스트 = 없음
- **내레이션**: "AI가, 아이디어를 현실로." *(밝고 확신에 찬 톤)*
- **사용 도구와 목적**:
  - 비디오: **Google Flow** — 다인물 상호작용과 밝은 자연광 오피스 묘사에서 안정적인 결과를 줘서 채택
  - 오디오: 내레이션(클로바더빙)
- **입력 프롬프트 (원문 · EN)**:
  > A cinematic medium-wide shot of a productive team collaborating around a computer in a modern, open-plan office. One man sits in front of the screen, gesturing toward the monitor and typing. Two and more colleagues (diverse group, mixed gender) stand around him, leaning in closely, looking at the display with focused, enthusiastic expressions. They are actively discussing, laughing, and sharing ideas, pointing at elements on the screen, creating an uplifting and optimistic problem-solving atmosphere. Bright, natural daylight streams in from large windows, illuminating the office and creating soft highlights. Colorful office décor in the background (bookshelves, plants, whiteboards) is softly blurred. Natural skin tones, warm, cozy lighting, realistic film grain, captured in ultra-high definition, photorealistic, 4K resolution. Smooth handheld camera motion panning slightly to follow the interaction.
- **출력 결과 요약**: 밝고 협력적인 문제 해결 분위기의 전환 컷 확보.
- **결과 파일**: `source/video/scene2.mp4`, `source/narration/02_AI가_아이디어를_현실로.mp3`

### 6.3 씬 3 — 확신 (누구나 항해할 수 있다)

- **씬 길이**: 약 2.3초
- **목표 메시지**: "누구나 만들 수 있다"는 확신을 항해 은유로 전달한다.
- **화면 구성**: 구도 = 와이드샷, 전방 푸시인 트래킹 / 피사체 = 황금빛 바다 위를 나아가는 목선 / 배경 = 노을·일출빛 바다와 수평선 / 텍스트 = 자막 **"Anyone Can Make It"** (슬로건 노출)
- **내레이션**: "누구나, 만들 수 있습니다." *(자막과 의미를 겹쳐 이중 각인)*
- **사용 도구와 목적**:
  - 비디오: **Google Flow** — 광활한 바다·물결 질감 표현이 우수
  - 오디오: 효과음(파도·항해, 생성 내장, **프롬프트로 직접 통제** → §7), 내레이션(클로바더빙)
- **입력 프롬프트 (원문 · EN · 최종/수정 후)**:
  > A cinematic wide shot of a small wooden sailboat gracefully sailing forward through gentle golden waves on a vast, sunlit ocean that stretches infinitely to the horizon. Warm morning sunlight brilliantly reflects on the undulating water, creating a hopeful and uplifting atmosphere. The camera performs a smooth push-forward motion, tracking the boat. Bright colors, soft lens flare, highly detailed water texture, photorealistic, 4K resolution. (Audio: No music, background music removed, realistic ocean waves and sailing sound effects only, high quality SFX)
- **출력 결과 요약**: 희망적 항해 비주얼 + 깨끗한 파도·항해 효과음(음악 제거) 확보.
- **결과 파일**: `source/video/scene3.mp4`, `source/narration/03_누구나_만들_수_있습니다.mp3`

### 6.4 씬 4 — 브랜드 각인 (로고의 완성)

- **씬 길이**: 약 2.0초 (최종본에서 배속하여 10초에 맞춤)
- **목표 메시지**: 브랜드명·로고를 각인시키며 참여를 유도(CTA)한다.
- **화면 구성**: 구도 = 센터 로고샷 / 피사체 = 메탈릭 크롬 Codyssey 로고 → 원본(정식) 로고로 전환 / 배경 = 어두운 미래적 배경, 글로우 그리드 / 텍스트 = 브랜드명·로고(Codyssey) 노출
- **내레이션**: "지금, 코디세이와 시작하세요." *(로고 등장 타이밍에 CTA)*
- **사용 도구와 목적**:
  - 이미지: **Meta AI** — 크롬 로고 키비주얼 생성
  - 비디오: **Hailuo AI** — 입자→정식 로고 전환의 부드러운 모션 구현 (초기 Runway 시도 → 품질 문제로 교체, §7·§10)
  - 오디오: 내레이션(클로바더빙)
- **입력 프롬프트 (원문 · EN)**:
  > A futuristic metallic chrome "Codyssey" logo slowly transforms and lands into its final form, metallic particles dissolve and settle, glowing grid lines fade away, logo becomes clean and solid, smooth cinematic transition, dark background, slow and elegant motion, high quality
- **출력 결과 요약**: 미래적 크롬 로고에서 정식 브랜드 로고로 전환되는 마무리 컷 확보.
- **결과 파일**: `source/video/scene4.mp4`, `source/logo/codyssey_chrome_logo.jpg`, `source/logo/codyssey_logo.png`, `source/narration/04_지금_코디세이와_시작하세요.mp3`

---

## 7. 프롬프트 개선 로그

### 7.1 씬 3 — 오디오 톤 미스매치 (필수 기록)

| 구분 | 내용 |
|---|---|
| **수정 전 의도** | 노을빛 바다·항해 비주얼 확보 (비주얼 자체는 만족) |
| **문제** | 생성 결과에 **배경음악이 함께 포함**되어 나옴. 앞뒤 씬 및 전체 톤(내레이션·공통 BGM)과 붙였을 때 **오디오 톤이 충돌**하여 몰입을 해침 |
| **수정 후 변경** | 프롬프트 끝에 오디오 제어 구문 추가: `(Audio: No music, background music removed, realistic ocean waves and sailing sound effects only, high quality SFX)` |
| **결과 변화** | 배경음악 제거, 파도·항해 **효과음만 유지** → 공통 BGM(Suno)과 톤 통일 성공 |

> 별도 도구를 추가하지 않고 **프롬프트만으로 오디오를 통제**하여 멀티모달 제작의 대표적 문제인 "오디오 톤 미스매치"를 해결한 의사결정.

### 7.2 씬 4 — 로고 도구 교체 (도구 비교 사례)

| 구분 | 내용 |
|---|---|
| **수정 전** | 로고 모션 영상을 **Runway**로 생성 |
| **문제** | 로고 전환 품질이 기대에 못 미침(형태·모션 안정성 부족) |
| **수정 후 변경** | 동일 목적을 **Hailuo AI**로 재생성 |
| **결과 변화** | 입자→정식 로고 전환이 훨씬 부드럽고 브랜드 톤에 맞게 개선됨 |

---

## 8. 사용 도구 — 역할·강점·약점·선택 이유

| 구분 | 사용 도구 | 역할 | 강점 | 약점/한계 | 대체 도구 |
|---|---|---|---|---|---|
| 이미지 생성 | **Meta AI** | 크롬 로고 키비주얼 | 접근성 좋고 로고형 그래픽 빠르게 생성 | 세밀한 브랜드 typography 제어는 제한적 | Midjourney, DALL·E |
| 비디오 생성 | **Kling** | 씬1 (어두운 실내 인물) | 시네마틱·저조도 인물 묘사에 강함 | 크레딧 소모 | Runway, Pika |
| 비디오 생성 | **Google Flow** | 씬2·3 (협업/바다) | 다인물·자연광·광활한 풍경 안정적 | — | Runway, Kling |
| 비디오 생성 | **Hailuo AI** | 씬4 (로고 모션) | 부드러운 오브젝트 전환 모션 | — | Runway(초기 시도, 품질 문제) |
| 오디오 (내레이션) | **네이버 클로바더빙** | TTS 내레이션 | 자연스러운 한국어 보이스, 교육/비영리 활용 용이 | 세밀한 감정 연기 제한 | 타입캐스트, ElevenLabs |
| 오디오 (BGM) | **Suno** | 배경음악 생성 | 텍스트로 분위기 맞춤 BGM 생성 | 길이·구조 미세 제어 제한 | Udio |
| 통합 편집 | **CapCut** | 컷/자막/오디오/배속 | 무료·직관적, 오디오 레벨·싱크 편리 | (편집 툴, 생성 아님) | Premiere Pro |

> **도구 선택 원칙**: "많이 쓰기"가 아니라 씬별 목표에 가장 적합한 결과를 주는 도구를 선택했으며, 비디오는 크레딧 분산을 위해 의도적으로 여러 도구를 나눠 사용(§10).

---

## 9. 소스 통합 (해상도 · 비율 · 톤앤매너)

씬마다 다른 도구·언어(한/영 프롬프트)·스펙(대부분 4K 기준 생성)으로 나온 소스를 하나의 광고로 통합한 과정.

- **해상도/비율**: 서로 다른 도구 출력물을 CapCut에서 **1920×1080(16:9)** 기준으로 정렬·통일. 최종 인코딩도 1080p로 통일.
- **톤앤매너**: 어두움(씬1) → 밝음(씬2) → 황금빛(씬3) → 미래적(씬4)의 명암 흐름이 서사(기승전결)와 일치하도록 컷 순서 유지.
- **오디오 통일**: 공통 BGM(Suno)을 전 씬에 은은하게 깔고, **내레이션을 항상 최상위 레벨**로 배치. 씬3은 프롬프트로 음악을 제거해 BGM과 충돌을 방지. 효과음(씬1·3)은 내레이션과 겹치는 구간에서 레벨을 조정.
- **마무리 처리**: 로고 씬 배속으로 전체 길이를 10초에 맞추고, BGM 끝부분 페이드아웃.

---

## 10. 제작 중 겪은 문제 & 해결 전략

| 문제 | 상황 | 해결 전략 |
|---|---|---|
| **크레딧 부족** | 단일 영상 생성 AI로 4씬을 모두 뽑기엔 크레딧이 부족 | 씬별로 **서로 다른 비디오 AI(Kling·Google Flow·Hailuo AI)로 분산**하여 각 도구의 무료/보유 크레딧을 나눠 사용 → 제약사항의 "크레딧 부족 시 범위 조정" 전략 실천 |
| **오디오 톤 미스매치** | 씬3에 원치 않는 배경음악이 딸려나와 전체 톤과 충돌 | 프롬프트에 오디오 제어 구문 추가로 음악 제거, 효과음만 유지 (§7.1) |
| **로고 품질 미달** | 씬4 로고 모션을 Runway로 생성했으나 품질 부족 | Hailuo AI로 재생성하여 전환 모션 개선 (§7.2) |
| **영상 길이 초과** | 편집본이 11초로 10초 기준 초과 | 마지막 로고 씬을 배속하여 **정확히 10초 이내**로 맞춤 |
| **구성 밀도** | 짧은 길이에 메시지를 담아야 함 | 씬을 4개로 압축하고 각 씬에 명확한 서사 역할(기승전결) 부여 |

---

## 11. 제약사항 준수

- ✅ **모든 시각·청각 소스는 생성형 AI 결과물** (이미지·영상·내레이션·BGM 전부 AI 생성)
- ✅ 직접 촬영 영상·유료 스톡 소스 **미사용**
- ✅ 딥페이크·혐오·선정성·폭력 등 **유해 콘텐츠 없음**
- ✅ 편집 툴(CapCut)은 **컷 편집·자막·오디오 레벨·배속 등 통합 편집 용도로만** 제한 사용
- ✅ 이미지 생성 단계에서 스토리보드를 확정한 뒤 영상 변환 → **크레딧 낭비 최소화**
- ✅ 이미지/비디오/오디오 각각 **대체 도구 확보**(§8)
- ⚪ 스타일/캐릭터 일관성 기능(cref/sref, ControlNet 등): **미사용** (권장 항목, 이번 제작에서는 씬별 독립 구성이라 고정 레퍼런스 불필요)

---

## 12. 최종 영상 스펙

| 항목 | 값 |
|---|---|
| 파일명 | `final/codyssey_ad_final.mp4` |
| 길이 | 약 10초 (10초 이내) |
| 해상도 | 1920 × 1080 (1080p) |
| 프레임레이트 | 30fps |
| 비디오 코덱 | H.264 |
| 오디오 코덱 | AAC |
| 화면 비율 | 16:9 |
| 구성 요소 | AI 생성 시각(이미지·영상) + AI 생성 청각(효과음·BGM·내레이션) 모두 포함 |
| 브랜드 각인 | 마지막 구간에 로고·브랜드명·슬로건·CTA 내레이션 포함 |

---

## 13. 요구사항 충족 체크리스트

| 요구사항 | 충족 | 근거 |
|---|:--:|---|
| 브랜드 아이덴티티 정의(타겟/톤앤매너/USP) | ✅ | §3 |
| 광고 목적 + 핵심 메시지 1문장 | ✅ | §4 |
| 씬 단위 스토리보드 + 씬별 필수 필드 | ✅ | §6, 스토리보드 PDF |
| 프롬프트 수정 전/후 최소 1개 씬 기록 | ✅ | §7 (씬3, 씬4) |
| 이미지 생성 AI 1종 이상 | ✅ | Meta AI |
| 비디오 생성/변환 AI 1종 이상 | ✅ | Kling · Google Flow · Hailuo AI |
| 오디오 생성 AI 1종 이상 | ✅ | 클로바더빙 · Suno |
| 도구 선택 이유 기록 | ✅ | §6, §8 |
| 최종 영상 10초 이내 | ✅ | §12 |
| AI 시각 + 청각 요소 포함 | ✅ | §12 |
| 기승전결 또는 명확한 메시지 구조 | ✅ | §4, §6 |
| 마지막 3~5초 브랜드 인지 장치 | ✅ | 씬4 로고·슬로건·CTA |
| 대체 도구 준비 | ✅ | §8 |

---

## 14. 보너스 과제 (예정)

> 아래는 이후 진행 예정. 완료 시 결과와 과정을 이 섹션에 추가한다.

- [ ] **보너스 1 – 립싱크(Lip-sync)**: 인물 발화 장면 1개 이상 추가, 입모양·대사 싱크
- [ ] **보너스 2 – 동일 스토리보드, 다른 도구로 재제작**: 이미지/비디오 파트를 다른 도구로 씬 1~2개 재제작
- [ ] **보너스 3 – 플랫폼별 화면 비율 버전**: 16:9 외 9:16(숏폼) / 1:1(피드) 버전 제작

---

*Codyssey · AI 기반 브랜드 광고 패키지 · 미션 B1-2 · Anyone Can Make It*
