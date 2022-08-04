## 큐 (Queue) 

### 큐(Queue)의 정의
- 먼저 집어넣은 데이터가 먼저 나오는 **FIFO (First In First Out)** 구조로 저장하는 선형 자료구조  
ex. 매표소 대기열에서 먼저 줄을 선 사람이 먼저 나가는 것
- 나중에 집어넣은 데이터가 먼저 나오는 스택(Stack)과 반대 개념

<br>

### 큐의 표현  
![image](https://user-images.githubusercontent.com/87354210/182768707-bea9c828-e47c-4af8-86ca-7b21171cb156.png)  
- 큐는 처음 들어온 값은 처음에 나가고, 마지막에 들어온 값은 마지막에 나감
- 큐에 끝(Rear)에 요소를 추가하는 작업 : `enqueue`
- 큐에 맨 앞(Front)에 요소를 제거하는 작업 : `dequeue`  

<br>

### 기본 동작

- `enqueue()` - 큐에 끝(rear)에 항목을 추가
- `dequeue()` - 큐에 맨 앞(front)에 항목을 제거
- `peek()` - 큐에 맨 앞(front)에 있는 항목을 반환
- `isfull()` - 큐가 가득 찼는지 확인
- `isempty()` - 큐가 비어 있는지 확인  

<br>

### 시간 복잡도 (Time complexity)

Operation|Average|Worst|
---|---|---|
Access|Θ(n)|O(n)|
Search|Θ(n)|O(n)|
Insert(enqueue)|Θ(1)|O(1)|
Delete(dequeue)|Θ(1)|O(1)|

<br>

### 구현
큐를 구현하는 방법에는 두 가지가 있음.

- 배열 사용
  - 장점 : 구현하기 쉬움.
  - 단점 : 크기가 동적이 아님. 런타임 시 필요에 따라 늘어나거나 줄어들지 않음.

- 연결 리스트 사용
  - 장점 : 크기가 동적임. 런타임시 필요에 따라 크기가 확장 및 축소될 수 있음.
  - 단점 : 포인터를 위한 추가 메모리 공간이 필요함.
