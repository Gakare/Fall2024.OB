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
- The *concept of equivalence enables on to compare the "values" of cash flows that occur at different points in time.
- These could be single cash flows at different points in time, or a series of cash flows over several periods
- The following two examples illustrate this concept
## Example 4A: Present Worth and Future Worth concepts
If you invest $2,000 today in an account that earns an interest rate 5% per year, how much mony will you have in the account after 4 years?
	$F_N=P(1+i)^N=\$2,000(1+0.05)^4=\$2,431$
Then, using the concept of equivalence, the following statement can be made regarding this scenario:
	The $2,000 you have today is __*equivalent to*__ the $2,431 that you can have 4 years from now. In other words you would be indifferent between the choice of having $2,000 today or waiting to get $2,431 four years from now.
You can also make the following alternative statements:
	$2,431 is the 4-year __*future worth*__ of today's $2,000; or alternatively,
	$2,000 is the __*present worth*__ of a 4-year future $2,431 cash flow.