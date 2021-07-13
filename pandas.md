## Pandas

> 2차원 데이터를 가장 처리하기 쉬운 라이브러리

DataFrame - Column X Rows 2차원 데이터 셋

Series - 1개의 Column값으로만 구성된 1차원 데이터 셋

read_csv()

> read_csv 함수를 이용하여 csv 파일을 편리하게 DataFrame으로 로딩합니다. read_csv() 의 sep 인자를 콤마가 아닌 다른 분리자로 변경하여 다른 유형의 파일도 로드가 가능합니다.

- Pandas의 Index 객체는 RDBMS의 PK (Primary Key)와 유사하게 DataFrame, Series의 레코드를 고유하게 식별하는 객체입니다.

- DataFrame, Series 에서 Index 객체만 추출하려면 DataFrame.index 또는 Series.index 속성을 통해 가능하다.

- Series 객체는 Index 객체를 포함하지만 Series 객체에 연산 함수를 적용할 때 Index는 연산에서 제외된다.

- DataFrame 및 Series에 `reset_index()` method를 수행하면 새롭게 인덱스를 연속 숫자 형으로 할당하며 기존 인덱스는 index 라는 새로운 컬럼 명으로 추가된다.