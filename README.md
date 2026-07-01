# CBDC 안전 실험실 — 이중언어(한/영) 플랫폼 / Bilingual Platform

## 한국어

### 무엇이 들어 있나요
- **`cbdc_platform_bilingual.html`** — 메인 프로그램. 더블클릭하면 브라우저에서 바로 열립니다(설치 불필요).
- **`manuals/`** — 쉬운 사용 설명서 (한국어 · 영어)
- **`results/`** — 논문 실험 결과 CSV 파일들

### 새로 추가/개선된 점
1. **오른쪽 위 KOR / ENG 버튼** — 클릭하면 모든 화면 글자가 한국어 ↔ 영어로 전환됩니다.
2. **논문 일치성 검증 패널** (대시보드 바로 아래) — 논문(JFS R18)의 검증된 기준값과 이 도구의
   설계 비교 결과를 나란히 보여주고, 설계 순위가 일치하면 초록색 ✓ 배지를 표시합니다.
   - 논문 기준: No CBDC 0.04 / 무제한 0.41 / 고정한도 0.32 / **동적상한+계층 0.14**
   - θ₂ = 0.2217 (논문 OLS, n=79)
3. 이 도구의 빠른 계산은 *탐색용*이며, 정확한 크기는 검증된 파이썬 엔진
   `python-mt19937-v6.0`에서 나옵니다. **논문이 보증하는 것은 "설계 순위"** 이며, 이 도구가
   그 순위를 재현합니다.

### 결과 파일 (results/)
| 파일 | 내용 |
|---|---|
| `paper_table4_design_comparison.csv` | 4개 설계 실패확률 (논문 Table 4) |
| `paper_table2_ols.csv` | OLS 회귀 (θ₂=0.2217 등, Table 2) |
| `paper_table2b_ols_with_digital.csv` | 디지털 변수 추가 회귀 (Table 2b) |
| `paper_table9_five_country.csv` | 5개국 결과 (Table 9) |
| `experiment_results_engine_vs_paper.csv` | 엔진 계산값 vs 논문값 대조 |

> 참고: 영어로 전환해도 일부 **그래프 내부 글자**(차트에 그림으로 그려진 텍스트)는 한국어로 남을
> 수 있습니다. 화면의 일반 글자(메뉴·라벨·표·리포트)는 모두 전환됩니다.

---

## English

### What's inside
- **`cbdc_platform_bilingual.html`** — the main program. Double-click to open in a browser (no install).
- **`manuals/`** — easy user guides (Korean · English)
- **`results/`** — paper experiment-result CSV files

### What's new / improved
1. **KOR / ENG buttons (top-right)** — click to switch every on-screen text Korean ↔ English.
2. **Paper Consistency Check panel** (just below the dashboard) — shows the paper's (JFS R18)
   validated reference values side-by-side with this tool's design comparison, and displays a
   green ✓ badge when the design ranking matches.
   - Paper: No CBDC 0.04 / Unconstrained 0.41 / Fixed 0.32 / **Dynamic Cap + Tiered 0.14**
   - θ₂ = 0.2217 (paper OLS, n=79)
3. This tool's fast calculation is for *exploration*; exact magnitudes come from the validated
   Python engine `python-mt19937-v6.0`. **What the paper guarantees is the design *ranking*,**
   which this tool reproduces.

### Result files (results/)
| File | Content |
|---|---|
| `paper_table4_design_comparison.csv` | Failure probability of 4 designs (paper Table 4) |
| `paper_table2_ols.csv` | OLS regression (θ₂=0.2217, Table 2) |
| `paper_table2b_ols_with_digital.csv` | Regression adding digital adoption (Table 2b) |
| `paper_table9_five_country.csv` | Five-country results (Table 9) |
| `experiment_results_engine_vs_paper.csv` | Engine values vs paper values crosswalk |

> Note: when switching to English, some **text drawn inside charts** (rendered as an image)
> may stay Korean. All normal on-screen text (menus, labels, tables, reports) is translated.
