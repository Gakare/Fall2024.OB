1. Introduction to the time-value of money
2. Simple vs Compound interest
3. The "Rule of 72"
4. The concept of equivalence
5. Compound interest formulae
6. Steps in solving engineering economics problems
# Introduction: The time-value of money
* Suppose you were given the following options
	1. Getting $1,000 today
	2. Getting $1,000 two years from today.
		Which deal will you take?
* Most rational people go for option 1 as better of the two options. Why?
	* You can invest the $1,000 today and more than $1,000 in two years, or
	* You can buy more service/goods with $1,000 today, than with the same amount year 2 hence, due to the increase in prices of service and goods over time (inflation...)
		$\rightarrow$ In other words, time affects the value of money, i.e., money now is generally more valuable than more later
	* And that is one of the reasons that when you borrow money, you have to pay back in future more than what you borrowed, i.e., you pay back with "interest".
	* Similarly, when you invest your money somewhere, you expect to get paid back in future more than what you invested, i.e., you expect your money to earn an interest.
# Types of interest
## Simple vs Compound Interest
- ###  <u>Simple interest</u> is when the interest is applied only on the initial amount of money borrowed or invested (principal).
In this case, the total interest amount in any period,
	$I_k=(P)\times(i)$, where $i$ is the interest rates per period
And the total interest amount after N periods = $(P)\times(i)\times(N)$,
Therefore, the future value of an initial principal, P, after N periods,
	F = Principal + Total interest amount
	= P + (P)(i)(N)
	= P(1+Ni)
## Example 1:
What is the value of a $200 loan after 3 years if it is subject to a simple interest rate of 8% per year?
![[Ex_1.png]]
# Compound Interest
- In this case, the interest charged or earned in period (k) is applied to the original principal plus the total interest amount accrued or earned in the previous k-1 periods, i.e.,
	Interest amount in period k,
		$I_k=(F_{k-1}\times(i))$
	where
		(**$i$**) is the interest rate per period	
		(**$F_{k-1}$**) is original principal plus the total interest earned in the first k-1 periods
This translates into the following general relationship for the future amount, $F_N$, of an original principal, P, after N periods,
	$F_N=P(1+i)^N$ and, conversely
	$P=F_N(1+i)^{-N}$
## Example 2:
What is the value of a $200 loan after 3 years if it is subject to a compound interest rate of 8% per year?
![[Ex_2.png]]
<u>Note that</u>, in this class, we are going to deal exclusively with a compound interest, since it is the most commonly applied in the real world.

# The Rule of 72
- Based on the compound interest, the "Rule of 72" states that the number of periods required for the future amount to be twice the original principal is approximately equal to
	$N\approx\frac{72}{i}$ where $i$ is the interest rate per period in %
- Conversely, the interest rate required to double an original principle in N periods approximately equal to
	$i\approx\frac{72}{N}\%$

## Example 3a:
(a) How long will it take for a $2,000 investment to double to $4,000 if the investment earns an annual rate of return 6% per year?
![[Ex_3a.png]]
This confirms the accuracy of the estimate obtained using the Rule of 72.
## Example 3b:
(b) What interest rate is needed to double an initial principal in 5 years?
![[Ex_3b.png]]
# The Concept of Equivalence
- The *concept of equivalence* enables on to compare the "values" of cash flows that occur at different points in time.
- These could be single cash flows at different points in time, or a series of cash flows over several periods

The following two examples illustrate this concept
## Example 4A: Present Worth and Future Worth concepts
If you invest \$2,000 today in an account that earns an interest rate 5% per year, how much money will you have in the account after 4 years?
![[Ex_4A.png]]
	$F_N=P(1+i)^N=\$2,000(1+0.05)^4=\$2,431$
Then, using the concept of equivalence, the following statement can be made regarding this scenario:
- The \$2,000 you have today is __*equivalent to*__ the \$2,431 that you can have 4 years from now. In other words you would be indifferent between the choice of having \$2,000 today or waiting to get \$2,431 four years from now.
	
