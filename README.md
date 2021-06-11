

# 기말고사  

## 201901701 이종웅  

---  
### 모의 담금질 기법(Simulated Annealing)  

`높은 온도에서 액체 상태인 물질이 온도가 점차 낮아지면서 결정체로 변하는 과정을 모방한 해 탐색 알고리즘이다.`  
`어려운 문제를 풀기 위해 점진적으로 그 해(solution)에 가까운 방향으로 이동하되 적은 확률로 예상되는 해에 아주 먼 방향으로 이동하는 것이다.`
`초기 탐색은 최솟값을 찾는데도 불구하고 확률 개념을 도입하여 현재 해의 이웃해 중에서 현재 해보다 나쁜(위 방향으로) 이동하는 자유로움을 보인다. 점차 탐색 방향을 아래 방향으로 향하고 점차 위 방향으로 이동하는 확률이 낮아진다. 처음 도착한 골짜기 (지역 최적해)에서 더 이상 아래로 탐색할 수 없는 상태에 이르렀을 떄 '운 좋게' 위 방향으로 탐색하다가 전역 최적해를 찾는다.`

### 계획

`3차 함수를 기준으로 계획을 해보았습니다.`  
`아래 그림에서 3차함수의 첫 지점을 (0,0)으로 하고 처음 고점의 위치를 (10,10), 전역 최소점의 위치를 (20,-10)으로, 마지막 끝 최고점의 위치를 (30,10)로 하였습니다.`
![캡처1](https://user-images.githubusercontent.com/80937145/121676697-e69d6000-caef-11eb-8805-2cde384cc0e5.PNG)
`먼저 x축과 y축의 확률을 각각 나누어 x축은 확률적으로 점차 증가하다가 30포인트에 도착하게 되면 0포인트로 다시 돌아가 또 다시 확률 적으로 점차 증가하게 하였습니다. y축의 경우 포인트에 점차 낮아짐에 따라 포인트가 낮아지는 확률은 낮아져 포인트가 낮아지는 확률이 점차 낮아지게 하였습니다.`
`초기해의 위치를 (0,100)으로 높은 곳에서 시작하여 확률적으로 점차 낮아지면서 전역 최적점을 찾고자 하였습니다. y축의 경우 y축의 감소 확률을 startpointy / 110 으로 설정하여 startpointy 즉 (0,100)에서 시작하여 점차 작아지는 y축은 낮아질 확률이 점차 줄어들게 됩니다. - 10포인트에 도달하였을 경우 y축은 멈추게 되고 최대로 낮아졌을 시 y 포인트는 -10 포인트로 전역 최적점에 도달 할 수 있습니다. `
`x축의 경우 x축이 증가할 확률을 1 / 10 으로 정해두고 30포인트에 도달하였을 시 +(-30,0)으로 0포인트로 돌아가서 다시 1 / 10 확률로 증가하도록 하였습니다. y축이 -10 포인트에 도달하였을 경우 y축이 멈추게 되고 x축의 증가확률은 꾸준히 1 / 10 입니다. x축은 꾸준히 왔다갔다 하므로 (20,-10) 포인트에 도달 할 수 있게 됩니다.`
`마지막으로 (20,-10)포인트에 도달 시 break를 걸어 멈추도록 하였습니다.`


 

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
