

# 기초실험1: 저항, 전압, 전류 측정

## 실험목표
1. 칼라코드를 이용하여 저항 값을 읽는 법을 익힌다. 멀티미터를 이용하여 저항 값을 측정해본다.
2. 브레드보드의 내부구조를 파악하고 활용해본다.
3. 전원공급기를 이용하여 전압을 생성하고 회로에 공급한 뒤 전압을 측정해본다.
4. 회로의 특정 지점을 통해 흐르는 전류를 측정해본다.

### 사용장비,주요부품 및 구현 회로도

이번 실험에 사용할 주요 부품과 이를 브레드보드에 구현한 주요 회로도는 다음과 같다. 실험 시작 전 혹은 담당교수의 지시사항이 있을 때 실험 준비실로 이동하여 필요한 수량만큼 해당 부품을 수령한다.

![00_BOM](./images/00.jpg 'BOM')

### 예비보고서

1. 본 실험 자료를 읽고 실험 목차, 방법, 예상 결과에 대해 요약해본다. 
2. 추가로 담당교수의 지시사항에 대해 리포트로 작성한다.

예비보고서를 작성할 때는 다음주에 실시할 실험 목표, 내용, 절차, 예상결과 순으로 요약한다. 실험에 필요한 이론적인 배경지식이 부족한 상태이므로 이해하기 어려운 부분이 있더라도 본인이 판단할 수 있는 범위내에서 최대한 상세히 작성하도록 한다.



-------------------------
## 멀티미터 테스트

아래 그림은 멀티미터의 short test 모습을 보여준다. 멀티미터의 기본 동작을 확인하고 케이블이 끊어지지 않았는지 확인하거나 회로의 특정지점이 short되어 있는지 확인하는데 주로 사용한다. 

![01_fuse_test](./images/01.jpg '멀티미터 Short Test')

과전류 등으로 인해 멀티미터 내부 보호용 퓨즈가 손상될 수 있으므로 멀티미터가 정상동작하지 않을 경우 뒷면 커버를 벗긴 뒤 퓨즈가 끊어졌는지 눈으로 확인하여 끊어졌다면 다른 퓨즈로 교체하도록 한다. (멀티미터에 따라서 퓨즈가 끊어져도 short test에서 정상으로 확인되므로 육안으로 확인해야 한다.)

1. 멀티미터 전면부 다이얼을 조정하여 그림과 같이 스피커 모양의 위치로 다이얼을 조절하여 Short Test모드를 설정한다.
2. 멀티미터 케이블의 단자를 멀티미터 본체 하단 포트에 그림과 같이 연결한다. 색깔에 주의한다.
3. 멀티미터 케이블의 반대쪽 클립을 서로 연결한다.
4. 소리가 나지 않을 경우 케이블 불량 혹은 퓨즈 손상을 의심하여 교체하도록 한다.



## 저항 칼라 코드 읽기

아래 그림은 저항에 표기된 칼라코드에 따른 저항값을 읽는 방법을 보여준다.

![02_저항값읽기](./images/02.jpg '저항 칼라코드 읽기')

칼라코드의 띠가 한 쪽으로 몰려 있기 때문에 시작점과 오차값의 위치를 구분할 수 있다. 하지만 저항 종류에 따라서 한쪽으로 치우쳐 있지 않는 경우가 있는데 이때는 보통 은색, 금색 띠가 오차 값을 표시하는 띠라고 생각하면 된다.

저항의 크기를 칼라코드로 계산하지 않고 멀티미터를 이용하여 실제 값을 측정할 수 있지만 저항에 표기된 칼라 띠를 이용하여 직접 저항 값을 계산할 수 있도록 연습해두는 것이 좋다. 4색 띠로 표현된 저항의 경우 왼쪽 두개는 Digit를 표시하며 3번째는 지수 곱, 그리고 마지막이 저항 값의 오차를 나타낸다. 해당 색깔에 따라 계산에 사용되는 수치는 그림의 표를 참고한다.

