## 배열 (Array)

### 1. 배열
- 연속된 메모리 공간에 순차적으로 저장된 데이터 모음
- 동일 타입 데이터만 저장  

ex.
35|2|7|13|22|44|8|                  
---|---|---|---|---|---|---|

<br>

### 2. 배열의 시간 복잡도 (Time complexity)
Operation|average case|worst case|
---|---|---|
read|O(1)|O(1)|
insert|O(n)|O(n)|
delete|O(n)|O(n)|
search|O(n)|O(n)|

<br>

### 3. 특징
① 동일한 데이터 유형을 가짐  
(cf. 이질형 데이터들이 모인 집합체는 레코드라고 함)  

② 배열의 각 요소에 접근하는 시간은 `O(1)`로 모두 동일  

③ 연속된 메모리에 단일로 데이터를 저장    
- 낭비되는 공간이 거의 없음  
- but, 배열의 크기가 커질 경우, 필요 메모리 할당이 불가능할 수 있음  

④ 실제 메모리 상에서 물리적으로 데이터가 순차 저장 (데이터에 순서가 있음)
- `index` 가 존재하여 `indexing` 및 `slicing`이 가능

<br>

### 4. 장점
① 인덱스로 접근 -> `모든 요소에 빠르게 접근이 가능`

② 기록밀도가 1이기 때문에 메모리 낭비가 없음  

③ 간단하고 사용하기 쉬움

<br>

### 5. 단점
① 배열을 선언한 후 할당된 메모리의 크기 변경 X  

② 중간에 특정 요소를 삽입 및 삭제하는 경우, 메모리가 순차적으로 이어져 있어야 하기 때문에  
요소들을 이동시켜주어야함. (삽입 및 삭제에 비용이 많이 듬)  

③ 배열의 크기가 정적으로 결정. 동적 상황에서 크기를 미리 결정하는 것이 어렵고,  
오버플로우나 저장공간의 낭비 초래 가능

<br>

### 6. 배열을 사용하는 경우
- 순차적인 데이터를 저장하며 값보다는 순서가 중요할 때  
- 다차원 데이터를 다룰 때  
- 어떤 특정 요소를 빠르게 읽어야 할 때  
- 데이터 사이즈가 자주 바뀌지 않으며, 요소들이 자주 추가되거나 삭제되지 않을 때  

<br>

## 2. ArrayList
- 엄밀히 말하면 배열과 다르지만 쉽게 생각해서 배열이라고 보면 됨
- 원하는 값을 추가 또는 삭제할 때, 배열의 크기가 n일 때 최대 n번의 이동이 필요
- 시간복잡도가 O(n)
- 파이썬에서는 arr = [], arr = list 와 같은 방식으로 사용

<br>

### 1. ArrayList를 사용할 때 주의점
- 배열의 삽입과 삭제가 빈번히 일어나는 문제에서는 시간복잡도를 신경써야함

<br>

### 2. ArrayList를 사용하는 예제
백준 10818번: 최소, 최대 문제

https://www.acmicpc.net/problem/10818

- 풀이
```python
N = int(input())
arr_list = list(map(int, input().split()))

max_num = arr_list[0]
min_num = arr_list[0]

for num in arr_list:
    if num > max_num:
        max_num = num
    if num < min_num:
        min_num = num

print(min_num, max_num)

```

