Video: https://www.youtube.com/watch?time_continue=2&v=TZxA0X1dIc4&embeds_referring_euri=https%3A%2F%2Fplugin.3playmedia.com%2F&source_ve_path=MjM4NTE
These are the last two methods for economic evaluations and comparisons that are going to be presented in this class.

This first part of the lecture presents the B/C Ratio Method as follows:
1. Definition of B/C Ratio for an investment alternative
2. Calculation of the B/C Ratio
3. Economic analyses using B/C Ratios
	- Evaluation of one alternative
	- Comparison of mutually exclusive alternatives
# Definition of B/C Ratio
- The "Benefit/Cost Ratio" is the ratio of the present worth of the revenues to the present worth of the costs over the service life of an investment at the given value of MARR, i.e,
	- $B/C=\frac{PW(Benefits)}{PW(Costs)}$
- The calculation can alse be defined in terms of the equivalent AW or FW values, i.e.,
	- $B/C=\frac{AW(Benefits)}{AW(Costs)}$
	- $B/C=\frac{FW(Benefits)}{FW(Costs)}$
There are two definitions of the B/C ratio:
- The "<u>Conventional</u> B/C Ratio": For a given investment with uniform periodic cash flows (see cash flow diagram)
	- Conventional B/C $=\frac{PW(\text{Gross Benefits})}{PW(Costs)}=\frac{A_R(P/A,i,N)}{P+A_C(P/A,i,N)-S(P/F,i,N)}$
Note that the salvage value, $S$, though it may be a revenue, it is considered part of the initial investment cost.
Therefore, if the salvage value is a revenue, it is considered as a reduction in the investment cost by subtracting its PW from the initial cost, $P$, hence the negative sign in the denominator.
- On the other hand, the "<u>Modified</u> B/C Ratio" is defined as
	- Modified B/C $=\frac{PW(\text{Net Benefits})}{PW(\text{Investment Costs})}=\frac{(A_R-A_C)(P/A,i,N)}{P-S(P/F,i,N)}$
- Note that the calculations are done at $i=MARR$.
- Note also that an ==investment is considered economical== if the B/C Ratio $\ge 1$ because it means that the PW(Benefits) $\ge$ PW(costs).
# Use of the Benefit-Cost Ratio for Economic Analysis
Using the B/C Ratio for Economic Evaluation
- <u>Evaluating a Single Alternative</u>
	- Evaluation of a single investment alternative essentially means comparing the alternative to the "Do Nothing" alternative, that is typically represented by the MARR. Therefore,
		- If the B/C Ratio $\ge1$ at the value of MARR, then the investment is economical, since that means that the Net PW(Revenues) $\ge$ Net PW(Costs).
		- If the B/C Ratio $<1$, then the investment is not economical.
- <u>Evaluating Multiple Mutually Exclusive Alternatives</u>
	- In general, the individual B/C Ratios of alternatives should <u>not</u> be used to determine which of mutually exclusive alternatives is the most economical. The B/C ratio simply indicates whether or not an individual alternative is economical.
	- To determine which of the mutually exclusive alternatives is the most economical, an **incremental analysis using the B/C ratios has to be performed**.

Comparing multiple mutually exclusive alternatives using B/C ratio incremental analysis
- <u>Evaluating two alternatives</u>
- To determine which one of two alternatives is more economical, the following procedure should be followed.
	- **Step 1**: <u>Calculate the B/C ratio of each alternative at the value of MARR</u>. If any alternative has B/C $<1$, it can be <u>rejected outright</u>, otherwise go to Step 2. This step is skipped if dealing with cost-only alternatives.
	- **Step 2**: Rank the <u>alternatives in order of the values of the denominator</u> of the B/C ratio. The one with the <u>higher value</u> is considered the <u>higher ranked alternative</u>. For <u>cost-only alternatives</u>, the ranking should be based on the <u>initial investment and salvage value</u>.
	- **Step 3**: Calculate the <u>incremental cash flows</u>, subtracting the cash flows of the lower ranked alternative from those of the higher ranked one.
	- **Step 4**: Calculate the <u>B/C ratio of the incremental cash flows</u>. The objective here is to determine whether or not the <u>additional expenditure in the higher ranked</u> alternative produces incremental revenues that result in an incremental B/C ratio $\ge1$. Therefore,
		- If the incremental B/C Ratio $>1$, then the <u>higher</u> rakned alternative is more economical.
		- If the incremental B/C Ratio $<1$, then the <u>lower</u> ranked alternative is more economical.
		- If the incremental B/C Ratio $=1$, then the two alternatives are <u>economically equivalent</u>.