예를 들어 오른쪽 위의 그림과 같은 저항의 경우, 첫 번째 갈색은 1을 의미하고, 두 번째는 검은색이므로 0을 의미한다. 두개를 합쳐서 10으로 표현된다. 3번째는 빨간색이므로 지수 값으로 10의2승 혹은 100을 의미하고 이 값을 digit와 곱하므로 최종적으로 1000=1k를 나타낸다. 마지막 띠의 색깔이 금색이므로 5% 오차를 가지는 저항을 의미한다. 



## 저항값을 멀티미터로 직접 측정해보기

![03_저항측정](./images/03.jpg '멀티미터를 이용한 저항 측정')

위의 그림은 멀티미터의 저항측정모드를 이용하여 저항의 실제 값을 측정하는 모습을 보여준다.

멀티미터를 이용하여 다음의 순서를 따라하면서 저항 값을 직접 측정해보자. 아직 멀티미터 사용이 익숙지 않을 경우 해당 절차에 따라 조심스럽게 따라 해보도록 하자.

1. 멀티미터 전면부 다이얼을 조정하여 저항측정모드로 설정한다. 이때 측정 저항값의 범위를 고려하여 측정 해상도(범위)를 적절히 설정한다. (그림은 최대 4KΩ 측정모드로 설정함)
2. 멀티미터 케이블의 연결 잭을 본체에 결합한다. 이때 색깔에 주의한다.
3. 멀티미터 케이블의 클립 사이에 저항을 연결한다.
4. 멀티미터 LCD 창에 현재 측정된 저항값이 표시된다. 1번에서 다이얼을 조절할 때 측정 대상의 범위를 고려하여 적절히 조정한다. 



## 브레드보드 활용

브레드보드의 내부 배선의 구조를 파악해보자.

![04_브레드보드_연결테스트](./images/04x.jpg '브레드보드 하판 연결성 테스트')

브레드보드 상판에는 점퍼선을 삽입할 수 있는 홀만 존재하고 내부에 배선이 어떻게 되어 있는지 명확하게 표시되어 있지 않다. 따라서 멀티미터의 short test모드를 이용하여 서로 연결된 두 지점을 파악해보도록 하자. 그전에 먼저 브레드보드 내부 연결 구조를 알아보자.

1. 멀티미터 전면부 다이얼을 조정하여 스피커 모양의 Short Test모드로 이동시킨다.
2. 멀티미터 케이블의 연결 잭을 본체에 그림과 같이 결합한다. 이때 색깔에 주의한다.
3. 멀티미터 케이블의 반대쪽 클립에 적절한 크기의 점퍼선을 결합한다. (브레드보드의 특정 홀에 삽입위해)
4. 그림과 같은 브레드보드를 준비한다. 표면에는 여러 개의 홀로 구성되어 있지만 내부에는 서로 연결된 패턴이 존재한다. 
5. 그림에 표시된 빨간색 박스 내부의 홀끼리는 내부적으로 연결되어 있음을 숙지하고 회로를 구성한다. 마찬가지로 파란색 박스 내부의 홀끼리는 내부적으로 연결되어 있다.
6. 브레드보드의 가운데 영역은 예를 들어 그림의 초록색 박스안의 홀끼리 가로방향 패턴으로만 서로 연결되어 있다. 

멀티미터의 프로브 끝에 악어클립으로 씌우져 있는 캡을 벗기면 팁이 나온다. 이 팁을 직접 브레드보드 홀에 강제로 삽입할 경우 브레드보드 접촉부가 망가져서 접촉 불량을 일으킨다. 따라서 가능하면 측정지점에 점퍼선을 연결한 뒤 악어클립으로 안전하게 결합하도록 한다.

간혹 브레드보드 접점 불량이 발생하므로 혹시 정상적인 동작을 하지 않을 경우 브레드보드의 다른 영역을 사용해보도록 한다. 점퍼선이 브레드보드의 홀에 정확하게 결착되지 않은 경우가 많아서 회로 오동작 시 조교에게 질문하기 전 먼저 브레드보드에 모든 점퍼선이 정확하게 결착되었는지 다시 한 번 확인해보도록 한다.

브레드보드 내부 배선이 short된 두 지점에 저항을 연결하게 되면 연결한 저항 크기와 상관없이 0옴이 되므로 주의한다. 특히 이 지점에 대해 전류를 측정하게 되면 과전류가 흘러서 멀티미터 퓨즈가 끊어질 수 있음에 주의하자.



