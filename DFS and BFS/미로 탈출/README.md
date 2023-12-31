# 미로 탈출

### 문제 정의
- 동빈이는 N x M 크기의 직사각형 형태의 미로에 갇혀 있다. 미로에는 여러 마리의 괴물이 있어 피해 탈출해야 한다.
- 동빈이의 위치는 (1, 1)이고 미로의 출구는 (N, M)의 위치에 존재하며 한 번에 한 칸씩 이동할 수 있다.
- 이때 괴물이 있는 부분은 0으로, 없는 부분은 1로 표시된다.
- 미로는 반드시 탈출할 수 있는 형태로 제시된다.
- 이때 동빈이가 탈출하기 위해 움직여야 하는 최소 칸의 개수를 구하시오.
- 단, 칸을 셀 때는 시작 칸과 마지막 칸을 모두 표함해서 계산한다.

<br/>

- 입력 조건
  - 첫째 줄에 두 정수 N, M (4 <= N, M <=200)이 주어집니다.
  - 다음 N개의 줄에는 각각 M개의 정수(0 or 1)로 미로의 정보가 주어진다.
  - 각각의 수들은 공백 없이 붙어서 입력으로 제시된다.
  - 또한 시작칸과 마지막칸은 항상 1이다.
- 출력 조건
  - 첫째 줄에 최소 이동 칸의 개수를 출력한다.

<br/>
<br/>

### 문제 해성
- BFS는 시작 지점에서 가까운 노드부터 차례대로 그래프의 모든 노드를 탐색하기에\
  BFS를 이용 시 매우 효과적으로 해결 가능.
- (1, 1) 지점에서부터 BFS를 수행해 모든 노드의 값을 거리 정보로 넣으면 된다.
- 특정한 노드를 방문하면 그 이전 노드의 거리에 1을 더한 값을 리스트에 넣는다.
