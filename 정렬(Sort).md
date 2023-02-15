## 정렬
- 데이터를 정렬하는 방법에 대한 알고리즘  
ex. { 3, 4, 6, 1, 8 } 을 오름차순으로 정렬 : { 1, 3, 4, 6, 8 }


### 1. 선택 정렬 (Select Sorting)
- 처리되지 않은 데이터 중에서 가장 작은 데이터를 선택해  
맨 앞에 있는 데이터와 바꾸는 것을 반복
- N번 만큼 가장 작은 수를 찾아서 맨 앞으로 보내야함 (시간 복잡도 : O(N**2))

![image](https://user-images.githubusercontent.com/87354210/218942215-880606cb-8a04-4021-877d-26f69797e56c.png)


### 1-2. 선택 정렬 소스코드

```python
array = [7, 5, 9, 0, 3, 1, 6, 2, 4, 8]

for i in range(len(array)):
  min_index = i # 가장 작은 원소의 인덱스
  for j in range(i + 1, len(array)):
    if array[min_index] > array[j]:
      min_index = j
  array[i], array[min_index] = array[min_index], array[i] # 스와프
  
  print(array)

```

### 2. 퀵 정렬 (Quick Sorting)
- 분할정복을 통해 구현 가능
- 평균적으로 매우 빠른 속도를 자랑하는 정렬 방법
- 평균의 경우, O(N log N) 의 시간 복잡도
- 하지만 최악의 경우, O(N**2)의 시간 복잡도

1) 분할 : 집합을 pivot 위치를 기준으로 2개의 부분 배열로 분할
2) 정복 : 부분 배열을 정렬
3) 합병 : 정렬된 부분 배열을 하나의 배열로 합병

![image](https://user-images.githubusercontent.com/87354210/218943474-7f32a310-6552-4e18-b477-c71539d0d49a.png)


### 2-1. 퀵 정렬 소스코드
```python
array = [5, 7, 9, 0, 3, 1, 6, 2, 4, 8]

def quick_sort(array):
  # 리스트가 하나 이하의 원소만을 담고 있다면 종료
  if len(array) <= 1:
    return array
  pivot = array[0]  # 피벗은 첫 번째 원소
  tail = array[1:]  # 피벗을 제외한 리스트
  
  left_side = [x for x in tail if x <= pivot]   # 분할된 왼쪽 부분
  right_side = [x for x in tail if x > pivot]   # 분할된 오른쪽 부분
  
  # 분할 이후 왼쪽 부분과 오른쪽 부분에서 각각 정렬 수행하고, 전체 리스트 반환
  return quick_sort(left_side) + [pivot] + quick_sort(right_side)
  
print(quick_sort(array))
```