### 브레드보드 내부배선 연결구조 파악

아래 그림은 브레드보드의 내부에 서로 연결된 두 지점을 확인하기 위해 멀티미터의 short test를 이용하는 과정을 보여준다. 내부 배선이 서로 연결되었다면 저항값은 0에 가까운 작은 값으로 측정되며 비프음이 날 것이다.

![05_브레드보드_연결테스트_short](./images/05x.jpg '브레드보드 내부에 서로 연결된 부분 확인')

멀티미터의 Short Test모드를 활용하여 브레드보드 내부 배선 연결 구조를 파악해본다.

1. 멀티미터 전면부 다이얼을 조정하여 스피커 모양의 Short Test모드로 설정.
2. 멀티미터 LCD창에 현재 측정된 저항값이 표시된다.
3. 멀티미터 케이블 끝 프로브 클립에 연결한 점퍼선을 브레드보드의 적절한 두곳에 연결하여 소리가 나는 지점을 확인하고 내부에 서로 연결되어 있는 여러 위치를 실험적으로 파악한다. 
4. 그림에서 표시한 측정 위치는 브레드보드 내부에서 서로 연결되어 있으므로 저항이 0이 되며 비프음과 함께 멀티미터 화면에도 작은 저항값이 표시된다.



![06_브레드보드_연결테스트_open1](./images/06x.jpg '브레드보드 내부에 서로 끊어진 부분 확인')

위의 그림처럼 브레드보드에서 끊어진 두 지점의 저항을 측정해보자.

1. 멀티미터 전면 부 다이얼을 조정하여 스피커 모양의 Short Test모드로 이동시킨다.
2. 멀티미터 LCD창에 현재 측정된 저항 값이 표시된다.
3. 멀티미터 케이블 클립에 연결한 점퍼 선을 브레드보드의 적절한 두 곳에 연결하여 소리가 나지 않는 두 지점이 서로 끊어져 있음을 파악한다. 
4. 예상한대로 그림에 표시된 브레드보드의 두 지점은 서로 끊어져 있으므로 소리가 나지 않으며 큰 저항 값이 측정된다.

위의 그림에 표시된 영역 간에는 서로 연결되어 있지 않음을 숙지한다.



![07_브레드보드_연결테스트_open2](./images/07x.jpg '브레드보드 내부에 서로 끊어진 부분 확인')

위의 그림에 표시된 두 지점 사이의 저항값을 측정해보자. 만약 브레드보드 내부 배선이 끊어져 있다면 큰 저항값이 측정되며 비프음이 들리지 않을 것이다.

1. 멀티미터 전면부 다이얼을 조정하여 스피커 모양의 Short Test모드로 이동시킨다.
2. 멀티미터 LCD창에 현재 측정된 저항값이 표시된다.
3. 멀티미터 케이블 끝의 악어 클립에 연결한 점퍼선을 브레드보드의 두 지점에 연결하여 저항값을 측정함으로써 두 지점이 서로 끊어져 있음을 파악한다. 
4. 예상한대로 그림에 표시된 브레드보드의 두 지점은 서로 끊어져 있으므로 소리가 나지 않으며 큰 저항값이 측정된다.



![08_브레드보드_연결테스트_short_vertical](./images/08x.jpg '브레드보드 내부에 서로 연결된 부분 확인')

------

이제 브레드보드의 양 가장자리쪽 내부 배선 구조를 파악해보자. 위의 그림처럼 세로로 같은 줄 위 아래로 저항크기를 측정해보자. 작은 저항값이 측정될 경우 두 지점은 서로 연결되어 있음을 알 수 있다.

1. 멀티미터 전면부 다이얼을 조정하여 스피커 모양의 Short Test모드로 이동시킨다.
2. 멀티미터 LCD창에 현재 측정된 저항값이 표시된다.
3. 멀티미터 케이블 끝의 악어 클립에 연결한 점퍼선을 브레드보드의 두 지점에 연결하여 저항값을 측정함으로써 두 지점이 서로 연결되어 있음을 파악한다. 
4. 그림에서 표시한 위치는 브레드보드 내부에서 서로 연결되어 있으므로 비프음이 나며 멀티미터 화면에도 작은 저항값이 표시된다.



