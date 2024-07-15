## 유튜브 링크
https://youtu.be/W82agW5uE5g

## 새로 추가한 기능
장애물에 부딪히면 부딪힌 더듬이방향에  LED가 켜지는 동시에 소리가 나며 90도씩 돌고,
양 더듬이가 동시에 부딪히면 180도 돌아가도록 했습니다.

## 소스코드
```c
#include <Servo.h>
Servo sl, sr;

void setup() {
  pinMode(7, INPUT_PULLUP);
  pinMode(5, INPUT_PULLUP);
  pinMode(4, OUTPUT);
  pinMode(8, OUTPUT);
  sl.attach(13);
  sr.attach(12);
}

void loop()
{
  byte wl = digitalRead(5);
  byte wr = digitalRead(7);

  if ((wl == 0) && (wr == 0)){
    digitalWrite(4, HIGH);
    digitalWrite(8, HIGH);doremi();
    backward(1000);
    turnLeft(1000);
  }
  else if (wl == 0){
    digitalWrite(8, HIGH);doremi();
    backward(1000);
    turnRight(500);
  }
  else if (wr == 0){
    digitalWrite(4, HIGH);doremi();
    backward(1000); 
    turnLeft(500); 
  }
  else{
    forward(20);
  }
}

void forward(int time){
  digitalWrite(4, LOW);digitalWrite(8, LOW);
  sl.write(1700);
  sr.write(1300);
  delay(time);
}

void turnLeft(int time){
  sl.write(1300);
  sr.write(1300);
  delay(time);
}

void turnRight(int time){
  sl.write(1700);
  sr.write(1700);
  delay(time);
}

void backward(int time) {
  sl.write(1300);
  sr.write(1700);
  delay(time);
}

void doremi(){
  tone(3, 2349, 500);
  }
``` 
 
## 작성소감
팀원들과 함께 고민하고 수업을 마친 후 모여서 코드를 짜보며 아두이노에 대한 관심을 높이고 팀원들 간의 협동심을 기를 수 있었습니다. 
수업시간에 배웠던 내용들을 이번 과제를 통해 다시금 복습할 수 있는 좋은 기회였습니다. 이 과제를 통해 아두이노에 대한 열정을 느낄 수 있었습니다. 
이 열정을 가지고 아직은 부족하지만 앞으로 더 노력해서 부족한 점을 채워나가는 학생이 되겠습니다.
이 과제를 내주신 교수님 정말 감사합니다! 이 과제를 통해 많은 것을 배웠습니다. 교수님 사랑하고 존경합니다
  
