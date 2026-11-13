We have an overarching goal of communicating over noisy channels. In particular, to be able to communicate with small probability of error, and high rate.
Our current concept of repetition codes introduce redundancy on a per bit basis.
Improving on this can be done via introducing redundancy to blocks of data instead. 

We do this via hamming codes. 

# The (7,4) Hamming code 
This hamming code is based upon the $K=4,N=7$ $(N,K)$ [[block code]]. So it codes length 4 blocks


We demonstrate this via coding the sequence $1\ 0\ 0\ 0$


![[Pasted image 20261113170622.png|428]]
We write the source code bits into the arrangement shown above.
So we get:
![[Pasted image 20261113170604.png|437]]

Then, our parity check bits are the bits that we set $t_{5},t_{6},t_{7}$ in order to ensure EVEN quantities of  $1$ bits inside each circle.

 
![[Pasted image 20261113171116.png|395]]

 ![[Pasted image 20261113171441.png|298]]
This gives us $1,0,1$ as our final sequence of bits we add to our block 

Algebraically, we have set $t_{i}=s_{i}$ for $i=1,..,4$
So, $t_{5}=s_{1} \oplus s_{2} \oplus s_{3}$
$t_{6}=s_{2} \oplus s_{3} \oplus s_{4}$
$t_{7}=s_{1} \oplus s_{3} \oplus s_{4}$
this is more apparent when you view the image above. 
