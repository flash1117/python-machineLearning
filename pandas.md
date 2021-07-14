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

- 데이터 전처리 , 스케일링 이런건 pandas로 사용하다가 머신러닝 API에 사용하려고 ndarray로 변환시키는 경우가 있다.

변화시킬 때는 `dataFrame-Name.values` 를 통해 변환시킬 수 있다.

`inplace = false` 라면 원본 데이터는 변환되지 않은 채 drop 된 객체만 반환된다.

drop 할 때 `axis = 0` 부분을 없애면 **행이 사라지는 것**

- DataFrame 및 Series에 `reset_index()` 메서드를 수행하면 새롭게 인덱스를 연속 숫자 형으로 할당하여 기존 인덱스는 index 라는 새로운 컬럼 명으로 추가된다.

- ix
위치 , 명칭 인덱스 둘다 제공하는 것 처럼 보이지만 index column 을 추가할때 명칭을 정수로 사용하고 index를 또 따로 사용하는 경우 오류를 발생할 수 있다.
- loc
명칭 기반 인덱스를 제공

- iloc
위치 기반 인덱스를 제공
    - dataframe의 객체를 넣으면 오류를 반환하게 된다. 정수를 넣어야함.

- Series 는 1차원 객체

- 논리 식을 변수에 할당해서 boolean 연산자를 사용할 수 도 있다.

- sum , max, min ,count 등의 함수는 DataFrame/Series에서 집합(Aggregation)연산을 수행.

- DataFrame은 Group by 연산을 위해 groupby() 메서드 제공

- dataframe의 groupby 된 객체의 index는 groupby 할 때 사용한 컬럼의 이름이 나온다.

- 각 컬럼별로 다른 값을 구하고 싶을 때 dictionary를 사용하여 다양한 aggregation 함수를 적용할 수 있다.

- isna : dataframe 의 isna의 메소드는 컬럼값들이 NaN인지 True/False를 반환한다. ( NaN 이면 True )

- fillna : missing data를 인자로 주어진 값으로 대체한다

- 람다식이 속도는 조금 더 느리지만 식이 너무 복잡하면 사용한다.

ex)

`titanic_df['Name_len'] = titanic_df['Name'].apply(lamda x : len(x))` 

`titanic_df['Child_Adult'] = titanic_df['Age'].apply(lamda x : 'Child' if x<=15 else 'Adult' )`

- 람다식에 함수도 적용 가능하다. 함수에 반드시 return 값 필요.