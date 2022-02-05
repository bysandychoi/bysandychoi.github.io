---
layout: default
title: Sonarqube 설명
parent: GitHub
nav_order: 6
---

## Issue
 sw 품질을 개선할 수있는 항목

### Type  

|--- |---|
|Bug|코드를 손상시키고 즉시 수정이 필요한 issue|
|   |프로그램 실행 시 예상되는 동작을 하지 않거나 작동하지 않는 위험성이 있는issue|
|Vulnerabilities|해커들에게 약점이 되어 공격 할수 있는 이슈, 보안 취약점|
|CodeSmell      |심각한 issue는 아니지만, 유지보수를 하기 어렵게 만드는 코드|
|               |ex)중복된 코드, 거대한 코드, naming convention|

### Severity
 적용된 규칙이 얼마나 심각하고 중요한지 수준 별 정의 
 
|--- |---|
|Blocker|프로그램의 동작에 영향을 줄 가능성이 높은 issue|
|       |코드를 즉시 수정 필요|
|       |ex)memory leak, 닫히지 않은 JDBC 연결|
|Critical|프로그램의 동작에 영향을 줄 가능성이 낮은 issue|
|        |코드를 즉시 검토 필요|
|        |ex)|
|Major  |개발자 생산성에 영향을 크게 줄 수 있는 품질 issue|
|       |시간을 두고 검토 필요 |
|       |ex) Nullpointer Exception |
|Minor  |개발자의 생산성에 잠재적인 영향을 미칠 수 있는 품질 issue|
|       |ex) 너무 긴 코드, 3개 미만의 switch 문 등|
|Info   |품질상의 결함이 아닌 인지를 위한 알림|

### Resolution
 해결 상태.

|--- |---|
|Unresolved |분석 결과 해결되지 않은 issue|

#### Closed 상태의 issue

|--- |---|
|Fixed |분석 결과 해당 isseu가 수정 완료 됨|
|      |SonarQube가 자동으로 설정|
|      |ex) 분석 파일 제외 된 code 내의 issue 는 fixed 됨|
|Removed|분석 결과 해당 issue를 발생시킨 코딩 규칙 혹은 소스 콛드가 존재하지 않은 경우| 
|       |ex) 파일이름 변경, 파일 위치 이동, 파일 삭제시 해당 파일은 존재하지 않는 것으로 판단|

#### Resolved 해결 상태의 isse

|---|---|
|Won't Fix |issue 이지만 수정하지 않음|
|          |사용자가 직접 설정|
|False Positive|오검출|
|              |사용자가 직접 설정|

### Status
 issue 가 생성된 후에는 다음 중 하나의 상태 

|---|---|
|Open     |Sonarqube가 새로운 issue 라고 결정한 상태|
|Confirmed|해당 issue가 유요한 issue라고 사용자가 직접 설정한 상태|
|Resolved |다음 분석시 해당 issue가 완료될 것이라고 사용자가 직접 설정한 상태|
|Reopend  |Resolved 상태의 issue가 실제로 수정되지 않았을 경우|
|         |Sonarqube가 자동으로 설정한 상태|
|Closed   |Soanrqube가 자동으로 생성한 issue 중, 분석시 해당 issue 가 완료된 상태|


## Rule

### Tag 
 rule 에 대한 categorizing

|---|---|
|cert            |CERT 표준 규칙과 관련|
|cwe             |Common Weakness Enumeration|
|pitfall         |당장은 문제되지 않지만, 후에 문제가 될 수 있는 issue|
|convention      |coding convention, ex) fomatting, naming.|
|clumsy          |extra steps are used to accomplish somthing that could be done more clearly and consisely|   
|suspicious      |완벽히 bug는 아니지만 의심스러운 issue|
|confusing       |유지 보수시 헤깔릴 우려가 있는 issue|
|branin-overload |너무 복잡한 코드|
|unused          |사용하지 않은 코드|
|bad-practice    |의도한 바와 비슷한 방식으로 동작하나, 일반적으로 해당 코드의 설계가 잘못된 방식으로 인식 됨|
|owasp           |OWASP top 10 보안 기준 관련|
|sans-top 25     |SANS top 25 보안 기준 관련|