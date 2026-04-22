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


A circular bufferChatHistory
```java
class circularBufferChatHistory implements ChatHistory{
	private String[] arr;
	private int nextAvailable;
	private int size;
	CircularBufferChatHistory(int capacity){
		this.arr = new String[capacity]
		this.nextAvailable = 0;
		this.size = 0;
	}
	public void addMessage(){
	
	}
	public void display(){
	
	}
}
```


