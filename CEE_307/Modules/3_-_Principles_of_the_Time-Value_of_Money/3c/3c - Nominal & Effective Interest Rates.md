- Typically, financial interest quote <u>annual interest rates</u>;
- However, interest may actually be compounded several times a year.
- For example, a credit card company may quote an annual interest rate of 18%, but they may compound the interest every month.
	- In that case, then, the company is actually charging an interest rate of 1$\frac{1}{2}$% per month, i.e., 18%/12.
	The the question becomes, what is the equivalent annual interest rate that is compounded once a year?
# Example - Suppose you want to invest $1,000 in a deposit account and you have two interest options to choose from:
- (1) Bank A offers you an annual interest rate of 9% and will compound the interest once at the end of <u>each year</u>.
- (2) Bank B offers you the same interest rate of 9% but they will compound the interest at end of <u>each month</u>. This means they are actually offering you an interest rate of 9%/12 = 3/4% per month.
Which is the more economical option for you?
# Solution - Calculate for each option, how much money will be in the account at the end of the first year., i.e.,
- Option (1), compounding will be done once a year, i.e.,
	- $F_1 = \$1,000(1+0.09)^1=\$1,090$
- Option (2), compounding will be done 12 times in the year, once every month at 3/4% monthly interest rate, i.e.,
	- $F_1=\$,1,000(1+0.0075)^12=\$1,093.81$
- Note that option (2) results in a higher future worth with an equivalent once-a-year interest rate of $i_e=(1,093.81-1,000)/1,000=9.381\%$.
This means that a "nominal" annual interest rate of 9% that is compounded monthly, i.e., 12 times a year, results in an "effective" annual interest t rate of $9.381\%$.

- Derivation of formula
	- Let r = "nominal" interest rate per year
	- m = number of compounding periods per year
	- $\rightarrow i=r/m=$ interest rate per year compounding period
- $i_e=$ "effective" interest rate per year
- $P=$ Initial principal
- $F=$ future worth at the end of $N$ years
- $N=$ total number of years
- $\rightarrow NM=$ the total number of compounding periods in N years.
Suppose we want to calculate F from an initial principal, P, we have two options to do that:
1. We can use compounding periods for analysis, in which we have $i=r/m$ per compounding period, and $Nm$ as the total number of periods. In this case, then,
		$F=P(1+i)^{Nm}=P(1+\frac{r}{m})^{Nm}$
2. We can use years as analysis periods, in which case we have $i=i$, per year over the $N$ years. In this case, then,
		$F=P(1+i_e)^N$
Since these F are supposed to be equal, then $F=P(1+i_e)^N=P(1+\frac{r}{m})^{Nm}$
Which reduces $(1+i_e)=(1+\frac{r}{m})^m$
And finally, the effective interest rate, $i_e=(1+\frac{r}{m})^m-1$

The effective interest rate, $i_e=(1+\frac{r}{m})^m-1$
Verify the formula using the previous example (option 2), i.e., r=9%; m=12;
Therefore, $i_e=(1+\frac{r}{m})^m-1=(1+\frac{0.09}{12})^{12}-1=9.381\%$

Note that when dealing with periodic cash flows, then
$r=$ nominal interest rate per cash flow period
$m=$ number of compounding periods per cash flow period, and
$i_e=$ the effective interest rate per cash flow period.

# Continuous compounding
Continuous compounding means that the number of compounding periods per cash flow period, $m=\infty$. 
Therefore, the effective interest rate,
	$i_e=lim_{m\rightarrow\infty}{(1+\frac{r}{m})^m}-1=e^r-1$ (refer to the notes for derivation of this)
i.e., Under continuous compounding
	$i_e=e^r-1$

- General rules for application of nominal and effective interest rates
	 In general, effective interest rate should be calculated and applied whenever <u>compounding is done more than once</u> within a cash flow period.
	 For example, if cash flows occure once a <u>year</b> but compounding is done <u>monthly</u>, then effective interest rate per <u>year</u> will be required and should be calculated based on an <u>annual</u> nominal interest rate, r, and 12 compounding periods per year, i.e., $m=12$.
	 Or, if cash flows occure once a <u>month</u> but compounding is done <u>daily</u>, then the effective interest rate will be calculated based on a <u>monthly</u> nominal interest rate, $r$, and $m=30$ compounding periods per <u>month</u>.
	 However, if cash flows and compounding occure at the same frequency, then there is no need to calculate the effective interest rate, because it is going to be the same as the nominal interest rate per cash flow period.
	 Below is a summary of the different situations in application of nominal and effective interest rates.
- <u>Case 1</u>: Compounding is done once every cash flow period, i.e., the frequency of cash flows is equal to the frequency of compounding:
	- In this case, there is <u>no need</u> for calculation of effective interest rate
	- The nominal interest rate per cash flow period should be used directly
	- For example, for a problem with <u>monthly</u> deposits and a nominal annual interest rate, r, with compounding being done <u>monthly</u>, then the nominal interest rate of r/12 <u>per month</u> should be used directly.
	- Note that in this example, the periods of analysis will be <u>months</u>.
- <u>Case 2:</u> Compounding is done less often than the occurrence of cash flows, i.e, cash flows occure more frequently than compounding:
	- In this case also, there is also <u>no need</u> for calculation of effective interest rate
	- The nominal interest rate <u>per compounding period</u> should be used directly, and the cash flows per compounding period will be equal to $A'=nA$, where
		- $A=$ cash flow per cash flow period, and
		- $n=$ number of cash flow periods per compounding period
	- For example, for a problem with <u>monthly</u> deposits, A, and a nominal annual interest rate, r, with compounding being done <u>quarterly</u> (i.e., once every three months), then the nominal interest rate of r/4 <u>per quarter</u> should used directly, with the corresponding <u>quarterly</u> cash flows of 3A (three months in a quarter).
	- Note that in this example, the periods of analysis will be <u>quarters</u>.
- <u>Case 3:</u> Compounding is more often than the occurrence of cash flows, i.e., compounding is done several times in each cas flow period:
	- In this case, the effective interest rate per cash flow period should be calculated, i.e.,
	The effective interest rate per cash flow period $i_e=(1+\frac{r}{m})^m-1$
	- Where, $r=$ is nominal interest rate per <u>cash flow period</u>, and
		$m=$ number of compounding periods per <u>cash flow period</u>
	- For exmaple, for a problem with <u>quarterly</u> deposits and a nominal annual interest rate, $r$, with compounding being done <u>monthly</u> (i.e., three times every quarter), then the effective inteerst rate per quarter will be based on a nominal interest rate of $r/4$ per quarter and m=3.
	Note that in this example, the periods of analysis will be <u>quarters</u>.
	- Note also that this case also applies when you have continuous compounding.