Note that all the B/C ratios are calculated at the interest rate equal to MARR.
Comparing multiple mutally exclusive alternatives using B/C ratio incremental analysis
- <u>Evaluating more than two alternatives</u>
- To determine which one of several alternatives is the most economical, a procedure that involves iterative pairwise comparisons is used. This procedure is similar to that of the IRR method and is as follows.
- **Step 1**: Calculate the <u>B/C ratio of each</u> alternatives at the value of MARR. If any alternative has B/C $<1$, it can be rejected outright, otherwise go to step 2. This step is <u>skipped if dealing with cost-only alternatives</u>.
- **Step 2**: Rank the <u>alternatives in order of the values of the denominator</u> of the B/C ratio. The one with the highest value is ranked the highest and the one with the lowest value is ranked the lowest. For <u>cost-only alternatives</u>, the ranking should be based on the initial investment and salvage value.
- **Step 3**: This step is repeated several times (i.e., <u>"iterations"</u>), and at each iteration, an <u>incremental B/C</u> analysis between the <u>base alternative</u> and a <u>higher ranked</u> alternative is <u>performed</u>.
	- For the first iteration, the base alternative is going to be the <u>lowest ranked alternative</u>, and it is going to be compared to the <u>next higher ranked alternative</u>. This procedure is similar to the incremnetal IRR procedure. Here are the sub-steps:
		- <u>Calculate the incremental cash flows</u> between the two alternatives;
		- Hence, <u>calculate the corresponding incremental B/C ratio</u>, and perform the <u>following</u> analysis:
			- If the **incremental B/C $\ge1$**, the **higher ranked** alternative is more economical and it becomes the **new base alternative** for the next iteration; the <u>lower ranked</u> alternative is <u>rejected</u>;
			- If the **incremental B/C $<1$**, the base (i.e., lower ranked) alternative is <u>more economical</u> and remains as the <u>base alternative</u> while the higher ranked alternative is rejected.
- **Step 4**: Go to the next <u>higher ranked alternative</u>, and repeat Step 3.
- **Step 5**: Repeat <u>Steps 3 and 4</u> until all alternatives have been evaluated. Then the <u>more economical alternative</u> in the last iteration is the <u>most economical alternative</u>.
# Second Part
This is the second of a two part lecture and presents the Payback Period Method for economic evaluation.
1. Definition of Payback Period for an investment alternative
2. Calculation of the Payback Period
3. Economic analyses using Payback Period
# Definition of the Payback Period
- Payback period is the minimum number of periods required to <u>recover the initial investment</u> for a given project
- There are two definitions of payback period, namely,
	(1) the <u>simple payback</u> period, which <u>ignores</u> the interest rate, and
	(2) the <u>discounted payback</u> period, which does <u>take into account</u> the interest rate.

# Simple Payback Period
This definition of payback period ignores the interest rate. If Np is the number of periods it will take to recover the initial investment, $P$, then, given the periodic revenues and cost, $A_R$ and $A_C$.
- Total cumulative revenues after Np periods = Initial investment, $P$.
i.e.,
- $N_P(A_R-A_C)=P$
Therefore, the simple payback period,
- $N_p=\frac{P}{A_R-A_C}$
For non-uniform periodic cash flows, the simple payback period $N_p$ is the minimum period such that the cumulative net revenues are at least equal to $P$, i.e.,
- $\sum_{k=1}^{N_P}(A_{Rk}-A_{Ck})\ge P$
where
- $A_{Rk}$ and $A_{Ck}$ are the revenue and cost for period $k$, respectively.
The solution for this can be obtained graphically as shown in the accompanying figure.
The example in the figure is for $P=\$2,500$ which results in $N_P\approx 7.8$ periods.
![[Payback Graph.png]]
# Discounted Payback Period
This definition takes into account the interest rate. If $N_P$ is the number of periods it will take to recover the initial investement, $P$, then,
- Total cumulative present worth revenues after $N_P$ periods = Initial investment, P
i.e.,
- $(A_R-A_C)(P/A,i,N_P)=P$
This leads to
- $(P/A,i,N_P)=\frac{P}{(A_R-A_C)}$
Substituting the expression for $(P/A,i,N_P)$ we get
- $(\frac{(1+i)^{N_P}-1}{i(1+i)^{N_P}})=\frac{P}{(A_R-A_C)}$
Which reduces to $N_P=\frac{ln(A_R-A_C)-ln(A_R-A_C-Pi)}{ln(1+i)}\rightarrow$ The discounted payback period.
If the periodic cash flows are non-uniform, then the discounted payback period is the minimum value of Np that satisfies the following relationship for the cumulative present worth of the net revenues, i.e.,
- $\sum_{k=1}^{N_P}(A_{Rk}-A_{Ck})\times(P/F,i,k)\ge P$
where $A_{Rk}$ and $A_{Ck}$ are the revenue and cost for period $k$, respectively.

Similar to the simple payback period, this can be determined graphically, in this case from a graph of the cumulative net <u>present worth</u> as a function of $k$.
# Significance of the Payback Period
- When the payback period is used for economic analysis, the objective is normally to recover the initial investment as quickly as possible or within a desired timeframe.
- Although the discounted payback period is the more appropriate one to use, the simple payback period is sometimes used for quick comparison between alternatives because it is easy to calculate.
- When comparing mutually exclusive alternatives using this method, the alternatev with the **shortest payback period** would normally be preferred.
- However, it should be noted that the alternative with the shortest payback period <u>may not</u> necessarily be the most economical one over the entire service lives or study period.
The reason being that the payback period does <u>not</u> consider all the cash flows over the entire service life, it **ignores all the cash flows beyond the payback period**.
For example, an alternative with the shortest payback period may have significantly lower revenues than the competing alternative beyond the payback period, resulting in a lower net PW over the service life compared to the competing alternative.
# Example 7 (08:21)
(Note: The example numbers match with the examples in Module 4c notes)
A project that requires an initial investment of \$1,000,000 is expected to generate gross annual revenues of \$410,000 annual costs of \$100,000 over its projected service life of 8 years. The salvage value at the end of its service life is expected to be \$200,000. Calculate both the simple and discounted payback periods, given a MARR of 12% per year.
**Solution (09:29)**
# Example 9: Using the payback period to compare mutually exclusive alternatives (11:57)
For the following three mutually exclusive alternative equipments, select the preferred equipment based on a MARR of 16% per year using
(a) The discounted payback period method
(b) The PW method.
**Solution (12:54)**
