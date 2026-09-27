# 두리콜렉션 27SS 원가 — #fabric-unit 재게이트 2 (산식 칸 글자 크기) 2026-09-28

- 오더: 두리콜렉션 봇 · `Z:\HDD1\MARU\dashboard\두리콜렉션\27SS\원가\index.html` · read-only(대시보드 수정·Z 배포·브라우저 없음)
- 주장: 46행만 변경(#fabric-unit note font-size 0.875rem → 14px) · 해시 7047B419…7679
- 선행: reports/2026-09-28-duri-27ss-cost-fabric-unit-regate.md (조건부: 0.875rem = 12.25px)
- 박스: `/workspace/uploads/duri-cost-regate2-0928/` (index.html + visibility.css 사본) · 스크립트 `_verify/duri-cost-merge-0928/{sim_regate2.js,font_regate2.js}`

## 판결
`승인`

## 주장 | 실측 | 차

| 항목 | 주장 | 실측 | 차 |
|------|------|------|-----|
| 해시 | 7047B419…7679 | Z index.html **2026-09-28 08:48:25 KST** · 46,091B · SHA256 `7047B4197FFDDC2F…9F077679` · 박스 사본 같음 | 0 |
| 변경 범위 | 46행만 | 08:45판(`58A68987…`) 대비 diff **1줄**: `#fabric-unit td.note, #fabric-unit-note { font-size:0.875rem; }` → `{ font-size:14px; }` | 0 |
| 글자 크기(캐스케이드) | ≥14px | visibility.css(Z `DF65068D…`, html/body 14px)를 넣고 jsdom 계산: html 14px · td.note 4개 **14px** · p#fabric-unit-note **14px**. `.note`(0.85rem, 0-1-0)보다 `#fabric-unit td.note`(1-1-1)·`#fabric-unit-note`(1-0-0)가 우선. 두 파일의 `!important`는 `.wrap{padding}` 1개뿐(글자 무관) · 해당 요소 style 속성 0 · visibility.css에 td/p/.note 글자 규칙 없음 | 0 |
| 다른 4개 파일 | 변경 없음 | styles_cost.json `4D5B403E…` · po_profit.json `AA4BBBF8…` · assumptions.json `C17397C1…` · report.md `E4BE4EA6…` = 08:44 사본과 같음(mtime 08:44:31~32 KST) | 0 |
| 불변식 | 이전 재게이트 그대로 | 마스터 셀 차 **0/192** · KPI 같음 · 원가합 **130,042,100** · 수익 61,457,900 · 32.09% · qty 24,300 · wavg **5,351.53** | 0 |
| 병합·필터 | 유지 | ALL rowspan **40** · 버튼 5개 14번 전환 오류 0 | 0 |
| 링크 | 바뀐 참조 없음 | href/src 변경 0 → Test-Path 생략(직전 13/13 True 유지) | 0 |

## 참고
- 배지(`.badge` 0.72rem)는 기존 규칙 그대로 — 표 본문 글자가 아닌 라벨로 이전 게이트들과 같은 기준 적용.
- 선행 재게이트의 비차단 관찰(KORA 통화 출처 문구·styles_cost `generated` 날짜·공임 detail fx 1358.4·sample_qa.md 미검)과 질문(케어라벨 본사 공급 근거 문서·9/15 요척 반영 시점)은 그대로 남음.

## 오답 처리
- 승인 → 두리콜렉션 승인 행(키 `시인성=참고대시보드급·전칸공통`) 추가 · `close_open.py`로 열린 두리콜렉션 시인성 행 닫기

## 재현1줄
Get-FileHash 7047B419…·4파일 해시 같음 · diff 46행 1줄 · `node font_regate2.js` td.note×4·note p = 14px · `node sim_regate2.js` 셀차0·rowspan40·필터14회 오류0 · Σ130,042,100 · wavg 5,351.53
