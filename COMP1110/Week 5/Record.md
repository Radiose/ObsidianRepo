Record
Groups pieces of information together.

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

Note that all records are examples o