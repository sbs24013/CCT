여름에 하면 좋을 것

- 가상머신?
- 리눅스 커맨드 라인?
- 빅데이터에 필요 (ex. 스파크?)
  - 라이브로 여러 소스의 방대한 데이터를 수용
- 과학 저널 쓰는 연습

필수 사항

- RAM 8기가 필요

논문 관련

- Scientific Research > Domain
- 2학기에 proposal을 제출하고, 토픽을 선택

CA1 구조

- 인트로
- 각 모듈별 섹션
- 결론

# Scaling & Dealing with Categorical Data

EDA (Exploratory Data Analysis)

카테고리 데이터는 데이터는 머신러닝에 그래도 사용할 수 없다.

머신러닝에서 사용할 수 있는 포맷으로 변경해야 한다. (ex. 넘버)

example

```
Pets: Cat, Dog, Dog, Dog, Cat, Mouse, Mouse, Cat
Ordimal/Label: 1, 2, 2, 1, 2, 3, 3, 1
```

클래스 마다 숫자를 할당 하는 것

- 문제점: 클래스 마다 상관 관계가 있는가?
- 컴퓨터는 숫자를 통해 클래스 간의 컨텍스트를 알 수 없다
- ex. Dog - Cat = Cat

Ref. [OneHotEncoder](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html)

클래스 마다 특성을 부여하여 속하는 클래스는 True, 다른 클래스는 False를 주는 것

Example.

```
      Pets_Cat  Pets_Dog  Pets_Mouse
Cat   1         0         0
Cat   1         0         0
Dog   0         1         0
Cat   1         0         0
Mouse 0         0         1
```

문제점

1. 특성이 많으면 디멘션이 너무 많아 진다
2. 대부분의 데이터가 0 이다

? sparse array
