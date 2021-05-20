# Job scheduling

## 201901701 이종웅
---

## Job scheduling
---
* n = [4, 8, 16]
* m = 2

기계에서 수행하는 n개의 작업[4, 8, 16]이 있고, 각 작업에 시작 시간과 종료 시간이 존재한다고 할 때  
기계 2개를 배치하면서 모든 작업을 수행하도록 한다.  
이 때, 수행 시간이 중복되지 않게 모든 작업을 가장 적은 수의 기계에 배정하는 최적해를 구해야 한다.  
---  

### 코드
---
```java
import java.util.*;
import java.util.Random;

public class Jobsceduling {
int n;
m = 2;

for (int i = 0; i < 100; i++) {
int time = rand.nextInt(11);

for( j = 1; j < m; j++) {
L[j] = 0;
for (i = 1; i < n; i++) {
min = 1;
for (j = 2; j < m; j++) {
if (L[j] < L[min]){
min = j;
}}}}

i -> min
L[min] = L[min] ti
} return

public static void main(String args[]){
ArrayList<Job> a = new ArrayList<Job>();
Random rand = new Random();
  
  a.add(new Jobscheduling(1));
  a.add(new Jobscheduling(2));
  a.add(new Jobscheduling(3));
  a.add(new Jobscheduling(4));
  
  }
```  
본래 생각은 문제대로 n= 4, 8, 16 일 때의 최적해와 근사해를 time 을 random 11로 하여 구하는 것이었는데 코드 구현을 하지 못하였습니다...  ---

### 시간복잡도
---
n개의 작업을 하나씩 가장 빨리 끝나는 기계에 배정한다.
기계를 찾기 위해 알고리즘의 for 루프가 (m-1)번 수행된다.
즉, 모든 기계의 마지막 작업 종료 시간인 L[j]를 살펴보아야 하므로
O(m) 시간이 걸린다.

m = 2

n개의 작업을 배정해야한다.
배열 L을 탐색해야하므로
n * O(2) + O(2) = O(2n) 이다.

n = 4, 8, 16
---

### 근사 비율

Jobscheduling 알고리즘의 근사해는 최적해의 2배를 넘지 않는다.
