# 과제 진행 현황

- 주제: 2026시즌 두산·LG·한화·키움 유니폼 구단 분류. 홈·원정·특별 유니폼 포함.
- Step 0~3, 5~12 완료. 원본 600장은 보존했고 사용자 판단으로 231장을 이동, 369장을 유지했다.
- Step 4 미완료: data/new_images의 각 구단 폴더에 사용자·지인이 직접 촬영한 사진 최소 5장과 출처 설명이 필요하다.
- Step 13 부분 완료: clean 모델 학습 완료. 학습 295장 / 시험 74장, 최종 정확도 100.0% / 89.2%. 정제 전 run은 99.8% / 85.0%. 시험 집합이 다르므로 이 차이만으로 정제 효과를 결론 내리지 않는다. 같은 새 사진으로 run/clean 비교는 대기 중이다.
- Step 14 구현·테스트 및 다운로드 시험 오답 자료 완료. 오답 8장, results/clean_worst.png 및 clean_analysis_output.txt. 전체 테스트 42개 통과.
- Step 15 웹 모델 변환 및 ONNX/Python 일치 확인 완료. 최종 check.py는 새 사진 확보 후 다시 실행해야 한다. 현재 예비 출력은 results/check_pending_photos.txt에 있으며 미완료 항목은 새 사진 없음이다.
- Step 16 로컬 데모의 초록색 배지와 사진 업로드 예측 확인 완료.
- Step 17 GitHub Pages 공개 완료: https://jaehakie.github.io/DataAI-assignment1/ . 공개 주소에서 데스크톱·모바일 화면 크기의 자체 검사 및 업로드 예측을 확인했다. 사용자의 실제 휴대폰 모바일 데이터 확인은 남았다.
- Step 18 미착수: 사용자가 가설과 변경할 사진·방법을 직접 정한다. 에이전트가 가설이나 실험을 대신 제안하지 않는다.
- Step 19 Long report 초안 작성 중. 확인된 결과·그림·원문 출력을 반영했고 새 사진 평가, Problem 7, 사용자 소감, 이름·학번 등은 fillin으로 남았다. Overleaf XeLaTeX 컴파일은 아직 하지 않았다. mas1004.sty는 변경하지 않았다.
- Step 20 Short report는 사용자가 AI 작성·교정 없이 작성한다. short_report 파일은 수정하지 않았다.

## 다음 실행 순서

1. 새 사진의 구단별 출처를 기록하고 JPEG/PNG로 정리한다.
2. uv run python src/clean.py overlap 의 출력을 results/overlap.txt로 저장하고, 사용자가 실제 중복 여부를 판단한다.
3. uv run python src/check.py --compare run clean 의 전체 출력을 results/compare.txt로 저장한다.
4. uv run python src/check.py 의 최종 전체 출력을 results/check.txt로 저장한다.
5. 사용자가 새 사진의 오답을 해석하고 Problem 7 실험을 결정한다. 각 요청을 원문 그대로 보존한다.
6. Long report를 완성하고 Overleaf에서 컴파일·확인·ZIP 다운로드한다. 제출 공지는 Long report ZIP, Short report PDF, links.txt를 요구한다.

기존 run/scratch/frozen/low_lr/clean 모델과 결과를 덮어쓰지 않는다. 사진이나 결과를 임의로 정제·수정하지 않는다.