---
{}
---
Logic circuits

in a simple circuit, you can model them with [[logical connective]]. EG with a basic switch, you can model it with p. EG if p is on, the light is on.

The connective $\land$ is useful for creating two switches after each other. 

the AND gate 
![[Pasted image 20260225191054.png]]




The or gate is also useful.
![[Pasted image 20260225191115.png]]

the not gate

![[Pasted image 20260225191139.png]]


Gates can be combined to create a circuit corresponding to a given compound statement.

A useful method for multiple wires leading to one output is to use x and y, or p and q. That way you can follow them to the finihs.

NAND gate
$\uparrow$ is a very important logical connective.
This is because $\uparrow$ can be make up many other ones. $\neg p\equiv p \uparrow p$
$x \land y \equiv \neg(x \uparrow y)$

![[Pasted image 20260225191214.png]]

recogniser circuits
A circuit that outputs 1 for only one input combination is called a recogniser for that input combination 