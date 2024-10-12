Another method for making economic evaluations and comparisons of alternatives.
1. Definition of IRR
2. Calculation of the IRR for an investment alternative
3. Economic analysis using IRR
	- Evaluation of one alternative
	- Comparison of mutually exclusive alternatives

# Definition of Internal Rate of Return (IRR)
The IRR is the interest rate which the <u>net worth</u> of all the cash flows for an investment alternative over its study period is equal to <u>zero</u>. In other words, it is the *break-even* interest rate, i.e.,
At $i=IRR$
	Net PW = PW(revenues) - PW(costs) = 0, or
	Net AW = AW(revenues) - AW(costs) = 0, or
	Net FW = FW(revenues) - FW(costs) = 0.
- An investment is <u>economical</u> if its IRR $\ge$ MARR.
- An investment is <u>not economical</u> if its IRR $<$ MARR and should normally be rejected.

# Calculation of the IRR
To determine its IRR for a typical investment with uniform periodic cash flows (see the cash flow diagram), one has to find the interest rate, $i$, such that
![[IRR.png]]
Net PW = PW(Periodic Revenues - Costs) + PW(Salvage Value) - Initial Cost = 0
- $=(A_R-A_C)(P/A,i,N)+S(P/F,i,N)-P=0$
- The calculation process normally involves an iterative or trial-and-error procedure.

# Example 1
Calculating the IRR for an initial investment P with a future value F.
If you invest \$1,000 now and expect to be paid back a total of \$1,200 after exactly 1 year, what IRR will you have earned on the investment?
<u>Solution:</u>
The IRR is the interest rate, $i$, such that
Net PW = PW(Revenues) - PW(Costs) = 0, i.e.,
- $\$1,200(P/F, i,1)-1,000 = 0$
- $\$1,200(1+i)^{-1}-1,000=0$
Then $(1+i)=1,200/1000$
And therefore
	- $i=1,200/1,000-1=0.20$, i.e., the IRR=20%

# Example 2
The "trial-and-error" method with one compound interest factor.
Mark invested \$20,000 on a business venture that is expected to bring him uniform annual revenues of \$4,800 for each of the 6 years that the business will last. What internal rate of return (IRR) does this investment generate?
Solution:
Again, the IRR is the interest rate, $i$, such that
Net PW = PW(Revenues) - PW(Costs) = 0, i.e.,
- $\$4,800(P/A,i,6)-20,000 = 0$
- $\$4,800(\frac{(1+i)^6-1}{i(1+i)^6})-20,000=0$
This is a difficult equation to solve for $i$ analytically. Therefore, a trial-and-error process is normally used for this.

Using the factor notation, instead of the detailed expression for the factor, we have
- $\$4,800(P/A,i,6)-20,000 = 0$
Then, the factor
- $(P/A,i,6)=20,000/4,800=4.1667$
Then, by going over the compound interest tables in the textbook or some other source, we have to look for the two interest rates whose values for factor (P/A, **i**, 6) are the closest <u>above</u> and <u>below</u> 4.1667.
In this case, from the tables (shown in video), we will find that
at $i=10\%$, the factor (P/A,i,6) = 4.3553 (closest value higgher than 4.1667).
at $i=12\%$, the factor (P/A,i, 6) = 4.1114 (closest value lower than 4.1667).
This means thath the IRR is between 10% and 12%.

Then by graphing the relationship between the factor (P/A,i,N) and the interest rate i, the IRR can be estimated by *linear interpolation* using the geometry, i.e.,
![[example 2.png]]
Using the property of similar triangles,
$\frac{x_1}{h_1}=\frac{x_1+x_2}{h_1+h_2}$, and therefore
$x_1=h_1\frac{x_1+x_2}{h_1+h_2}$
and IRR = 10% + $x_1$
In this case, 
- $h1=4.35533-4.1667$
- $h1+h2=4.3553-4.1114$
- $x_1+x_2=12\%-10\%$
Therefore
- IRR$=10\%+x_1=10\%+h_1\frac{x_1+x_2}{h_1+h_2}=10\%+(4.3553-4.1667)\frac{12\%-10\%}{4.3553-4.1114}=11.54\%$

# Example 3
The "trial-and-error" method with more than one compound interest factors.
Mark invested \$14,200 on a business that made net annual revenues of \$2,000 for 10 years, and a salvage value \$3,500 at the end of the $10^{th}$ year. What average annual IRR did the investor earn on the investment?
<u>Solution:</u>
The IRR is the interest rate, $i$, such that
Net PW = PW(Revenues)-PW(Costs)=0, i.e.,
- $\$2,000(P/A,i,10) + 3,500(P/F,i,10)-14,200=0$

In this case, there are two compound interest factors, P/A and P/F, in the equation. This means that the method presented in Example 2 above cannot be used, since it only works if there is one factor.

Therefore, a purely a *trial-and-error process* is used that involves guessing and checking different interest rates. Normally two guesses of **i** are made, one that gives a positive Net PW closest to zero, and the other that gives a negative Net PW closest to zero.
Then the approximate IRR is obtained by *linear interpolation* between the two.
