# home-planner (배포본)

수내역 통근권 주택 매수 판단을 위해 만든 계산기의 **빌드 산출물**이다.
소스는 별도 비공개 저장소에 있고, 이 저장소는 GitHub Pages 서빙만 한다.

## 성격

**참고용이다. 은행 심사 결과가 아니다.** 실제 한도는 신용점수, 은행 내부기준,
DSR 산정 방식에 따라 달라지고 세액은 개별 사실관계에 따라 달라진다.
최종 확인은 은행과 세무 상담이 필요하다. 화면 하단에도 같은 문구가 있다.

입력한 수치는 **브라우저 안에만 저장된다**(localStorage). 서버로 전송되지 않고
이 저장소에도 포함되지 않는다.

## 데이터 출처와 라이선스

| 데이터 | 출처 | 라이선스 |
|---|---|---|
| `data/market/candidate-coords.json` 의 좌표 | OpenStreetMap | **ODbL 1.0**. 출처표시와 share-alike 적용 |
| `data/market/price-history.json`, `candidates.json` 의 실거래 | 국토교통부 실거래가 공개시스템 | 공공누리 출처표시 |
| `data/market/bundang-special-districts.json`, `redevelopment-districts.json` | 토지이음(국토교통부) 고시정보, 성남시·용인시 고시 원문 | 공공누리 출처표시 |
| `data/policy/2026-09-08.json` | 법령·행정규칙·주택도시기금 고시 등. 항목별 근거는 파일 안 `verifiability` 필드 참조 | 공공누리 출처표시 |

OpenStreetMap 기여자에게 귀속된다. (c) OpenStreetMap contributors, ODbL 1.0.
OSM 에서 파생한 데이터베이스를 다시 배포할 때는 같은 ODbL 로 공개해야 한다.

## 값의 확실성 표기

모든 수치에 확실성이 함께 붙어 있다. 화면에서 `미측정`, `추산`, `미확정` 배지와
`값을 매길 수 없다` 같은 문구를 그대로 읽으면 된다. **없는 것과 0 인 것을
구분해서 표시한다** - 분담금이 `0원`이 아니라 `미측정`이면 확인이 안 된 것이다.
