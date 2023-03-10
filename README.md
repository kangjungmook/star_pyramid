# 별로 피라미드 찍는 알고리즘

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
<br> 첫 행부터 8, 7, 6 … 식으로 줄이면서 표시하게 되겠죠.
```java
    for (int j=0; j<i*2+1; j++) {
                System.out.print("*");
            }
            System.out.println();
```
* 세번째 for문은  두번째 * 표시 for 문은 곱하기 2 을 해서 표시해야
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
