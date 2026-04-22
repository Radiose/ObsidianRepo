---
aliases:
  - interface
---
a non sealed interface can be implemented wherever, while a [[sealed interface]] can only be implemented where 
Interfaces are [[reference type]]. They serve as a contract. Any [[Class]] that implements an [[non sealed interface|interface]] must implement those methods. 

```java
interface ChatHistory{
void addMessage(){}
void display(){}
}
``` 
this can be implemented in another file 



```java
class LinkedListChatHistory implements ChatHistory{
	//defining type inside class makes type internal only
	record ChatLL(String msg, ChatLL rest){};
	private ChatLL list;
	LinkedListChatHistory(){
		this.list = null;
	}
	public void display(){
		ChatLL current = this.list;
		while(current != null){
			IO.println(current.msg());
			current = current.rest();
		}
	}
	public void addMessage(String msg){
		this.list = new ChatLL(msg, this.list;
		
	}
}
```

What this means is that whenever you need ChatHistory, you can provide an instance of a LinkedListChatHistory.
Any implementation of an interface must include the original [[Method]]s
In this way, a [[Class]] is a subitem of an [[non sealed interface|interface]], or more accurately, a [[Class]] gets put into categories, that are interfaces. 



### Extending an [[non sealed interface|interface]]
Here you add in more methods to the original interface. Its important to note that a [[Class]] can only extend one other class, while it can implement many [[non sealed interface|interface]]s. 

```java
// File: ErasableChatHistory.java
interface ErasableChatHistory extends ChatHistory {
  void erase();
}
```


