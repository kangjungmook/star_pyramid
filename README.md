# 별로 피라미드 찍는 알고리즘

* 처음에 사용자가 입력받은 정수를 쓰면 그에 대한 피라미드의 층수가 나오고 <br>
  그 피라미드의 모양을 잡기 위해서 공백으로 모양을 잡아 주면 됩니다.<br>
  공백을 잡기 위해서는 반복문을 써서 (전체층 - 현재층) 하면 됩니다. <br>
  그리고나서 모양을 잡아 줬으면 별을 찍어 줘야 하는데 벽을 찍기 위해서는 일단 별의 개수가 홀수가 되야 합니다.<br>
 다음엔 반복문을 써서 현재층 에서 * 2 를 해서 개수를 늘이고 홀수를 만들기 위해서 +1 을 합니다.<br>
 <br>
 
 ## 자바로 구현을 해본다 

```java
        Scanner sc = new Scanner(System.in);

        System.out.println("몇 단을 출력할껀가요?");
        int num =sc.nextInt();
```
* 스캐너로 키보드로 입력 받을 정수를 가져온다

```java
        for (int i=0; i<num; i++) {
            for (int j=1; j<num-i; j++) {
                System.out.print(" ");
            }
```
* 첫번쨰 for 문은 num 에서 받아온 정수만큼 피라미드를 출력 하는 것이고
 두번 쨰 for 문은 공백을 출력 하는 것 입니다.<br>예를 들어
num = 10 이라고 했을 때 for 문안에 있는 첫번째 for 문은 공백을 표시하게 됩니다
<br> 첫 행부터 8, 7, 6 … 식으로 줄이면서 표시하게 됩니다
```java
    for (int j=0; j<i*2+1; j++) {
                System.out.print("*");
            }
            System.out.println();
```
* 세번째 for문은 * 을 출력 하기 위해 곱하기 2 을 해서 표시해야
<br>되는 개수를 늘이고 홀수로 만들기 위해 +1 을 했습니다. 
<br>홀수로 만들어야 양쪽으로 동일한 크기의 표시가 가능합니다

## 전체 코드
```java
import java.util.Scanner;

public class TriangleLB {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("몇 단을 출력할껀가요?");
        int num =sc.nextInt();

        for (int i=0; i<num; i++) {
            for (int j=1; j<num-i; j++) {
                System.out.print(" ");
            }
            for (int j=0; j<i*2+1; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
## 실행화면
![image](https://user-images.githubusercontent.com/106642094/224196116-3df09e6f-b106-4052-aa8d-86047a4b07b2.png)
