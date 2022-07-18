# finding-highscore-student
# c program
# Let's find the student with the best grades among the students in the student list using the 'struct'! 학생리스트에 담긴 학생들중 학점이 가장 좋은 학생을 구조체를 이용해서 찾아보자!
#include <stdio.h>
struct student{
	int number;
	char name[20];
	float grade;
};
int main(void) {
	struct student list[]={{20180001,"홍길동",4.2},{20180002,"김철수",3.2},{20180003,"김영희",3.9}};
	struct student high_stu;
	int i, size;
	size=sizeof(list)/sizeof(list[0]);
	high_stu=list[0];
	for(i=1;i<size;i++){
		if(list[i].grade>high_stu.grade){
			high_stu=list[i];
		}
	}
	printf("평점이 가장 높은 학생은 이름: %s, 학번: %d, 학점: %f입니다.\n",high_stu.name,high_stu.number,high_stu.grade);
    return 0;
} 
#result--> 평점이 가장 높은 학생은 이름: 홍길동, 학번: 20180001, 4.2입니다.
