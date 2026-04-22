---
{}
---
reference type 
A value declared to be of a reference type, when initialised, will not contain the data of the type itself (EG, an [[Array]] ), but instead the location of the type in memory. This is why [[String equality]] has to be checked the way it does. If I create a pointer to a string, and another String that equals that pointer, then I can directly check if string1 == string2.


All types that start with a **capital letter** are of reference type. 
