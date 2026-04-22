---
{}
---
Record
Groups pieces of information together.

```java
record Student (String name, Grade grade){};
student stu = new Student(args[1], g);

void printSummary(Student stu){
String stuName = stu.name();
Grade stuGrade = stu.grade();
IO.println(stuName + " got "+ stuGrade);
}
```
You cannot compare records with == . You should use `.equals` like with [[String equality]].

Note that all records are examples of [[Class]]es.  Accessing a records values requires `stu.name()` as opposed to simply `stu.name`. This is because what is actually occurring is we are calling a [[Method]] in the record class that will return the value of the [[field]]. This is due to [[Encapsulation]]. 