![09_브레드보드_연결테스트_open_vertical](./images/09x.jpg '브레드보드 내부에 서로 연결된 부분 확인')

양 가장자리 쪽 서로 다른 세로줄 홀 간의 저항을 측정해보면 서로 끊어져 있음을 알게 된다.

1. 멀티미터 전면부 다이얼을 조정하여 스피커 모양의 Short Test모드로 이동시킨다.
2. 멀티미터 LCD창에 현재 측정된 저항값이 표시된다.
3. 멀티미터 케이블 끝의 악어 클립에 연결한 점퍼선을 브레드보드의 두 지점에 연결하여 저항값을 측정함으로써 두 지점이 서로 끊어져 있음을 파악한다. 
4. 예상한대로 그림에 표시된 브레드보드의 두 지점은 서로 끊어져 있으므로 소리가 나지 않으며 큰 저항값이 측정된다.

내부 배선 구조가 브레드보드 상판에는 정확하게 표기되어 있지 않거나, 간혹 내부 홀 불량이 있는 경우가 많으므로 반드시 회로를 구성하기 전에 반드시 short test를 통해 내부 연결 구조를 검사해보는 것이 좋다.



------------------
### 브레드보드에 올바른 저항 배치 방법

![10_브레드보드_저항측정_정상](./images/10x.jpg '브레드보드에 올바른 저항 배치 방법')

브레드보드에 저항을 올바르게 배치하는 방법을 살펴보고 브레드보드에 배치된 회로의 저항값을 측정해보자. 위의 그림은 브레드보드에서 내부 배선 구조상 서로 연결되어 있지 않는 두 지점에 저항을 연결한 모습이다. 양단 저항값을 측정하면 칼라 코드로 표기된 저항값의 크기와 같음을 알 수 있다.

1. 멀티미터 전면부 다이얼을 조정하여 저항 측정 모드로 이동시킨다. 현재 1KΩ 저항을 연결하였으므로 측정범위를 4KΩ 위치로 설정하자.
2. 그림과 같이 브레드보드에서 서로 연결되어 있지 않는 두 지점에 저항을 배치한다.
3. 멀티미터 LCD창에 측정된 저항값을 살펴본다. 정상적으로 측정되어 대략 1KΩ로 표시됨을 알 수 있다.



![11_브레드보드_저항측정_비정상](./images/11x.jpg '브레드보드에 잘못된 저항 배치')

위의 그림은 브레드보드에 저항을 잘못 배치한 모습을 보여준다. 위에 표시한 두 지점은 브레드보드 내부 배선 구조상 연결되어 있으므로 저항을 배치하는 것이 아무 의미가 없다. 어떠한 저항 크기이든 양단 저항은 0옴으로 측정될 것이다.

1. 멀티미터 전면부 다이얼을 조정하여 저항 측정 모드로 이동시킨다. 현재 1KΩ 저항을 연결하였으므로 측정범위를 4KΩ 위치로 설정하자.
2. 그림과 같이 브레드보드에서 서로 연결되어 있는 두 지점에 저항을 배치한다. 이 두 지점은 브레드보드 내부에서 직접 연결되어 있으므로 저항 크기가 0이다.
3. 멀티미터 LCD창에 측정된 저항값을 살펴본다. 배치된 저항값 1KΩ가 아닌 0에 가까운 값이 나온다. 따라서 잘못된 저항 배치 방법임을 알 수 있다.



------------------
## 전압측정

![12_회로구성_전압측정](./images/12x.jpg '브레드보드에 회로 구성 후 전압측정')

그림과 같이 브레드보드에 회로를 구성한 뒤 전압을 회로에 공급한 뒤 원하는 위치의 전압을 측정해보자. 전원공급기 사용법에 대해서는 장비 사용 섹션을 참고하도록 한다. 전원 VDD 및 GND라인은 브레드보드의 양 가장자리 쪽을 사용하는 것이 편하다. 위의 그림처럼 브레드보드 가장자리 쪽에 점퍼선을 이용하여 전원을 공급하면 가로방향으로 전원 라인이 브레드보드 내부에서 자동으로 구성되며 회로도와 유사한 모양으로 브레드보드에 회로를 꾸밀 수 있어서 편리하다.

