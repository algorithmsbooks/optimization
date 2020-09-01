# algforopt-errata

Errata for Algorithms for Optimization book

## First printing

* p. 10: Eq 1.14 and 1.16 should use x* in x*+hy (thanks to Chris Peel)
* Figure 3.6, page 38: F_2 should be F_3 and F_3 should be F_4 (thanks to Zdeněk Hurák)
* p. 57: Change "strong Wolfe condition" to "strong curvature condition" (thanks to Chris Peel)
* p. 78: Change eq 5.26 to use s of k+1 rather than s of k. RMSProp uses the most recent value. (thanks to Michael Gobble)
* Fig 5.7: change "hypermomentum" in legend to "hypergradient" and change caption to begin: "Hypergradient versions of gradient descent and Nesterov momentum compared on..."
* p. 110: Change "elseif yr > ys" to use \geq
* p. 138: Covariance matrix adaptation had inconsistencies with the recommended implementation in the original work. Primarily, this changes eq 8.18 such that first m_elite entries sum to 1, that all entries sum to approx 0, and that weights need not be non-negative. Eq 8.19 and 8.22 only sum to m_elite. (thanks to Arec Jamgochian)
* p. 160: The ref to eq. 9.8 in the last paragraph should actually be to eq. 9.7. (thanks to Anthony Corso and Joan Creus-Costa)
* p. 171: There should be minus signs instead of plus signs before each of the x_i terms under the square root (thanks to Zhengyu Chen)
* p. 174: Eq 10.20 should have a + instead of a - as the gradients must point in opposite directions and mu is non-negative (thanks to Erez Krimsky)
* p. 176: Stationarity condition should use a + instead of a -
* p. 177: Stationarity condition (eq 10.31) should use + instead of - (thanks to Erez Krimsky)
* p. 179, Example 10.5 optimum should actually be at -sqrt(3) rather than -1.5. Future releases will use x^2 < 1 so optimum will be at -1. (thanks yingjieMiao)
* p. 180: Ex 10.6 incorrectly optimizes the dual function. It should recognize that the dual function is unbounded below when lambda is less than 1/2. The dual problem is maximized at 1/2, yielding two optimal solutions.
* p. 195: In ex. 11.4, the minimization should be over x and s in the second problem and over x+, x-, and s in the third problem (thanks to Holly Dinkel)
* p. 200: The leaving index should be in B.
* p. 203: Ex 11.7 should read "causes x_4 to become zero" (thanks to Wouter Van Gijseghem)
* p. 208: The dual form should have a >= constraint. This must also be changed in alg 11.6. (thanks to Wouter Van Gijseghem)
* p. 209: Example 11.9 should use a >= constraint for A'mu.
* p. 248: Alg 13.11 should use 13 instead of 6 in its implementation. (thanks to Sudarshan Chawathe)
* p. 277: Ex 15.1 has 1^-1, which should be 2^-1 (thanks to Ryan Samuels)
* p. 284: In the matrix in Ex 15.3, the subscript of row 5, column 6 should be 21, not 12 (thanks to Veronika Korneyeva)
* p. 287: Add period to end of line 5. (thanks to Javier Yu)
* p. 324: Ex 18.1 analytic solution for variance was incorrect. (plot appears to be correct) (thanks to Veronika Korneyeva)
* p. 336: Fix q vector formatting in Ex. 18.6
* p. 347: Ex 19.3: Each of -0.091 - floor(-0.091) and -0.455 - floor(-0.455) should be reversed (thanks to Veronika Korneyeva)
* p. 426: Alg B1: The euler constant (\euler in Julia) does not exist in the DejaVu Sans Mono font, so is missing. (thanks Sudarshan Chawathe)
* p. 449: Eq D.2 should read: 4 * (-27) = -108
* p. 454: Changed two instances of sigma to mu on the left-hand-side of Excercise 8.4.
* p. 459: Ex. 11.3: solution should be "We can add a slack variable $x_3$ and split $x_1$ and $x_2$ into $x_1^+$, $x_1^-$, $x_2^+$, and $x_2^-$. We minimize $6x_1^+ - 6x_1^- + 5x_2^+ - 5x_2^-$ subject to the constraints $-3x_1 + 2x_2 + x_3 = -5$ and $x_1^+, x_1^-, x_2^+, x_2^-, x_3 \geq 0$." (thanks to Jimin Park)
* p. 463: Ex. 13.2: The probability converges to one. (thanks to Wouter Van Gijseghem and Jacob West)

### Minor
* p. 46: Change Eq 3.14 to use y_min on both sides for consistency
* Example 4.2: "satisfied" is twice misspelled as "satisifed."
* Fig 4.9: Needs one more iteration to get to x^10.
* Sec 4.5: "termination" is misspelled as "terminiation"
* Mu vector prior to Eq 8.18 should be bold. 
* p. 201: Changed "positive" to "non-negative" is 2nd-to-last paragraph
* p. 347: In Example 19.3, in the last array of equations, the right pair had too much space before the equals sign.
* The latest version of Julia includes Iterators in Base, so `product` can be accessed via `Iterators.product`.

## Second printing

