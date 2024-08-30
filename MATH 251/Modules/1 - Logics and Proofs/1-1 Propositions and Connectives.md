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
## Example: 1.1.3
	Prove that (P v Q) v (~P ^ ~Q) is a tautology

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
is true and has the form ~(P ^ Q), where P is "x is even" and Q is "x > 10." By part (h) of Theorem 1.1.1 this is equivalent to ~P v ~Q, which is
	"It is not the case that $x$ is even or it is not the case that $x > 10$."
An easier way to say this is
	"$x$ is not even or $x$ is not greater than 10,"
which may be restated as
	"$x$ is odd or or $x \le 10$."
A **denial** of a proposition *P* is any proposition equivalent to *~P*. A proposition has only one negation, *~P*, but always has many denials, including *~P*, \~\~\~P, \~\~\~\~\~\~P, etc. Some denials of "$x$ is odd" are "$x$ is not odd", "$x$ is even", and "$x$ is divisble by 2". DeMorgan's Laws provide other ways to construct useful denials.
==In other words a denial is a proposition that denies the original proposition and that there can be multiple ways of denying that proposition.==
## Examples 1.1.4
A denial of "Either the defendent paid a fine or the judge declared a mistrial" is
	The judge did not declare a mistrial and the defendent did not pay a fine."
- ### P = "The defendant paid a fine"
- ### J = "The judge declared a mistrial"
- ### ~P = "The defendent did not pay a fine"
- ### ~J = "The judge did not declare a mistrial"
This can be verified by first writing the two sentences symbolically as P v J and (~J) ^ (~P), respectively. Then we observe that P v J is equivalent to J v P, so a denial of P v J is equivalent to ~(J v P), which we know by DeMorgan's Laws is equivalent to (~J) ^ (~P). We could also verify that the sentence is a denial by checking the truth tables for P v J and (~J) ^ (~P) have exactly opposite values.
## Examples 1.1.5
Suppose $L_1$ and $L_2$ are two lines in a coordinate system. Find a denial of the statement
	"$L_1$ and $L_2$ have the same slope or $L_1$ and $L_2$ are vertical lines."
- ###  S = "$L_1$ and $L_2$ have the same slope,"
- ### P = "$L_1$ is a vertical line"
- ### Q = "$L_2$ is a vertical line"
The mathematical concepts expressed determine the form of the statement. The component S cannot mean "$L_1$ has the same slope" and "$L_2$ has the same slope". However, "$L_1$ and $L_2$ are vertical lines" must mean Component P and Q. The correct symbolization is S v (P ^ Q).
The negation of the statement is ~\[S V (P ^ Q)], which is equivalent to ~S ^ ~(P ^ Q). This form, in turn, is equivalent to ~S ^ (~P v ~Q). The denial proposition would then be:
	"$L_1$ and $L_2$ do not have the same slope, and either $L_1$ is not a vertical line or $L_2$ is not a vertical line."

Does someone who says, "Not P or Q" mean "Neither P nor Q" or "Either not P or else Q"? That is, should the symbolic translation be ~(P v Q) or (~P) v Q? The two translations are not equivalent. Ambiguities like this cannot be tolerated where precision matters.
Propositional forms are often written without all the parentheses you might expect. To correctly understand such a form, use these rules:
-  **~** always is applied to the smallest proposition following it.
-  **^** connects the smallest propositions surrounding it.
-  **v** connects the smallest propositions surrounding it.
Also when the same connective is used two or more times in succession, parentheses are restored from the left. Thus, ~P v Q is an abbreviation for (~P) v Q,  but ~(P v Q) is the only way to write the negation of P v Q. Here are some other examples:
- ~P v ~Q abbreviates (~P) v (~Q)
- P v Q ^ R abbreviates P v (Q ^ R)
- P ^ ~Q v ~R abbreviates \[P ^ (~Q)] v (~R)
- R ^ P ^ S ^ Q abbreviates \[(R ^ P) ^ S] ^ Q
- ![[Pasted image 20240829225751.png]]