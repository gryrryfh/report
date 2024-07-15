##  변경점
LED와 스피커를 이용하여 abot이 구급차의 사이렌소리인 미와 도의 주파수를 넣고 소리를 내면서 달리게 해보았습니다. 
그리고 이동하는 중 오른쪽으로 90도씩 돌게하여 제자리도 돌아오게 만들었습니다.

## 소스코드
```c
#include <Servo.h>     
Servo sl;                     
Servo sr;
void setup()            
{
  int i;
  pinMode(4, OUTPUT);
  sl.attach(13); sr.attach(12);

  while(1){
  sl.write(1300); sr.write(1700); 
  for(i = 0; i < 5; i++){
  digitalWrite(4, HIGH);  tone(7, 659, 300);
  delay(400);
  digitalWrite(4, LOW);   tone(7, 523, 300);
  delay(400);
  }
  sl.write(1500); sr.write(1500);
  delay(500);
  sr.write(1700);
  delay(700);
  }
}  
void loop()               
{                    
 } 
 ```
 ## 유튜브 링크 https://youtu.be/OAZStGuJ0oA
 
 
 ## 소감
 어릴적 가지고 놀기만 했던 자동차 장난감을 직접 만들어 보면서 아두이노에 흥미를 느낄 수 있었습니다. 팀원들과 함께 고민하고
 수업을 마친 후 모여서 코드를 짜보며 아두이노에 대한 관심을 높이고 팀원들 간의 협동심을 기를 수 있었습니다. 수업시간에 배웠던 내용들을 이번 과제를
 통해 다시금 복습할 수 있는 좋은 기회였습니다. 아직은 부족하지만 앞으로 더 노력해서 부족한 점을 채워나가는 학생이 되겠습니다.
 이 과제를 내주신 교수님 정말 감사합니다! 이 과제를 통해 많은 것을 배웠습니다. 교수님 사랑하고 존경합니다!♥!