1. 전원공급기 출력포트에 케이블 단자를 연결하고 반대쪽 빨간색 클립을 위 그림에 표시한 브레드보드의 빨간색 점퍼선 지점에 연결한다. (출력 VDD전압(+)을 브레드보드에 공급)
2. 전원공급기 출력포트에 케이블 단자를 연결하고 반대쪽 검은색 클립을 위 그림에 표시한 브레드보드의 -로 표시된 검은색 점퍼선 위치에 연결한다. (출력 GND전압(-)을 브레드보드에 공급)
3. 점선으로 표시된 라인은 이미 브레드보드의 내부에 연결되어 있으므로 별도의 점퍼선을 이용하여 연결할 필요가 없다.
4. 1KΩ을 그림과 같이 배치하고 VDD와 GND라인에 점퍼로 연결한다.
5. 저항 양단 전압을 측정하기 위해 그림과 같이 점퍼선을 이용하여 전압 측정 지점을 따로 뽑아둔다.



![12b_부팅_5V고정출력](./images/12bx.jpg '전원공급기 고정전압 출력 5V 생성')

전원공급기의 고정전압 출력 단자에 전원공급기 케이블의 잭을 연결하고 리드선 반대쪽 끝 악어 클립을 브레드보드에 배치한 회로의 특정 지점에 연결한다.

1. 그림에 표시된 전원 스위치를 눌러 전원을 켠다.
2. 고정전압 출력 포트에 빨간색 케이블 연결 (5V)
3. 고정전압 출력 포트에 검은색 케이블 연결 (GND)   

자세한 내용은 전원공급기 섹션을 참고한다.



![13_회로구성_전압측정](./images/13x.jpg '브레드보드에 회로구성 및 멀티미터를 이용한 전압측정(병렬)')

1. 멀티미터를 전압측정모드로 설정한다. 측정 전압을 예상하여 측정 범위를 적절히 조절한다. 
2. 멀티미터 연결잭을 본체에 결합하고 케이블 반대쪽 프로브 클립을 측정대상에 연결하도록 준비한다.
3. 전원공급기의 출력 (빨간색 케이블) VDD전압(+)을 브레드보드의 빨간색 점퍼선에 그림과 같이 연결한다.
4. 전원공급기의 출력 (검은색 케이블) GND전압(-)을 브레드보드의 검은색 점퍼선에 그림과 같이 연결한다.
5. 전압 측정 지점에 그림과 같이 멀티미터 측정 클립을 병렬로 연결한다.
6. 5V또는 3.3V가 측정될 것이다. (5V 또는 3.3V 여부는 전원공급기 출력포트 옆 스위치를 이용하여 조절가능. 전원공급기 설명섹션 참고)



![14_전원공급기_고정전압설정](./images/14x.jpg '전원공급기 고정전압 출력선택 (5V/3.3V)')

전원공급기의 고정전압 출력포트에서 생성되는 출력 전압값을 (5V,또는 3.3V 여부) 스위치로 선택할 수 있다. 연필 등을 이용하여 위 아래로 레버를 젖히면서 출력 전압을 조절할 수 있다. 

1. 전원공급기 하단에 그림에 표시된 위치에 출력 포트가 2개 존재한다. 왼쪽 포트에서 생성되는 출력 전압을 조절하기 위해서 그림에 표시된 부분의 스위치를 볼펜 등의 팁을 이용하여 위쪽 위치로 이동시킨다. 위로 이동시 5V가 출력되며 아래로 스위치를 내리면 출력으로 3.3V가 생성된다.

자세한 내용은 전원공급기 섹션을 참고하되 여기서는 고정전압 5V가 생성되는 출력 단에 케이블을 연결하여 회로에 공급해본다. 아래 그림처럼 악어클립의 색깔에 주의하면서 브레드보드의 VDD 및 GND라인에 정확하게 결착한다. 전원케이블을 움직이면서 실수로 브레드보드에 결합된 점퍼선이 미세하게 분리될 수 있으므로 주의하자.



