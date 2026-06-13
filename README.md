# 연속 PC 셋업 추천기 (Continuous Tetris Perfect Clear Recommender)

보이는 미노를 입력하면 회차별로 퍼클(Perfect Clear) 확률이 높은 셋업을 추천하고,
각 셋업에 맞는 솔버/연습 링크를 자동으로 제공하는 단일 HTML 도구입니다.
설치 없이 브라우저만으로 동작하므로 PC방·공공장소에서 바로 쓸 수 있습니다.

## 사용법
1. `index.html`을 브라우저로 열기 (또는 GitHub Pages 주소 접속)
2. 회차별 입력:
   - **1회차**: 보이는 미노(현재+넥스트)를 도착 순서대로 입력 (홀드 활용 가능)
   - **2회차**: 잔여 4미노 + 다음 가방 도착순 → 세이브 순 추천
   - **3·5회차**: 잔여(extra/쌍) 선택 → 셋업 열람
   - **4회차**: 없는 쌍(No-XY) 선택 → PC% 순 추천
   - **6·7회차**: 잔여 상태 선택 → 셋업/솔버
3. 추천 카드의 **🔧 솔버/연습** 버튼으로 해당 셋업을 풀거나 연습
4. **🔄 연속 흐름** 내비(`다음 N회차 ▶`)로 다음 회차로 진행 → 반복
   - 7회차 다음은 주기성에 의해 1회차로 순환

## 데이터 원칙
- 출처(pcinfokorea)의 검증된 셋업만 수록 (818개, 1~7회차)
- 회차 간 이월은 플레이어 선택이므로 고정 매핑을 넣지 않고, 셋업별 솔버로 정확히 처리
- 2→3회차만 세이브 데이터로 자동 연결, 나머지는 관찰 입력 + 솔버

## 출처
- 셋업 DB: [pcinfokorea](https://sites.google.com/view/pcinfokorea)
- 솔버: [tetra-tools PC solver](https://wirelyre.github.io/tetra-tools/pc-solver.html),
  [downstack-practice](https://himitsuconfidential.github.io/downstack-practice/)
