#include<time.h> 
#include<stdio.h> 
#include<conio.h> 
#include <stdlib.h> 

char x,response; 
int y,draw,win,loss;  
void main() 
{ 
c: draw = 0,win = 0,loss = 0; 
d: system("cls"); 
	printf("welcome\n\n"); 
	printf("石头剪刀布 \n"); 
	printf("0:石头   1:剪子   2:布\n"); 
	printf("\n请选择:"); 
	if((x = getch()) == '0')  
		printf("石头"); 
	else if(x == '1')   
		printf("剪子");
	else if(x == '2')  
		printf("布"); 
	else  {    printf("请按0-2\n按任意键继续\n"); 
	getch();   
	goto d;  } 
	srand((unsigned)time(NULL)); 
	y = rand()%3; 
	result=(int)gamer+y; 
	switch(y)
	{   
	case 0:    
		printf("\n\n电脑出拳:石头\n\n");    break;  
	case 1:     printf("\n\n电脑出拳:剪子\n\n");   break;   
	case 2:     printf("\n\n电脑出拳:布\n\n");    break; 
	}   
	if(x == '0')  
	{    switch(y){
		case 0:      printf("平局");     draw++;     break;  
		case 1:      printf("你赢了");     win++;     break;   
		case 2:      printf("你输了");   
			loss++;     break;   } 
	}  
	else if(x == '1') 
	{    switch(y)
	          {     case 0:      printf("你输了");loss++;     break;   
			  case 1:      printf("平局");     draw++;     break;   
			  case 2:      printf("你赢了");     win++;     break;   } 
	}   else if(x == '2') 
	{   
				  switch(y)  
				  {     case 0:      printf("你赢了");     win++;     break;  
				  case 1:      printf("你输了");loss++;     break; 
					   case 2:      printf("平局");     draw++;     break; 
				  }  
	}  
	printf("\n\n你的战况:赢%d局   输%d局    平%d局", win, loss, draw);  
	if(win <= loss+draw)  {    printf("\n\n还不服气?\nY or N?\n");   response=getch();  
	if(response == 'Y' || response == 'y' || response == 13)  
	{       
	response = getch();    
						   if(response == 'Y' || response == 'y' || response == 13)   
						   {      goto c;    }     goto d;   } 
	}  else
		{    printf("\n\n厉害,继续?\nY or N?\n");   
	response = getch();    
	if(response == 'Y' || response == 'y' || response == 13)   
	{      
	if(response == 'Y' || response == 'y' || response == 13)  
	{      goto c;   
	}     goto d;   } 
	}if(win>loss){printf("win\n");break;}
	else{printf("loss\n";break;)}9


}