------------------
## 전류측정

![15_회로구성_전류측정](./images/15x.jpg '브레드보드에 회로구성 및 전류측정 위한 점퍼선 연결')

저항을 통해 흐르는 전류를 측정하기 위해서는 위의 그림과 같이 저항과 멀티미터를 직렬로 연결하여야 하며 이를 위해 5번과 같이 점퍼선 이용하여 전류 측정지점을 따로 뽑아두어야 한다. 저항과 직렬로 연결하기 전에는 절대로 멀티미터의 동작모드를 전류측정모드로 설정하면 안 된다.

1. 전원공급기의 출력단자에 케이블 단자를 연결하고 반대쪽 빨간색 프로브 클립을 브레드보드의 빨간색 점퍼선에 연결한다.
2. 전원공급기의 출력단자에 케이블을 연결하고 반대쪽 검은색 클립을 브레드보드의 검은색 점퍼선에 연결한다.
3. 점선으로 표시된 라인은 이미 브레드보드의 내부에 서로 연결되어 있으므로 별도의 점퍼를 사용하여 연장할 필요가 없다.
4. 2KΩ을 그림과 같이 배치하고 초록색으로 표시된 점퍼를 이용하여 서로 연결한다.
5. 저항을 통해 흐르는 전류를 측정하기 위해 그림과 같이 2개의 점퍼선으로 뽑아두어 직렬로 멀티미터에 연결할 수 있도록 준비한다.



![16_회로구성_전류측정](./images/16x.jpg '멀티미터를 이용한 전류측정(직렬)')

전원공급기 출력을 브레드보드에 구성된 회로에 연결하여 전압을 공급하고 회로의 특정 지점을 통해 흐르는 전류를 측정해보자. 위 그림과 같이 멀티미터를 저항에 직렬로 연결하고 전면 동작모드를 전류모드로 설정한 뒤 전원공급기의 전원을 켜도록 한다.

1. 먼저 멀티미터를 전류 측정모드로 설정한다. 아직 멀티미터 측정 팁을 회로에 연결하지 않는다. 측정 전류범위를 적절하게 설정한다. 
2. 멀티미터 케이블 단자를 본체의 포트에 결합한다. 멀티미터 케이블 리드선 끝단 측정 클립을 대상회로에 연결하기 전에 반드시 측정 지점을 직렬로 연결하는지 한 번 더 살펴본다. 멀티미터를 전류측정모드로 설정할 경우 본체의 내부저항이 0이 되므로 저항 양단에 병렬로 연결하게 되면 멀티미터 본체 내부로 과전류가 흘러들어오게 되며 퓨즈가 끊어질 수 있다.
3. 전원공급기의 출력포트에 케이블 잭을 연결하고 반대쪽 빨간색 프로브 클립을 그림에 표시된 브레드보드의 빨간색 점퍼선 지점에 연결한다.
4. 전원공급기의 출력포트에 케이블을 연결하고 반대쪽 검은색 클립을 그림에 표시된 브레드보드의 검은색 점퍼선 지점에 연결한다.
5. 그림과 같이 전류 측정 지점을 2개의 점퍼 선으로 뽑아낸 곳에 멀티미터 측정 클립을 직렬로 연결한다. (측정 지점과 멀티미터가 직렬로 연결되어 있는지 연결구성을 반드시 확인한다.)
6. 멀티미터에 약 2.5mA가 측정되는지 확인한다.



## 결과보고서

1. 담당교수의 지시사항을 숙지하여 해당 내용에 대한 실험을 실시한다. 실험과정, 측정 데이터를 결과 보고서에 작성하여 제출한다.
2. 본 실험 자료에서 제시된 기본적인 실험 과정, 장비사용방법, 측정 결과들을 충실히 요약 정리한다. 
3. 실험과 관련된 이론과 실측치를 비교하여 회로의 전기적 동작 원리에 대해 생각해본다. (Optional) 
4. 전압을 병렬로, 전류를 직렬로 연결하여 측정하는 이유를 계측기 내부 회로의 구조관점에서 생각해보고 보고서에 추가로 작성한다. (Optional)




