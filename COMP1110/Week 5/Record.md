Record
Takes in a string and an enum. 

```java
record Student (String name, Grade grade){};
student stu = new Student(args[1], g);

void printSummary(Student stu){
String stuName = stu.name;
Grade stuGrade = stu.grade;
IO.println(stuName + " got "+ stuGrade);
}
```
You cannot compare records with == . You should use `.equals` like with [[String equality]].

![[Linked list]]