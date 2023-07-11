# programmers-airflow-ETL


## 로그 데이터 Airflow 파이프라인  구축

[PPT](https://drive.google.com/file/d/1Vf_5PjsqAyTjv4_fS7gazsn3CjKi06c3/view?usp=sharing)  <br>
[보고서](https://drive.google.com/file/d/1dFx-y0XNwNcr3PT8atcIusFzSGJCd2GC/view?usp=sharing)

<aside>
📊 로그 데이터 Airflow 파이프라인  구축 <br>
[로그데이터 분석 대시보드 구축 프로젝트](https://github.com/hyedall/programmers-log-dashboarding/blob/main/README.md)
  의 파이프라인을 Airflow로 구축하였습니다.

</aside>

### 기술 스택

Airflow,  Docker, Postgres

### 상세 내용

로그 데이터 생성, 적재하는 과정을 Airflow로 자동화함.  
- 하루 간격으로 스케줄링
  - execution_date ~ next_execution_date 까지 시간 별로 데이터 개수가 차이나게 생성 후 로그 데이터 time 걸럼에 넣어줌
  - 날짜 별로도 랜덤 값을 줘서 날짜 별 데이터 양이 다르게 생성
  - Airflow backfill을 활용하여 데이터 생성
- 증분으로 적재되게 만듬



### 주요성과

![이미지](https://drive.google.com/file/d/1dnr1L610o0MYbsxzW2ttWDurRBBdP_Lm/view?usp=sharing)


### 기여한 부분

에어플로우 dag 작성

### 배운 점

- 저번 프로젝트 때 시간별로 같은 분포를 가지는 부분이 아쉬워서 airflow로 데이터를 생성하면서 시간별로 데이터 양이 다르게 생성되게끔 수정해봄  
- airflow를 활용해보면서 full refresh와 증분에 대한 부분도 고민해보고,  execution_date에 대해 자세하게 활용해볼 수 있었음







