# elckekd
assignment
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int rockScissorsPaper()
{
 int x;
 x = rand() % 3 + 1;
 return x;
}
int winLoseDraw(int player, int opponent)
{
 if(player==1)
 {
  if(opponent==2)
   return -1;
  if(opponent==3)
   return 1;
  if(opponent==1)
   return 0;
 }
 if(player==2)
 {
  if(opponent==1)
   return 1;
  if(opponent==3)
   return -1;
  if(opponent==2)
   return 0;
 }
 if(player==3)
 {
  if(opponent==1)
   return -1;
  if(opponent==2)
   return 1;
  if(opponent==3)
   return 0;
 }
}
int main()
{
 int x,y;

 srand((unsigned int)time(0));

 do
 {
  do{
   printf("가위(1), 바위(2), 보(3) 입력, 끝내려면 0 : ");
   scanf("%d",&x);
  }while(x<0||x>3);
   y = rockScissorsPaper();
  if(x!=0)
  {
  printf("당신 = %d, 컴퓨터 = %d :",x,y);
 
  if(winLoseDraw(x,y)==1)
   printf(" 이겼습니다.\n");
  if(winLoseDraw(x,y)==-1)
   printf(" 졌습니다.\n");
  if(winLoseDraw(x,y)==0)
   printf(" 비겼습니다.\n");
  }
 }while(x!=0);

 return 0;
} 

