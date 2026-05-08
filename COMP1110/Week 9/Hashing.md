Hashing
Say you wanted to find the most common element in a collection. One method would be to use an [[Array]] of numbers in a guaranteed range, create another array with the length of the range, and then directly add ++ to the count\[number] spot. 
However, for strings, this would not work. There is no index that we can use simply for the count[] array. 
Hashing provides a method around this.
A hash [[function]] H should
Respect equality (if a == b, then H(a) == H(b)) (not the same injectivity)
It should be deterministic -
	Each execution of H should give the same result for the same input. 
		If H(a) = X once, then H(a) will always equal X
	it should be fast 
	 It has to be constant [[time complexity]], relative to the amount of keys
Relatively evenly distributed 
	 H(a) should be relatively spread across its codomain(almost always int)

 
.hashCode() is a [[Method]] available on every java object. For strings, it will multiply each ascii code of the characters by 31. This ensures some spread over the codomain.

Hashing with strings would get the [[Modular arithmetic|modulus]] of the hashcode by 100. However, obeying [[pigeonhole principle]], it would be likely for clashes to occur. 

The basics of hashing in java takes advantage of this. It uses an [[Array]] with a fixed size. Each element in the array contains a linked list. The [[Linked list]] entries contains an integer denoting its count, and the string that it is. Its a sort of nested data structure, an array of linked lists.

Mutable keys: The key to a hash is the type of variable that you want to map to words. The key must NOT be [[Class mutability|mutable]]. You dont want the key to change.

Average complexity of a hash table, provided that you create enough pigeonholes, would be close to O(1).

# GET CODE FOR HASHING WHEN RELEASED - MOST COMMON STRING


Cryptographic hash
A different type of hash function to the one discussed in [[Hashing]]. It makes computing H(x) easy, but computing X from H(X) is difficult. This is useful for some scenarios, such as internet security. 
