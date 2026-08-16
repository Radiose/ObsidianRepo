This is a method of factorising [[matrix|matrices]] into an upper triangular form and a lower triangular form.  

# Theory 
An M $\times$ N matrix can reach its [[row echelon form]] via applying sufficient [[Row operation]]s to it. 
We can express this via [[Matrix multiplication]] using [[elementary Matrix]]es 
$E_{k}\dots E_{2}E_{1}A = REF(A)$
$\iff A = E^{-1}_{1}E^{-1}_{2}\dots E^{-1}_{k}REF(A)$

Our goal is to *factorise* A into A = RU, where R is a lower triangular matrix, and U is the REF(A).

A key property: Lower triangularity is **closed under [[Matrix multiplication]].**
$\text{If } L_{1},\  L_{2} \text{ are lower triangular matrices, then }L_{1}L_{2}\text{ is also lower triangular}$

Thus, we are left with the question, can we make $E^{-1}_{1}E^{-1}_{2}\dots E^{-1}$ into a lower triangular matrix?
The only we can do this is via utilising only certain [[elementary Matrix|elementary matrices]]. 


# Creation
Because [[elementary Matrix]] 1 is always lower triangular, we can use it freely. 
Elementary matrix 2 is never lower triangular, so we can never use it
Elementary matrix 3 can only be used when we are applying operations from an upper row onto a lower row. 
The method to create the U factor is to multiply the *inverse* of all the row operations with each other. For example, for the simple row operation $R_{2}+R_{1}$, we would get the U factorisation by getting the elementary matrix of $R_{2}-R_{1}$

The golden reason to conduct [[LU factorisation]] is that once you have your two factors, you can solve a system in just two steps. 
$L \vec{y}=\vec{b}$
$U \vec{x}=\vec{y}$
