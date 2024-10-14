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
	 $i=1,200/1,000-1=0.20$, i.e., the IRR=20%

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

The "trial-and-error" process:
- First guess, $i=10\%\rightarrow$ Net PW = $\$2,000(P/A, 10\%, 10) + 3,500(P/F,10\%,10)-14,200=-\$561$
The next guess should be an interest rate that should result in a ==positive net PW==. This means the interest rate that would make PW of the revenues higher.
To achieve this, we have to pick an interest rate lower than 10\% which will make the factors P/A and P/F greater than at 10\%. In this case 8\% is selected, i.e.,
- at $i=8\%\rightarrow$ net PW = $\$2,000(P/A,8\%,10)+3,500(P/F,8\%,10)-14,200=+\$841$.
Therefore, at 10\%, net PW = -\$561 and at 8% net PW = +\$841
- This means that the IRR is between 8\% and 10\%, and its approximate value can be obtained by linear interpolation between the two.

The interpolation process: The results obtained can be represented with a diagram.
![[Example 3.png]]
Using the property of similar triangles,
$\frac{x_1}{h_1}=\frac{x_1+x_2}{h_1+h_2},\rightarrow x_1=h_1\frac{x_1+x_2}{h_1+h_2}$
Then
- IRR = $8\%+x_1$
In this case,
- $h_1=841$
- $h_1+h_2=841+561$
- $x_1+x_2=10\%-8\%$
Therefore
- IRR = $10\%+x_1=10\%+h_1\frac{x_1+x_2}{h_1+h_2}=8\%+841\frac{10\%-8\%}{841+561}=9.20\%$ (Note that the exact value is 9.16\%)
# How to make "good guesses" of the interest rates for interpolation
- There are no hard and fast rules on how to determine good initial guesses of the interest rates.
- This means one may have to try several interest rates before getting the two suitable ones for interpolation, i.e., ones that give positive and negative present worth values close to zero.
- However, it should be noted that, since the actual relationship between the PW and interest rate is non-linear, and therefore linear interpolation introduces an error in the estimated value of the IRR.
![[Linear Interpolation Error.png]]
Things to consider about this error
- The bigger the difference between $i_A$ and $i_B$, the greater the error will be.
It is therefore important that the range between the two interpolated interest rates be kept as small as possible in order to minimize the error.

# Potential for multiple unique solutions for IRR
- One of the major shortcoming of the IRR method, is the potential existence of **multiple values of IRR** for a given investment or set of cash flows.
- The rule of thumb for possible existence of multiple unique values of IRR states that "<u>there may be as many unique values of IRR as the number of sign reversals</u>" in the cash flow diagram for the investment. A sign reversal is anytime there is a change in the sign of the cash flows either from negative to positive (i.e., cost to revenue cash flow) or vice versa as you go from one period to the next. This example here has two sign changes, hence may have two unique value of IRR.
![[Multiple values of irr.png]]
- This figure is actually from Example 4 in the module 4b notes, and the IRR solutions are 5.6% and 36.5%. There is no way of determining which of the two values is the correct IRR for this investment.
- There are techniques for handling this problem, but they are beyond the scope of this course (NOT IN TEST).

# Use of the IRR for Economic Evaluation
- <u>Evaluating a Single Alternative</u>
	- Evaluation of a single investment alternative essentially means comparing the alternative to the "Do Nothing" alternative, that is typically represented by the MARR. Therefore,
		- If the IRR $\ge$ MARR, the investment is economical, since its rate of return is higher or equal to the minimum acceptable.
		- If the IRR $<$ MARR, then the investment is not economical.
- <u>Evaluating Multiple Mutually Exclusive Alternatives</u>
	- In general, the individual IRR values of alternatives should <u>not</u> be used to determine which of mutually exclusive alternatives is the most economical. The IRR simply indicates whether or not an individual alternatives is economical.
	- To determine which of the mutually exclusive alternatives is the most economical, an **incremental analysis of the IRR has to be performed**.
# Comparing more than two alternatives using the incremental IRR method
This method involves iterative pairwise comparison of alternatives until the most economical alternative is identified. The following are the 5 steps involved:
1. Compute the rate of return (IRR) of each alternative. Any alternative with IRR < MARR should be rejected outright. Note that for "cost only alternatives", this step cannot be done, incremental analysis should start in step 2.
2. Arrange the remaining alternatives **in order of increasing initial investment**. The alternatives with the lowest initial investment cost will be the first one to be compared against and is referred to as the "**base alternative**".
3. Perform an incremental IRR analysis between the **higher cost alternative** with the **current base alternative**. Perform the following check:
	- If the **incremental IRR $\ge$ MARR**, **"accept" the higher cost** alternative, and make it the **new base alternative** for the next step.
	- If the **incremental IRR $<$ MARR**, "reject" the higher cost alternative and keep the **current base alternative**.
4. Go to the next higher cost alternative, and repeat Step 3.
5. Repeat Steps 3 and 4 until all alternatives have been evaluated. The selected **base alternative in the last iteration** is the most economical alternative.
![[3 conditions.png]]