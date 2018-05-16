# ArrayDate
#include "stdafx.h"
#include "iomanip"
using namespace std;
int fun(int aray[3][3]);
int main()
{
	int i, j;
	int aray[3][3] = { {1,2,3},{4,5,6},{7,8,9} }; printf("Converted before:\n");
	for (i = 0; i < 3; i++)
	{
		for (j = 0; j < 3; j++) { if (j != 2)printf("%d\t", aray[i][j]); else printf("%d\t\n", aray[i][j]); }
	}
	fun(aray);
	printf("Converted result:\n");
	for (i = 0; i < 3; i++) 
	{
		for (j = 0; j < 3; j++) { if (j!=2)printf("%d\t", aray[i][j]); else printf("%d\t\n",aray[i][j]); };
	}
}
int fun(int aray[3][3])
{
	int i, j, t;
	for (i = 0; i < 3; i++) { for (j = 0; j < i; j++) { t = aray[i][j]; aray[i][j] = aray[j][i]; aray[j][i] = t; } }return 0;
}