* p. 46: Eq. 3.14 should be $\left[ x^{(i)} - \frac{1}{\ell}(y_{min}-y^{(i)}), x^{(i)} + \frac{1}{\ell}(y_{min}-y^{(i)}) \right]$ (thanks to Ross Alexander)
* p. 47: Change for clarity: updated algorithm to use y_min and replaced j with i. (thanks to Ross Alexander)
* p. 58: add missing alpha and betas in first inequality (thanks to Ethan Strijbosch)
* p. 60: Dropped all indexing in eqs 4.7-9, as it was inconsistent and not strictly needed. (thanks to Remy Zawislak)
* p. 72: Change for clarity: adjust indexing of d and g, but not beta, in conjugate gradient equations by -1. (thanks to Raman Vilkhu)
* p. 74: Keep up with Convex.jl API using solve!(p, SCS.Optimizer) in Alg 4.4 (thanks to Ross Alexander)
* p. 76: Ref 4, subscript should be superscript (thanks to Robert Moss)
* p. 102: Alg 7.4, the second instance of line_search should have x' instead of x (thanks to Kaijun Feng)
* p. 109: Alg 7.7, yr ≤ yh changed to yr < yh (thanks to Ellis Brown)
* p. 116: Multivariate direct was using max half-width rather than the distance from cell center to vertex. Changed text to "The lower bound for each hyper-rectangle can be computed based on the longest center-to-vertex distance and center value.". Updated Algs 7.10 and 7.11 to use vertex_dist() and OrderedDict. (thanks to Ross Alexander)
* p. 119: Alg 7.11 method for computing potentially optimal intervals was incorrect. [Updated algorithm is here.](https://github.com/sisl/algforopt-errata/blob/master/p119.pdf)
* p. 122: ex 7.2: The interval centers were incorrect. (thanks to Ross Alexander) 
* p. 127: ex 8.1: Change caption to: "Positive spanning sets for $\mathbb{R}^2$." (thanks to Ross Alexander)
                  Swap columns 2 and 3 and note that "the lower triangular generation strategy can only generate the first two columns of spanning sets."  (thanks to Kaijun Feng)
* p. 128: eq 8.5: Remove unnecessary min
* p. 128: Alg 8.2: Change for loop over j to set the lower triangular components rather than upper. 
                   Use D on right hand side of `D = L[:,randperm(n)]`.
* p. 140: eq. 8.23, $\delta^(i)$ should be boldface on the right hand side (thanks to Robert Moss)
* p. 147: Eq. 9.1: Remove boldface x (thanks to Ross Alexander)
* p. 171: ex 10.2, simplify example to not require any constraints by making h(x) a linear function; then x_n can be determined from x_1 through x_n-1
* p. 174: last terms in equations 10.16 and 10.17 should have minus sign (thanks to Vladislav Ankudinov) 
* p. 177: Sentence before eq. 10.36 should have "minimization" not "maximization" (thanks to Kaijun Feng)
* p. 183: Swap order of lambda and rho updates in Alg 10.2 (thanks to Stuart Rogers)
* p. 183: delete f(x) from Alg. 10.2 where p is defined (thanks to Kaijun Feng)
* p. 183: 0 above eq. 10.43 should be in bold (thanks to Ross Alexander)
* p. 196: "If a linear program contains feasible points, it also contains at least one vertex" -> "If a linear program has a bounded solution, then it also contains at least one vertex."
* p. 208-209: mu should be lambda and polarity of constraint in dual form should be A^T lambda <= c, [see corrected pages](https://github.com/sisl/algforopt-errata/blob/master/p208-209.pdf) with additional explanation (thanks to Masha Itkina)
* p. 242: Change Morris-Mitchell Criterion list from {1,2,3,10,20,50,100} to {1,2,5,10,20,50,100}. (thanks to Stephan Milius)
* p. 254: Theta should be upright bold in sentence before eq. 14.7 (thanks to Ross Alexander)
* p. 263: Change sidenote 8 to add " if $\lambda = 0$" and change "sufficiently large" to "positive". (thanks to Chris Peel)
* p. 294: Square sigma hat in eq. 16.5.
* p. 295: Eq 16.12 for expected improvement needs a sigma squared leading the 2nd term (thanks to Philippe Weingertner)
* p. 296: Alg 16.2 for expected improvement needs a sigma squared leading the 2nd term (thanks to Philippe Weingertner)
          Figure 16.6 updated to reflect this change to expected improvement.
* p. 325: Remove repeated equation 18.18 and insert step between 18.13 and 18.14. (thanks to Christoph Buchner)
* p. 329: Update to Polynomials.jl interface change; Poly->Polynomial, polyint->integrate, polyder->derivative
* p. 376: In Example 20.6, one of the B's had the wrong font. (thanks to Christoph Buchner)
* p. 402: Figure 21.11: The expression "f(v, s, r, p,..." was missing the c^{(d)} argument. (thanks to Christoph Buchner)
* p. 402: Figure 21.11: right hand side of top block, y^{(d)} should replace c^{(d)} (thanks to Loren Newton)
* p. 409: Exercise 21.4: The problem should use 10 degrees rather than 10 radians. (thanks to Sudarshan Chawathe)
* p. 418: Replace `supertype` with `supertypes`. (thanks to Ellis Brown)
* p. 441: Eq C.29: For clarity, reversed order of terms in each addition pair (thanks to Anil Yildiz)
* p. 453: Change "multivariate normal distributions" to "multivariate mixture distributions" (thanks to Javier Yu)
