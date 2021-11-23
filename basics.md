The aim of this notes is to force me to learn the basics of `Quantum Computation`. The perspective would be that of a `computer scientist`. The idea is to learn enough to be able to contribute to the field. This necessiates deeply understanding those few `key ideas` that make everything else trivial.

I assume the readers are already sufficiently motivated. So let's cut to the chase. 

`Quantum mechanics`

State is an elemnet of a linear vector space. And this state vector is a function of time. Now we need to prescribe a rule for how it evolves with time.

`Digression`: Linear Vector Spaces
Contains a set of elements called vectors (|x>,|y>). Now it says
a. adding two vectors(in any order) still gives a vector in the same space.
`Linear Vector space` over a field(see them as constants), such that c.|x> still gives an element in V.
b. There exits a special vector called `null-vector`, such that adding this to any vector gives the same vector.

Now we haven't added much structure to it yet. We haven't endowed the Rn with a metric yet.let's do that.
![q1](https://user-images.githubusercontent.com/21222766/142949053-dc551d4d-9c22-4f9f-8ecc-824b4a5a441c.png)

For every linear vector space we can define a dual. In euclidean space where it's self-dual, the distinction is lost. But, we have to take a vector from v and it's dual to generate scalars for any linear vector space. so <a|b> gives a scalar product or inner product.
Now what does an inner-product with itself represent. Now, we want to have a crucial property - ` <a|a> = 0 iff |a> is the null vector`. To do this for complex numbers we want the vectors in dual to be `complex conjugate transpose` and the scalar is being defined by their matrix product.
![q2](https://user-images.githubusercontent.com/21222766/142950502-f142ed5e-409a-4f42-8fb3-4ebd673da075.png)

So here a.b is not equal to b.a but equal to b*.a.(dot-products with complex entries).Now, we generalize the notion of distance.
![q4](https://user-images.githubusercontent.com/21222766/142951081-bfecf24e-160f-4d94-abbb-59b006eed9ae.png)


Linear Independence
Span

`observation`: we can have set of vectors that are linearly independent but do not span the space. We can also have set of vectors that are not `linearly independent` but `span` the space.

![q5](https://user-images.githubusercontent.com/21222766/142951935-88f04bdf-0e55-40ee-a212-ca961a643e79.png)

Set of vectors that are linearly independent and span the LVS forms a basis-set. Now how many vectors are there in the basis-set(any) of a linear vector space ?
If we don't have a finite basis set-> Infinite dimensional.
Square summable sequences. as it's self-dual. (Didn't understand)

Gram-Schmidt orthonarmalization ?
Gives an orthonormal basis. This procedures points us towards `operators`.
![q6](https://user-images.githubusercontent.com/21222766/142953277-d6f65c12-defd-40c1-964f-926f1510aa01.png)

How to remember: Ket vectors(|a>) are like column vectors. Bra Vectors are row-vectors. If we put a `bra` on right and a `ket` on the left, we will get a `scalar`. If we switch the order we get operators.

Thus Operator = |a> <b|, but in special case when we have a==b == c, then this operator projects a given vector along `c`.(projection operator)

![q7](https://user-images.githubusercontent.com/21222766/142953794-3c9d8f0e-b4fb-4a83-a335-02827c5dd8b2.png)

But is this a good notation.
What happens if we apply projection operator multiple times. We get a same vector ? Let's prove this bra, ket notation.
![q9](https://user-images.githubusercontent.com/21222766/142953963-91bd678d-b8ba-40c3-97b1-7a895c321e3b.png)

![q10](https://user-images.githubusercontent.com/21222766/142954247-adcd10b3-9fe1-4e65-a773-53305d662e5b.png)

![q12](https://user-images.githubusercontent.com/21222766/142955007-8c4f57d6-a757-4b28-a2dc-ffec4fe855e0.png)

![q11](https://user-images.githubusercontent.com/21222766/142954868-df38cad7-a094-4394-b8cc-76521c54f402.png)



Tracing History:

1. `Peter Shor (1994)` : A polynomial time algorithm for factoring integers.(quantum algorithtm). `Caveat`: Shor’s result does not prove that quantum computers can solve a problem more efficiently than a classical computer. It is unknown whether an efficient classical solution exists.
2.  `Grover’s search algorithm` : For unstructured search.

`Rules of the game`

1. The probabilistic nature of the interaction and the resulting change of state are features of all interactions between qubits and measuring devices, no matter what their physical realization.
2. Qubit: Any quantum mechanical system that can be modeled by a two-dimensional complex vector space can be viewed as a qubit


Some doubts:
a. Is a system of two particles(so 4 base states) same as single particle with 4 states-qudit.(as it seems in the first case prob need not add upto 1,infact they add up to 2)
Todo: Continue from CMU:[lecture 4](https://www.youtube.com/watch?v=8jW5ArmHLOI&list=PLm3J0oaFux3YL5qLskC6xQ24JpMwOAeJz&index=5)
