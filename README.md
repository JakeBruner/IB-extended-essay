# Jacob's Math Extended Essay

## Research Question:

To what extent does the difficulty of ascertaining the normal subgroups of an abelian group correlate with the efficiency and effectiveness of a cryptographic protocol?

## Thesis:

To a great extent, the difficulty of ascertaining normal subgroups correlates highly with the efficiency of a cryptographic protocol by providing more security at a given key length.

# Outline:

## Introduction: motivating problem

Pose a problem scenario with an eavesdropped connection
Highlight ‘commonly known’ symmetric encryption
Frame why the answer might be obtained with math
Hint towards using group-theory to formalize and generalize these

## What is public key cryptography (RSA)?

TS: The first protocol developed to address this motivating problem was RSA encryption. Leveraging intuitive properties of numbers, RSA establishes our idea of ‘one-way operations’ using simple multiplication of large, highly prime (minimal divisors), numbers.
Basic implementation
Math behind it
Modular arithmetic
Fermat's little theorem
Shortcomings

(Carmen et al. 883)

## How can we formalize the math behind this? -> Introduction to Group Theory

TS: Group theory provides us a way to generalize certain, often intuitive, properties of number systems, by using axiomatic structure to classify groups ‘up to isomorphism’ and to prove various properties about their structures. A ‘Group’ boils down to a set, infinite or finite, and an operation that takes two elements and maps it to another while maintaining some structure. It’s common to think that this structure is too vague, or broad, but, in fact, it’s enough to prove sweeping conjectures and determine non-trivial properties, thereby making itself a staple of modern mathematics.

Again motivating problem in “plain english”
Introduce formal definition: associativity identity inverse
Relate to certain intuitive examples (i.e., additive group of integers, multiplicative reals, numbers modulo prime, symmetries of a square)
Differentiate abelian and non-abelian groups
Describe RSA cryptography in group theory terms

(Koblitz 42)
(Sacarino 55)

## Group theory and cryptography -- normal subgroups of abelian groups

TS: Cryptographic schemes like RSA rely on the commutative property of their underlying abelian groups and their underlying difficulty of reversing a one-way operation, that is, solving it’s discrete logarithm, to ensure computational impossibility of a brute-force attack. Notably, since all subgroups of an abelian group are normal, this idea of reversing a one-way operation, in many cases, boils down to determining the normal subgroup generated by repeated operations, i.e., the hidden subgroup problem.

Introduce idea of subgroups
State hidden subgroup problem
Idea of a prime group (include/restate Lagrange’s theorem — order of subgroup must divide order of group)
Discuss factoring mod p, i.e., subgroups of a cyclic group of prime order.
Question whether there is another way

(National Institute of Standards and Technology)
(Sacarino)
(Koblitz)

## Strengthening the Subgroup Structure using another underlying group

TS: Given the generalizations provided by group theory, there is likely another underlying group that could provide more structural resistance to ascertaining subgroups.

Numbers have certain properties that make factorizing take less time than theoretically required
Begin with Circle group law
Show that it’s unfortunately isomorphic to a cyclic group so isn’t helpful
Motivate another abelian variety
Examine Elliptic curves (next genus up)
Describe chord/tangent law on elliptic curves
Prove that an EC is isomorphic to a direct product of cyclic groups
Describe how the hidden subgroup problem is made more difficult because the EC Discrete Log is more difficult

(Koblitz)

## Evaluate effectiveness of EC groups in cryptography

TS: Elliptic curves reach a sweet-spot balance between difficulty in a public key scheme and length of the key pairs used.

Discuss how another abelian variety can be more secure, but is less feasible in the real world
ECC only uses normal arithmetic operations, and not too many at that
Examine implementations of these technologies (ECDLC etc…)
Convey the scope/ubiquity of their implementation
(National Institute of Standards and Technology) (Sacarino)
