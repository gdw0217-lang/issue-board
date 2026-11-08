# issue-board

유튜브 채널 세 곳(이거핫하다는데? · Star Moments · 윤현빈 블로그)의 지표 보드 + 분석 탭. 정적 페이지(index.html) + data/*.json. privacy.html 은 업로드 앱(issue-upload, 구글 클라우드 OAuth)의 개인정보처리방침.

- 데이터는 PC 예약 작업 `shorts_dash`(3시간마다)가 `apps/shorts/work/dash_build.py` 로 만들고 이 저장소에 올린다. 채널 탭 목록은 data/index.json(dash_build.py 가 씀).
- 분석 탭: `apps/shorts/work/board_analysis.py` 가 `apps/shorts/docs/분석_MMDD*.md` 중 최신 문서를 data/analysis.json 에 담고, index.html 이 마크다운(제목·표·목록·굵게·수평선)을 자체 렌더러로 그린다. 분석 탭은 index.json 에 없고 index.html 에 고정으로 붙어 있다.
- 조회·좋아요·댓글: PC가 1시간마다 찍는 기록(view_snaps.jsonl). 유지율·유입·검색어·시청자: 유튜브 분석 API, 하루 1번.
- 검색엔진 차단(robots.txt, noindex).
- 11/5 Star Moments 폐쇄 뒤 channel-board 에서 옮겨 옴. 11/6 복구되어 11/8 Star Moments 탭(ent) 복귀.
