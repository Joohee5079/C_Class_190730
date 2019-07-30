# C_Class_190730
업다운 게임


#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void main()
{
	int p, q, c = 0;
	srand((unsigned)(time(NULL))); //시간은 계속 변하기 때문에 시간에 "중복되지 않게 하려고" time(NULL)값을 준다.
	p = rand() % 100 + 1;
	do
	{
		printf("\n컴퓨터가 생성한 숫자는? >> ");
		scanf_s("%d", &q);
		c++;
		if (q == p)
		{
			printf("%d번만에 맞췄다.\n", c);
			break;
		}
		if (q > p) printf("~보다 작다. \n");
		else printf("~보다 크다.\n");
	} while (1);
	if (c > 10) printf("노력하세요.\n");
	else if (c > 7)printf("조금만 더..\n");
	else if (c <= 5)printf("훌륭합니다.\n");
}
