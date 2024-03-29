# Dijkstra Algorithm (다익스트라 알고리즘)
최단 경로 탐색 알고리즘은 게임에서 AI의 움직임을 정의할 때 많이 사용된다.  
다익스트라 알고리즘은 다이나믹 프로그램을 활용한 최단 경로 탐색 알고리즘.  
특정한 하나의 정점에서 다른 모든 정점으로 가는 최단 경로를 구할 때 활용.  
(다만, 이 때 음의 간선은 포함할 수 없음)  

## 기본 개념

**최단 거리는 여러 개의 최단 거리로 이루어져있다.**  
1. 출발 노드를 설정.  
2. 출발 노드 기준 각 노드로 가는 최소 비용을 배열에 저장.  
3. 방문하지 않은 노드 중에서 최저 비용의 노드를 선택.  
4. 해당 노드를 거쳐 다른 모든 노드들로 가는 경우의 비용을 계산해 최소 비용 배열을 갱신.
5. 모든 최소 비용이 갱신될 때까지 3 ~ 4를 반복.  
  
  **구현 방법**
  1. [인접 행렬을 이용한 선형 탐색](https://github.com/kkkh0315/Algorithms/blob/master/Studied_Algorithm_Lists/dijkstra/dijkstra(adjacency%20matrix).py)  
    시간 복잡도: O(N^2)  
    노드의 갯수가 많은데 간선은 적을 때 치명적으로 비효율적  
  2. [인접 리스트와 우선순위 큐를 이용한 방법](https://github.com/kkkh0315/Algorithms/blob/master/Studied_Algorithm_Lists/dijkstra/dijkstra(adjacency%20list).py)  
    시간 복잡도: O(NLogN)  
    지금까지 발견된 가장 짧은 거리의 노드부터 탐색  
    불필요한 계산을 스킵할 수 있음  
    

## 예제

1번 지점에서 다른 각 지점들로 갈 때의 각각의 최소 비용을 계산하여 배열에 저장해 반환하시오.  
*(예시) 1번에서 3번으로 가는 최소 비용은 4번과 5번을 거쳤을 때의 3이 된다.*
<br>
<img src="https://user-images.githubusercontent.com/60923302/94100688-2ab8d980-fe69-11ea-8bdb-2e9f8b113520.png" width="500" height="500">
