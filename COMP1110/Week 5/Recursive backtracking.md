---
{}
---
Recursive backtracking

Recursive backtracking is a sort of refined brute force that will eliminate choices that are not possible. Take the solution below:

```java
sealed interface BoolExp permits Constant, Variable, And, Or, Not
record Constant (boolean value) implements BoolExp {} 
record Variable(char name) implements BoolExpr {}
record And(BoolExpr left, BoolExpr right) implements BoolExpr {}
record Or(BoolExpr left, BoolExpr right) implements BoolExpr {}
record Not (BoolExpr e) implements BoolExpr {}

boolean evaluate (boolean[] assignment, BoolExpr expression){
	switch (expression){
		case and(BoolExpr left, BoolExpr right) -> {
			return evaluate (assignment left) && evaluate (assignment, right);
		}
		case or(BoolExpr left, BoolExpr right) -> {
			return evaluate (assignment left) || evaluate (assignment, right);
		}case not(BoolExpr e) -> {
			return ! evaluate (assignment, e);
		}case constant(B) -> {
			return b;
		}case Variable(char c) -> {
			return(assignment[c- 'a']);
		}
	}
}

```


This function above is a recursive function that will evaluate a boolean. 
```java
boolean solveRec(BoolExpr e, boolean[] soFar, int i) {
  if (i == 26)  {
    return false;
  }
  if (evaluate(soFar,e)) {
    return true;
  }
  // Try setting the i'th variable to true and then
  // solving the rest of the formula.
  soFar[i] = true;
  if (solveRec(e,soFar,i+1)) {
    return true;
  } else {
    //if that didn't work, then set it to false and then
    //solve the rest of the formula
    soFar[i] = false;
    return solveRec(e,soFar,i+1);
  }
}


boolean[] solve(BoolExpr e) {
  boolean [] assignment = new boolean[26];
  if (solveRec(e,assignment, 0)) {
    return assignment;
  } else {
    return null;
  }
}
```



solveRec is a function that will test each possible combination via two main combinations:   
```java
soFar[i] = true;
  if (solveRec(e,soFar,i+1)) {
    return true;
```
This will run the ENTIRE program again, with the current array index as **true**, testing each combination of true and false of the next array elements until it is finished. 

Then, if there is no possible combination with the original i at true, it changes it to false
```java
  } else {
    //if that didn't work, then set it to false and then
    //solve the rest of the formula
    soFar[i] = false;
    return solveRec(e,soFar,i+1);
  }
```
This is an incredible example of emergent complexity and demonstrates recursions potential.