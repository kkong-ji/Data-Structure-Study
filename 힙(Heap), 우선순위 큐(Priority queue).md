## 1. 힙(Heap)

- 힙 자료구조는 다른 자료구조를 구현하는 기술 중 하나로 쓰임.
- 2가지가 존재
  1. 최소 힙 자료구조 : 최댓값을 구하기 위해서 부모노드의 값을 자식노드의 값보다 항상 크게 트리를 만듬.
  2. 최대 힙 자료구조 : 최솟값을 구하기 위해서 부모노드의 값을 자식노드의 값보다 항상 작게 트리를 만듬.
  
<br>

### 1-1. 최대 힙(Max Heap)
- 최대 힙은 부모노드가 자식노드보다 값이 큰 완전 이진트리를 의미
- 부모노드의 모든 값이 자식노드보다 커야함
- 최대 힙의 루트노드는 항상 최대값을 가짐
- 트리구조를 사용하기 때문에 데이터를 추가하거나 삭제할 때 : O(log)  
  최댓값을 찾는데 O(1)이 소요되는 매우 빠른 자료구조  
- 데이터의 삽입/삭제가 많을 때 최댓값을 정말 빠른 속도로 찾을 수 있음

<br>

### <최대힙 원소 추가 과정>  

1. 차례대로 7, 3, 6, 1, 2, 4 를 추가하면 다음과 같음 

![image](https://user-images.githubusercontent.com/87354210/216893461-5d4fdcf1-7f67-4050-b8d2-110e0bd87e32.png)
 
2. 이 상태에서 부모 노드보다 큰 값인 8을 추가한다면?  

![image](https://user-images.githubusercontent.com/87354210/216893765-17f52e6a-e9bc-4dc0-afe8-69d5de3dd265.png)

3. 8의 부모노드 6은 8보다 작으므로 위치를 바꿈.  
8의 부모노드 7은 8보다 작으므로 위치를 바꿈.  

![image](https://user-images.githubusercontent.com/87354210/216894296-429c0be9-e984-43dd-bc64-5b659546744a.png)  

결과적으로 루트 노드의 값은 8로 8이 모든 노드 중에서 가장 큰 값임을 볼 수 있음.

### <최대힙 원소 삭제 과정>
- 최대 힙에서 데이터 삭제는 데이터 값이 가장 큰 루트노드를 삭제함을 의미.

1. 루트 노드인 8을 삭제  

![image](https://user-images.githubusercontent.com/87354210/216918423-93e06245-c107-4501-bc54-5567874c603a.png)

2. 가장 밑에서 오른쪽에 있는 노드 6을 루트 노드에 위치시킴  

![image](https://user-images.githubusercontent.com/87354210/216918570-b1196526-9e9f-4329-ba3c-cc1603a1edd8.png)


3. 6의 자식 노드 중 3, 7은 6보다 크기 때문에 위치를 바꿔줌  

![image](https://user-images.githubusercontent.com/87354210/216918927-edc1b667-029c-49f5-9588-446a53f90072.png)

<br>

### 1-2. 최소 힙(Min Heap)
- 최소 힙은 부모노드의 값이 자식노드보다 작은 완전 이진트리를 의미 (최대 힙과 반대)
- 부모노드의 모든 값이 자식노드보다 작아야함
- 최소 힙의 루트 노드는 항상 최솟값을 가짐  

![image](https://user-images.githubusercontent.com/87354210/216921616-e87ccc42-0a4a-4670-b565-61e3c406e722.png)

### <최소 힙 원소 추가 과정> 

![image](https://user-images.githubusercontent.com/87354210/216921804-81bc814a-2a63-4e70-bf91-556e1590c747.png)


### <최소 힙 원소 삭제 과정>  

![image](https://user-images.githubusercontent.com/87354210/216922131-4454e16e-e6f3-4b50-ac04-f78c14597453.png)

<br>

## 2. 우선순위 큐(Priority Queue)
- 문제들을 풀 때 종종 볼 수 있는 자료구조
- 데이터의 최댓값 혹은 최솟값을 삭제하는 경우가 빈번하며 삭제를 해도 최댓값 혹은  
  최솟값을 O(1)로 확인하기 위한 자료구조  
- 힙 자료구조를 통해 구현하기 때문에 입력과 삭제에는 O(log 데이터의 개수)가 소요되며  
  이 때, 데이터를 추가하든 삭제하든 항상 최댓값 혹은 최솟값을 O(1)로 확인할 수 있다는 장점

<br>

### 2-1. 스택, 큐, 우선 순위 큐의 차이점
- 스택 : 가장 최근에 입력된 데이터가 가장 먼저 출력
- 큐 : 가장 처음에 입력된 데이터가 가장 먼저 출력
- 우선순위 큐 : 입력된 순서와 상관없이 우선순위가 높은 값이 가장 먼저 출력  
> 값이 큰 수에 우선순위를 높게 매기면? -> 최대 힙을 이용  
> 값이 작은 수에 우선순위를 높게 매기면? -> 최소 힙을 이용