You can also make the following alternative statements:
- \$2,431 is the 4-year __*future worth*__ of today's \$2,000; or alternatively,
- \$2,000 is the __*present worth*__ of a 4-year future \$2,431 cash flow.
	
Note that:
	The **future worth** of initial principal P is equal to $F=P(1+i)^N$, or
	The **present worth** of a future cash flow F is equal to $P=F(1+i)^{-N}$
## Example 5A: Comparing alternative investment scenarios using the "concept of equivalence"
Calculate the equivalent present worth of each of the following two alternatives based on an annual interest rate of 8% and compare them.

|                           |           Alternative 1 |           Alternative 2 |
| ------------------------- | ----------------------: | ----------------------: |
| Initial investment cost   |                 $10,000 |                 $10,000 |
| Revenue end of year 1     |                  $7,500 |                  $1,500 |
| Revenue end of year 2     |                  $4,000 |                  $4,000 |
| Revenue end of year 3     |                  $1,500 |                  $7,500 |
| Net revenue after 3 years | \$13,000-10,000=\$3,000 | \$13,000-10,000=\$3,000 |
 - Note that both alternatives have the same net revenue of \$3,000 after three years. However, the timing of the annual revenues is different.
 - The solution involves calculating and comparing the equivalent (PW) of each alternative, which is sum of the PWs of the individual future revenues minus the initial cost, i.e.,
 - Alternative 1 has larger revenues early while Alternative 2 has larger revenues late. Therefore, these two alternatives may have different net profit if the time-value of money is applied. Therefore, to compare the alternatives we will compute the present worth of each alternative and compare them.

Based on the interest rate of 8% per year, the present worth (PW) of each alternative is equal to the sum of the PW of the individual future revenues minus the initial cost, i.e.,
![[Ex_5A.png]]
i.e., Alternative 1 cash flows have an *equivalent present worth* of $1,564, and the Alternative 2 cash flows have an *equivalent present worth of* only $772. This means that Alternative 1 should be preferred, since it has a higher equivalent present worth. This makes sense, since money now is generally worth more than the same amount years later. And since Alternative 1 has larger revenues early on, it makes sense for it to be the more economical alternative.

Thus, using the concept of equivalence, we have been able to reduce the series of cash flows for each alternative into one equivalent present worth value which takes into account the time value of money by applying an interest rate. The alternatives can then be more readily compared and choice made on a more economical alternative.

# 3.4 Derivation Of Compound Interest Rate Formulae:
## 3.4.1 Introduction - Symbolic notations, cash flow diagrams and sign convention
This section presents the derivation of a number of formulas relating different types of cash flows with the interest rate per period and the number of periods

**Symbolic notation of cash flows parameters**
	$i$ = effective interest rate per period
	$N$ = number of compounding periods (or length of analysis, in periods)
	$P$ = present sum of money or cash flow at period $N$
	$F$ = future single sum of money or cash flow at period $N$
	$A$ = uniform regular end-of-period cash flows from period 1 to $N$.
# Cash-flow diagram
- A cash flow diagram is a schematic representation of the project cash flows over time.
- Typically, the x-axis represents time periods and each cash flow is placed at an appropriate time period and represented by a vertical arrow either facing upwwards for positive cash flows, or downwards for negative cash flows.

# Sign convention of cash flows in a cash-flow diagrams
- Cost or expenditures are considered "**negative**" cash flows and are represented by "downard-pointing" arrows.
- Revenues or incomes are considered "**positive**" cash flows and are represented by "upward-pointing" arrows.
Whether a cash flow is positive or negative often depends on the **point of view**.

For example a loan from a bank to a customer is a positive cash flow to the customer, but a negative cash flow to the bank.
On the other hand, when the customer starts paying-off the loan, the payments are negative cash flows to the customer, but positive cash flows to the bank.
Therefore, when drawing cash flow diagrams, one has to be clear on from whose point of view the cash flow diagram is being drawn.

