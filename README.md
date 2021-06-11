# 기말고사  

## 201901701 이종웅  

---  
### 모의 담금질 기법(Simulated Annealing)  

`높은 온도에서 액체 상태인 물질이 온도가 점차 낮아지면서 결정체로 변하는 과정을 모방한 해 탐색 알고리즘이다.`  
`어려운 문제를 풀기 위해 점진적으로 그 해(solution)에 가까운 방향으로 이동하되 적은 확률로 예상되는 해에 아주 먼 방향으로 이동하는 것이다.`
`초기 탐색은 최솟값을 찾는데도 불구하고 확률 개념을 도입하여 현재 해의 이웃해 중에서 현재 해보다 나쁜(위 방향으로) 이동하는 자유로움을 보인다. 점차 탐색 방향을 아래 방향으로 향하고 점차 위 방향으로 이동하는 확률이 낮아진다. 처음 도착한 골짜기 (지역 최적해)에서 더 이상 아래로 탐색할 수 없는 상태에 이르렀을 떄 '운 좋게' 위 방향으로 탐색하다가 전역 최적해를 찾는다.`

### 계획

`3차 함수를 기준으로 계획을 해보았습니다.`
``
![][file:///C:/Users/Administrator/Desktop/KakaoTalk_20210611_183517306.jpg]
### 코드

```java
import java.awt.*;
import java.util.ArrayList;

public class simulatedannealing {
    private ArrayList see = new ArrayList <point> ();


    public pointy() {
        return point. y;
    }

    whlie(point. y >0) {
       int point = (int )(see point ());
    }

    private void point() {

    }


    public static void main (String[] args) {
    Point point = new Point(0, 0);
    Point point = new Point(10, 10);
    Point point = new Point(20, -10);
    Point point = new Point(30, 10);

}
}
```
