Our goal in this section and the next is to examine the structure of sentences used in making logical conclusions. Most sentences, such as "$\pi>3$" and "Earth is the closest planet to the sun", have a truth value (true or false). We call these <b>sentences propositions</b>. Other sentences, such as "What time is it?" (an interrogatory sentence) and "Look out!" (an exclamatory sentence) express complete thoughts but have no truth value.
## Definition - Proposition
	A proposition is a sentence that has exactly one truth value. It is either true, which we denote by T. or false, which we denote by F.

The statment "This sentence is false" is not a proposition because it is neither true nor false. It is an example of a <b>paradox</b> -- a situation in which, from premises that look reasonable, one uses apparently acceptable reasoning to derive a conclusion that seems to be contradictory.
By appyling logical connectivenes to proposition, we can form new propositions.
## Definition - Negation of a Proposition
	The negation of a proposition P, denoted ~P, is the proposition "not P". The proposition ~P is true exactly when P is false.
The truth value of the negation of a proposition is the opposite of the truth value of the proposition.
## Definition - Conjunction
	Given propositions P and Q, the conjunction of P and Q, denoted by P ^ Q, is the proposition "P and Q", P ^ Q is true exactly when both P and Q are true.
The English words *but*, *while*, and *although* are usually translated symbolically with the conjuction connective, because they have the same effect on truth value as *and*.
## Examples 1-1.1
	Let C be the proposition "19 is composite" and M be "45 is a multiple of 3." Then C is false and M is true. Thus the proposition C ^ M is false. We read C ^ M as "19 is composite and 45 is a multiple of 3".
The [[1-1 Propositions and Connectives#Examples 1-1.1|examples]] above illustrate an important distinction between a statement and a *form* of a statement. *The form P^Q itself has no truth value*. Only when the components *P* and *Q*T are assigned to be specific propositions does *P^Q* have the value T or F.
## Truth Table for Conjunction
| P   | Q   | P ^ Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | F     |
| F   | T   | F     |
| F   | F   | F     |
## Definition - Disjunction
	Given propositions P and Q, the disjunction of P and Q, denoted P V Q, is the proposition "P or Q". P v Q is true exactly when at least one of P or Q is true.
## Truth Table for Disjunction
| P   | Q   | P v Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | T     |
| F   | T   | T     |
| F   | F   | F     |
## Example 1-1.2
	If R is the proposition "12 is a prime number" and S is "16 is an integer power of 2," we know R is false and S is true. Thus, "12 is a prime number or 16 is an integer power of 2," which has the form R v S, is true. The false proposition "Either 12 is a prime number or 16 is not an integer power of 2" has the form R v ~S.

The statement "Either 7 is prime and 9 is even, or else 11 is not less than 3" may be symbolized by (P ^ Q) v ~R. Because the propositional form (P ^ Q) v ~R has three components (P, Q, and R), it follows that there are $2^3=8$ possible combinations of truth values in its truth table. The two main components are P ^ Q and ~R.
### Example: Truth Table for (P ^ Q) v ~R

| P   | Q   | R   | P ^ Q | ~R  | (P ^ Q) v ~R |
| --- | --- | --- | ----- | --- | ------------ |
| T   | T   | T   | T     | F   | T            |
| F   | T   | T   | F     | F   | F            |
| T   | F   | T   | F     | F   | F            |
| F   | F   | T   | F     | F   | F            |
| T   | T   | F   | T     | T   | T            |
| F   | T   | F   | F     | T   | T            |
| T   | F   | F   | F     | T   | T            |
| F   | F   | F   | F     | T   | T            |
In practice, we don't need make a complete truth table to determine the truth value of a specific statement. We can conclude that this statement is true because
* We know $P$ is true, $Q$ is false, and $R$ is false.
* Therefore, P ^ Q is false and ~R is true.
* Thus (P ^ Q) v ~R is true.
## Definitions - Tautology & Contradiction
	A tautology is a propositional form that is true for every assignment of truth values to its components.
	A contradiction is a propositional form that is false for every assignment of truth values to its components.
The *Law of Excluded Middle,* P v ~P, is an example of a tautology because it is true when P is true and true when P is false.
## Example: Prove that (P v Q) v (~P ^ ~Q) is a tautology

| P   | Q   | P v Q | ~P  | ~Q  | ~P ^ ~Q | (P v Q)  v (~P ^ ~Q) |
| --- | --- | ----- | --- | --- | ------- | -------------------- |
| T   | T   | T     | F   | F   | F       | T                    |
| F   | T   | T     | T   | F   | F       | T                    |
| T   | F   | T     | F   | T   | F       | T                    |
| F   | F   | F     | T   | T   | T       | T                    |
Both ~(P v ~P) and Q ^ ~Q are examples of contradictions. The negation of a contradiction is, of course, a tautology.
Particularly important in writing proofs will be the ability to recognize or write a statement equivalent to another. We say two propositional forms are <b>equivalent</b> if they have the same truth tables.
## Theorem 1.1.1 for propositions P, Q, and R, the following are equivalent:

| (a) P           | and ~(~P)             | Double Negation Law |
| --------------- | --------------------- | ------------------- |
| (b) P v Q       | and Q v P             | Commutative Laws    |
| (c) P ^ Q       | and Q ^ P<br>         | Commutative Laws    |
| (d) P v (Q v R) | and (P v Q) v R       | Associative Laws    |
| (e) P ^ (Q ^ R) | and (P ^ Q) ^ R       | Associative Laws    |
| (f) P ^ (Q v R) | and (P ^ Q) v (P ^ R) | Distributive Laws   |
| (g) P v (Q v R) | and (P v Q) ^ (P v R) | Distributive Laws   |
| (h) ~(P ^ Q)    | and ~P v ~Q           | DeMorgan's Laws     |
| (i) ~(P v Q)    | and ~P ^ ~Q           | DeMorgan's Laws     |
As an example of how this [[1-1 Propositions and Connectives#Theorem 1.1.1 for propositions P, Q, and R, the following are equivalent|theorem]] might be useful, suppose that for some integer $x$ we have determined that the statement "$x$ is even and $x>10$" is not true.
Then its negation,
	"It is not the case that the integer $x$ is even and $x>10$,"