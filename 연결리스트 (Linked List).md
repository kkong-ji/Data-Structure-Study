## 연결리스트 (Linked List)

### 1. 연결리스트의 정의
- 데이터가 포인터로 구성된 노드 간의 연결 (link)을 이용해서 리스트를 구현한 것.
- 배열의 고정 크기의 단점을 보완하기 위해 고안됨.
- 배열과 달리 연속적인 메모리 공간에 저장되어 있지 않기 때문에 연결이 필요.  

### 2. 연결리스트 표현
![img](https://user-images.githubusercontent.com/87354210/182076174-689a3e62-32fd-4668-be5c-b76bdb77ab1e.png)
- Head : 리스트의 처음
- 노드는 데이터, 다음 노드를 가리키는 Next 포인터로 구성
- next 포인터를 통해 노드들이 연결됨
- Null : 리스트의 끝

### 3. 시간 복잡도
operation|time|
---|---|
시작 위치에 대한 삽입/삭제|Θ(1)|
마지막 위치에 대한 삽입/삭제|Θ(1)(마지막 요소 위치를 아는 경우)|
마지막 위치에 대한 삽입/삭제|Θ(1)(마지막 요소 위치를 모르는 경우)|
중간 위치에 대한 삽입/삭제|search time + Θ(1)|
인덱싱|Θ(n)
공간 낭비|Θ(n)

### 4. 특징
- 노드의 next 부분에 다음 노드의 위치를 저장. (선형적 데이터 구조)
- 연결되어있는 구조이기 때문에 데이터 탐색을 위해서 순차 접근만 가능.
- 주소만 연결하면 되기 때문에 삽입 삭제가 배열에 비해 빠르고 쉬움.
- 포인터로 인해 추가 저장공간이 필요.

### 5. 장점
- 크기가 가변적임
  - 메모리가 허용하는 만큼 커질 수 있음
- 삽입 삭제가 쉬움
  - 삽입 삭제 시에 데이터 이동이 필요 없음

### 6. 단점
- 랜덤 액세스가 불가능. 요소에 접근하려면 첫 번째 노드부터 순차 접근
- 포인터를 위한 추가 메모리 공간이 필요

### 7. 연결 리스트의 구분
- 단순 연결 리스트
- 이중 연결 리스트
- 원형 연결 리스트


