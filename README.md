#include<stdio.h>
#include<assert.h>

//限制长度的字符串拷贝函数
void Mystrncpy(char *des,char *src,int count)
{
	int i;
	for(i=0;i<count&&src[i]!='\0';i++)
	{
		des[i] = src[i];
	}

	while(i < count)
	{
		des[i++] = '\0';
	}
	printf("%s\n",des);
}

int main()
{
  //限制长度字符串拷贝测试用例
	char str1[10];
	char *str2 = "abcde";
	Mystrncpy(str1,str2,8);
  
  return 0;
}
