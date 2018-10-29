# Search
## Binary Search
- 

## Interpolation Search
- 이미 정렬된 리스트에서 탐색 대상이 존재할 위치를 예측하여 탐색한다.
- 이진 탐색과 유사하나 리스트를 반으로 분할하지 않고 불균등하게 분할하여 탐색한다.
![InterpolationSearch](https://t1.daumcdn.net/cfile/tistory/2420A546574C427329 "Interpolation Search")
 - 찾는 데이터와 가까운 위치에서부터 탐색을 시작하기 때문에 탐색 대상을 줄이는 속도가 이진 탐색보다 뛰어나지만, 오차율을 최소화하기 위해 정수형 나눗셈이 아닌 실수형 나눗셈을 진행한다.
 - 평균적으로 O(log(log n))의 시간 복잡도를 보이나 최악의 경우 이진 탐색보다 느린 O(n)의 시간 복잡도를 보인다.

### 비례식
- s: 찾고자 하는 데이터가 저장된 위치의 인덱스 값
- low, high: 탐색 대상의 시작과 끝에 해당하는 인덱스 값
- x: 찾고자 하는 데이터의 값 arr[s]
  
  A : Q = (high-low) : (s-low)  
  s = Q(high-low)/A + low  
  s = x-arr[low](high-low)/arr[high] - arr[low] + low