# Oracle vs MySQL    

### 0. 왜 이 주제를 골랐나요?   
-> 저는 Oracle 만 주구장창 다뤄왔지만 입사하게된 회사에서는 MySQL을 사용하고 있기 때문에 두 RDBMS가 어떤 차이점이 있는지 학습해보고자 이 주제로 선정하였습니다.

### 1. 전반적인 차이
<table>
  <tr>
    <th></th>
    <th>Oracle</th>
    <th>MySQL</th>
  </tr>
  <tr>
    <th>요약</th>
    <th>높은 성농과 살벌한 비용</th>
    <th>오픈소스 & 상업용 라이센소 모두 제공</th>
  </tr>
  <tr>
    <th>소유권 & 라이선스</th>
    <th>Oracle 사에서 개발 및 소유중</th>
    <th>MySQL AB에서 개발되었으나 현재는 Oracle에서 소유중</th>
  </tr>
  <tr>
    <th>성능</th>
    <th>대용량 데이터처리와 복잡한 쿼리에 최적화 / 고성능을 위한 다양한 최적화 도구와 기법 제공</th>
    <th>소규모 or 중간규모의 데이터베이스 애플리케이션에 적합</th>
  </tr>
  <tr>
    <th>저장엔진</th>
    <th>자체적으로 통합된 하나의 저장 엔진 사용</th>
    <th>여러 저장 엔진을 지원 / 가장 많이 사용되는 엔진은 InnoDB와 MyISAM</th>
  </tr>
  <tr>
    <th>트랜잭션 관리</th>
    <th>뛰어난 트랜잭션 처리 / 다중 버전 동시성 제어(MVCC),  복구관리, 고급 롤백 및 롤포워드 기능 포함</th>
    <th>InnoDB 스토리지 엔진을 사용한 ACID 트랜잭션 지원 / Oracle에 비해 일부 고급 트랜잭션 관리 기능 부족할 수 있음</th>
  </tr>
  <tr>
    <th>보안</th>
    <th>매우 강력한 보안 기능을 제공 / 데이터 암호화, 고급 인증 및 권한 관리, 감사 기능 등을 포함</th>
    <th>기본적인 보안 기능을 제공하지만, Oracle만큼 강력하지 않을 수 있음 / 데이터 암호화, 사용자 권한 관리 등의 기본적인 기능을 제공</th>
  </tr>
  <tr>
    <th>사용 사</th>
    <th>대규모 엔터프라이즈 애플리케이션, 금융 서비스, 대규모 데이터 분석, 복잡한 트랜잭션 처리 등이 필요한 경우에 주로 사용</th>
    <th>웹 애플리케이션, 중소규모 데이터베이스, 스타트업 및 개발 환경에 주로 사용</th>
  </tr>
</table>



### 2.구문 차이 
<table>
  <tr>
    <th></th>
    <th>Oracle</th>
    <th>MySQL</th>
  </tr>
  <tr>
    <th>NULL 체크 (NULL 치환)</th>
    <th>NVL</th>
    <th>IFNULL</th>
  </tr>
  <tr>
    <th>현재 날짜 & 시간</th>
    <th>SYSDATE</th>
    <th>DATE()</th>
  </tr>
  <tr>
    <th>날짜 포맷 (날짜형 -> 문자형)</th>
    <th>TO_CHAR()</th>
    <th>DATE_FORMAT()</th>
  </tr>
  <tr>
    <th>요일 인식(숫자)</th>
    <th>일요일 : 1 ~~~ 토요일 : 7</th>
    <th>일요일 : 0 ~~~ 토요일 : 6</th>
  </tr>
  <tr>
    <th>문자 연결</th>
    <th> ' || '</th>
    <th>CONCAT()</th>
  </tr>
  <tr>
    <th>형변환</th>
    <th>TO_CHAR(), TO_NUMBER()</th>
    <th>CAST</th>
  </tr>
  <tr>
    <th>형변환 예시</th>
    <th>SELECT TO_CHAR(1234) FROM DUAL</th>
    <th>SELECT CAST(1234 AS CHAR) FROM DUAL</th>
  </tr>
  <tr>
    <th>대소문자 구분</th>
    <th>구분 안함</th>
    <th>구분함(설정변경 가능)</th>
  </tr>
  <tr>
    <th>상위 N개 / 페이징</th>
    <th>ROWNUM</th>
    <th>LIMIT</th>
  </tr>
  <tr>
    <th>페이징 예시</th>
    <th>SELECT ... WHERE ROWNUM <= 10</th>
    <th>SELECT ... FROM ### LIMIT 10</th>
  </tr>
</table>