For example, a bank loan from the point of view of the client (i.e., recipient of the loan) will have the loan amount as a positive cash flow (upward pointing arrow), and the monthly loan payments as negative cash flows (downward pointing arrows).
Cash Flow Diagram (CFD) for a bank loan:
![[Ex_CFD.png]]

Note that
- The diagram shows that the loan has to be paid back in 36 uniform monthly payments, A, at a monthly interest rate of $\frac{1}{2}\%$. The payment start 1 month after receiving the loan.
- This CFD is drawn from the <u>point of view of the client</u> who gets the loan, hence, the loan, P, is a positive cash flow to the client, therefore an upward-pointing arrow. On the other hand, the payments, A, are costs and therefore negative cash flows represented by a series of downward-pointing arrows from month 1 to 36.

## 3.4.2 Compound interest formulae for single cash flows P and F
Standard cash flow diagram:
![[CFD_FPFPIN.png]]
## Finding the future worth, F, given P, i, N
$F=P(1+i)^N$
The factor $(1+i)^N$ is referred to as the "**compound amount factor**".
It is usually denoted as (F/P, i, N) and stated as "finding F given P, i and N", i.e.,
$F=P(F/P,i,N)=P(1+i)^N$

## Finding the present worth, P, given F, i, N
$P=F(1+i)^{-N}$
The factor $(1+i)^{-N}$ is referred to as the "present worth factor".
It is usually denoted as (P/F, i, N) and stated as "finding P given F, i, and N", i.e.,
$P=F(P/F,i,N)=F(1+i)^{-N}$

# Formula for finding F given A and vice versa
## 3.4.3 Compound interest formulae relating cash flows A and F
Cash flow diagram
![[CFD_FAFAIN.png]]
Note that the uniform periodic cash flows A start from period 1 and continue up to period N.

**Finding the future worth, F, of a uniform series cash flows, A, given i, and N**
The future worth is equal to the sum of the future worth of each individual A. By treating each individual A that occurs in period K, we can find its future worth by using the "compound amount factor" with the appropriate number of periods from k to N.
$F'=A(1+i)^{N-k}$
Summing the future worths of all the A's from $K=1$ to $K=N$, we get
$F=A(1+i)^{N-1}+A(1+i)^{N-2}+...+A(1+i)^{N-N}$
$=A\sum_{k=0}^{N-1}(1+i)^k$

This is a geometric series of the form { $a+ar+ar^2+ar^3+...+ar^N$}

The sum of a geometric series, $S_N$, is given as
$S_N=\frac{\text{first term}-\text{ratio}*\text{last term}}{1-\text{ratio}}$, where the geometric ratio, $r=\frac{1}{1+i}$.

Therefore:
# $F=A[\frac{(1+i)^N-\frac{1}{(1+i)}(1+i)^0}{1-\frac{1}{(1+i)}}]$
which simplifies to
# $F=A[\frac{(1+i)^N-1}{i}]$

The factor $[\frac{(1+i)^N-1}{i}]$ is referred to as the "**uniform series compound amount factor**" and is usually denoted as (F/A, i, N) and stated as "finding F given A, i, and N", i.e.,
# $F=A(F/A,i,N)=A[\frac{(1+i)^N-1}{i}]$

## Finding the uniform periodic worth, $A$, of a future cash flow, $F$, given $i$, and $N$
To find $A$ given $F$, $i$, $N$, take the inverse of the uniform series compound amount factor, i.e.,
# $A=F[\frac{i}{(1+i)^N-1}]$

The factor $[\frac{i}{(1+i)^N-1}]$ is referred to as the "**uniform series sinking fund factor**" and is usually denoted as $(A/F,i,N)$ and stated as "finding $A$ given $F$, $i$, and $N$", i.e.,
# $A=F(A/F,i,N)=F[\frac{i}{(1+i)^N-1}]$

# Formula for finding P given A and vice versa
## 3.4.4 Compound interest formulae relating cash flows A and P
Cash flow diagram
![[CFD_PAPAAIN.png]]
Note that the P is at period zero and the A's start from period 1 and end at $N$.
## Finding the present worth $P$, of a uniform of cash flows, $A$, given $i$, and $N$
Similar to the derivation of the future worth formula, the present worth is equal to the sum of the present worth of each individual A. By treating each individual A that occurs in period $k$, we can find its present worth by using the "present worth factor" with the appropriate number of periods from 1 to $k$, i.e.,

$P'=A(1+i)^{-k}$

Summing the present worths of all the $A$'s from $k=1$ to $k=N$, we get
$P=A(1+i)^{-1}+A(1+i)^{-2}+A(1+i)^{-3}+...+A(1+i)^{-N}$
Mulitply through by $(1+i)^{-1}$ (This is an alternative approach compared to the derivation of $F/A,i,N$ )
$P(1+i)^{-1}=+A(1+i)^{-2}+A(1+i)^{-3}+...+A(1+i)^{-N}+A(1+i)^{-N-1}$ 

Subtracting Eqn(2) from (1), all the middle terms disappear, i.e.,
$P-P(1+i)^{-1}=A(1+i)^{-1}-A(1+i)^{-N-1}$, which can be re-written as
$P[1-(1+i)^{-1}]=A[(1+i)^{-1}-(1+i)^{-N-1}]$

i.e.,

$P[1-\frac{1}{(1+i)}]=A[\frac{1}{(1+i)}-\frac{1}{(1+i)^N(1+i)}]$

Which simplifies to:
$P=A[\frac{(1+i)^N-1}{i(1+i)^N}]$

The factor $[\frac{(1+i)^N-1}{i(1+i)^N}]$ is referred to as the "**uniform series present worth factor**" and is usually denoted as $(P/A,i,N)$ and stated as "finding $P$ given $A$, $i$ and $N$", i.e.,
$P=A(P/A,i,N)=A[\frac{(1+i)^N-1}{i(1+i)^N}]$

# Formula for finding P given A: Special case when N = infinity
![[infinity.png]]
For $N=\infty$,

$P=A[\frac{(1+i)^N-1}{i(1+i)^N}]=A[\frac{1}{i}]=\frac{A}{i}$

This present worth when $N=\infty$, is known as "**<u>capitalized cost</u>**" "**<u>capitalized worth</u>**".

This also translates to
$A=Pi$ when $N=\infty$.

An intuitive translation of this is that if you invest an amount P and at the end of each period you just take out the periodic interest amount $P_i$, then that principal amount will last forever!!.

# Finding the uniform periodic worth, $A$, of an initial cash flow, $P$, given $i$, and $N$
To find $A$ given $P$, $i$, $N$, taking the inverse of the uniform series present worth factor results in,
$A=P[\frac{i(1+i)^N}{(1+i)^N-1}]$. This factor $[\frac{i(1+i)^N}{(1+i)^N-1}]$ is referred to as the "**uniform series capital recovery factor**" and is usually denoted as $(A/P,i,N)$ and stated as "finding $A$ given $P$, $i$ and $N$", i.e.,

$A=P[\frac{i(1+i)^N}{(1+i)^N-1}]$. This factor $[\frac{i(1+i)^N}{(1+i)^N-1}]$ is referred to as the "**uniform series capital recovery factor**" and is usually denoted as $(A/P,i,N)$ and stated as "finding $A$ given $P$, $i$, and $N$", i.e.,

$A=P(A/P,i,N)=P[\frac{i(1+i)^N}{(1+i)^N-1}]$

Note: Similar to present worth factor, if $N=\infty$, then the factor $(A/P,i,\infty)=i$

For $N=\infty$, $A=P(A/P,i,\infty)=Pi$

This means that an initial investment principal P can last forever if at the end of each period only the interest amount (Pi) is taken out, leaving the initial $P$ in the account forever.

# 3.4.5 Relationships between factors
Several relationships can be developed between factors derived above. To develop these relationships, consider the factors as analogous to fractions and use the simple rules of algebra to develop the relationships.