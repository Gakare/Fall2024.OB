Video: https://www.youtube.com/watch?v=bRpAJ1O2CTQ
<u>Presents</u>
- Methods of handling uncertainty in the estimated values of input parameters of alternatives when performing economic analysis.
#  Sources of uncertainty in the input data
- Most of the uncertainty is due to the difficulties in obtaining accurate estimates of <u>future cash flows</u> and/or <u>occurrence of events</u>. This is particularly true for
	- Analysis involving <u>long study periods</u>
	- Analysis involving <u>new activities</u>, <u>products</u> or <u>services</u>
	- Analysis of <u>big projects</u> involving several interacting activities and project objectives
	- Analysis of <u>projects involving occurrence</u> of natural events, such as earthquakes, rainstorms, etc.
Uncertainty in the input data may be in the form of
- <u>Probability, or probability distributions</u>, of
	- occurrence of events
	- estimated values of inputs paramaters
- Range of estimates, i.e.,
	- most likely values
	- optimistic values (i.e., under best case scenarios)
	- pessimistic values (i.e., under worst case scenarios)
These range of estimates may or may not have associated probabilities of occurrence
# Examples of statements that describe uncertainty in input data
- Probability distribution:
	- The annual revenue for an investment is expected to be <u>normally distributed</u> with a mean of <u>\$450,000</u> and a standard deviation of <u>\$60,000</u>.
- Probability of occurrence:
	- Possible market values of an asset at the end of its service life are as follows: \$50,000 at a <u>probability</u> of 50%; \$60,000 at 30% <u>probability</u> and \$70,000 at 20% <u>probability</u>.
	- Note that since these are mutually exclusive outcomes, the sum of the probabilities is equal to 1.
- Range of estimates
	- The service life of a new equipment is uncertain. It is most likely going be 6 years, although it could be as long as 10 years or as short as 4 years.
	- Note that the lowest estimate, i.e., the 4 years is referred to as the "pessimistic" estimate, while the highest estimate (the 10 years) is the "optimistic" estimate.
# Methods of Analysis
- Designed to enable incorporating the uncertainty in input data when performing economic analysis of investments and/or projects.
- Methods presented
	1. Expected values method
		- Includes a brief discussion of "decision trees"
	2. Range of estimates method
	3. Breakeven analysis
	4. Sensitivity analysis
# Method of Expected Values
- In this case, <u>each input variable that is subject</u> to uncertainty will have several possible values or outcomes each assigned with a <u>probability of occurrence</u>.
- Analysis is then based on the "expected" values of such variables based on the laws of probability, i.e., the "expected" value of a variable that is subject to several possible outcomes,
	- $=\sum_{j=1}^{N}\{\text{prob}(\text{outcome}_j)\times\text{value}(\text{outcome}_j)\}$
	Where N is the total number of possible outcomes, and
	- $\sum_{j=1}^{N}\{\text{prob}(\text{outcome}_j)\}=1$
# Example:
- Possible market values of an asset at the end of its service life are as follows: \$50,000 at a probabiltity of 50%; \$60,000 at 30% probability and \$70,000 at 20% probability.
- Calculate the "expected" market value of the asset.
**Solution**
(8:05)
# Example 3a (09:46)
- A homeowner is planning to buy fire insurance for her new \$200,000 home. After much research, the lowest insurance premium she found was for \$580 per year. To check whether the premium is reasonable or not, the homeowner decided to get more information on the risk of fire damage for the home. The local fire department provided her with the following annual probabilities for fire loss in any year
**Solution (12:50)**
- To evaluate whether the quoted premium is reasonable or not, we calculate the "expected" annual cost of fire damage based on probabilistic data given, and compare it to the premium.
- Note that here we have four possible "outcomes", i.e., levels of fire damage in any given year, and their associated probabilities of occurrence.
- Hence, expected annual cost of fire damage
Note that the solution shows that
- The annual insurance premium (\$580) is higher than the expected annual cost of fire damage (\$420).
- From the <u>insurance company's point of view</u>, the company will spend an average of \$420 per year per home, and that differenc between the premium and expected fire loss is the revenue necessary for the company to cover <u>administrative and operating costs</u> as well as make a <u>profit</u>.
- From the <u>point of view of the homeowner</u>, the choice is between
1) <u>Not buying insurance</u> and <u>risking having to spend huge sums of money</u>, that the homeowner may not afford, when a fire occurs, or
2) <u>buy insurance</u> and be willing to <u>pay premium</u> that is higher than the expected annual fire damage in order to <u>transfer the risk of potential future higher costs</u> of fire damage to the insurance company.
# Example 4 (17:47)
- Deciding on an economical level of protection to provide for a city against flooding due to hurricanes by building levees.
- There are five alternatives being considered, each corresponding to the level of hurricane, i.e.,
 ![[Example 4.png]]
- Property damage in case of overflow = \$100,000,000;
- If the design life of the levees is 50 years, and MARR = 8%, which of the five hurricane category protection levels is the most economical?
**Solution (20:08)**
- Note the <u>trade-off</u> between the construction cost of the levees and the probability of flooding, i.e., the higher the level of protection, the higher the construction cost, but the lower the probability of flooding, hence, the lower expected cost of flooding; and vice versa.
- Therefore, the most economical protection level is the one that will minimize the total costs that include the construction cost of the levees and the expected flood damage costs.
- For a given level of protection j, the <u>equivalent uniform annual cost</u>
	- EUAC(j) = (construction capital recovery cost) + (expected annual flood cost)
			 = (construction cost)(A/P,i,N) + (Probability of flooding)(Flood cost)
			 = $P_j$(A/P,i,N) + $C_F$Prob(j)
Where
	 $P_j$ = the initial construction cost for hurricane category j protection
	 Prob(j) = probability of flooding under hurricane category j protection
	 $C_F$ = cost of flooding when it occurs
Calculations: For hurricane category 5 protection,
	EUAC(5) = \$70,000,000(A/P, 8%, 50) + \$100,000,000(0.01)
			 = 70,000,000(0.0817) + 100,000,000(0.01) = \$6,719,000
The rest of the calculations are summarized below
![[Example 4 Summary Table.png]]
- Additional questions: Discuss, without doing any calculations, whether you are likely to recommend *higher* or *lower* hurricane category protection for the following situations:
a) Lower flood cost of only \$70,000,000 every time flooding exceeds levee height,
b) A higher MARR value, say 15%
- Verify your answers by doing the calculations for each case.

# Decision Trees
- A "decision tree" is an analysis tool that breaks-down a complex problem into a <u>tree-like diagram</u> that consists of <u>nodes</u> and <u>branches</u>.
- For an engineernig economics problem, a decision tree would typically <u>consist of three types of nodes</u>
1) A <u>decision node</u> that identifies mutually exclusive alternatives from which one has to be selected. Each branch for a decision node represents one of the alternatives to be considered.
2) <u>Chance nodes</u> that identify the possible outcomes of each alternative. Each branch from a chance node represents one possible outcome of an alternative. These possible outcomes may have specified probabilities of occurrence.
3) <u>Outcome nodes</u>, are nodes that identify and/or calculate the outcome of branches of chance nodes. However, outcome nodes are not always present.
# Example 3b Using Decision Trees
Solve earlier Example 3a, the fire insurance example, by representing the problem as a decision tree, under the following <u>modification</u> to the problem:
	$\rightarrow$ The homeowner will be charged a \$1,000 deductible whenever he/she files an insurance claim for fire damage.
- The analysis is from the homeowner's point of view. The two alternatives are:
1. Buy insurance and pay \$580 in annual premium; will be requird to pay a \$1,000 deductible whenever filing a claim for fire damage
2. Self insure (i.e., do not buy insurance); pay for the fire damage from own pocket.
- The <u>decision tree</u> will consist of
	- A decision node with two branches, one for each of the two alternatives.
	- Each branch from the decision node will have a chance node each with the four possible outcomes.
![[Decision Tree 3b Example.png]]
- Expected outcome (Buy Insurance)
	- = \$580 + 0.986(\$0) + 0.010(\$1,000) + 0.003(\$1,000) + 0.001(\%1,000) = \$594
- Expcted outcome (Self insure)
	- = \$0 + 0.986(\$0) + 0.010(\$10,000) + 0.003(\$40,000) + 0.001(\%200,000) = \$420
# Range of Estimates
- In this case, three estimates are typically given for the value of an uncertain parameter of interest, namely, the ==most likely value== (M), the ==optimistic value== (O), i.e., the value based on the best case scenario, and the ==pessimistic value== (P), i.e., the value based on the worst case scenario.
- The value ==may or may not== have corresponding estimates of the probabilities of occurrence.
- The expected value for a variable with such data, can be calculated using either one of the following three methods
1. The <u>simple average of the three estimates</u>
2. Using the "<u>three point estimation</u>" technique which gives <u>more weight to the most likely value</u> than the extreme estimates, i.e.,
	- Expected value = $\frac{0+4M+P}{6}$
3. Using probabilities of occurrence for O, M and P estimates, if they are provided, i.e., Expected value = O $\times$ (prob(O)) + M $\times$ (prob(M)) + P $\times$ (prob(P))
Where
	prob(O), prob(M), and prob(P) are probabilities of occurrence of the O, M, and P estimates
- In the absence of probability information, the <u>preferred method</u> is the **three point estimation**.
# Example 5 (39:10)
Two alternatives are being evaluated for construction of a highway bridge that is projected to require 4 lates in the near future to handle projected traffic.
- Alternative 1: One-stage construction: Construct a 4-lane bridge now at a cost of \$5 Million;
- Alternative 2: Two-stage construction: Construct a 2-lane bridge now for \$3 Million, and widen to 4 lanes 5 years from now. There are 3 estimates for the future construction cost of widening in year 5:
	- Most likely = \$2,900,000
	- Optimistic = \$2,600,000
	- Pessimistic = \$3,600,000
Adding information: Annual maintenance cost for 2-lane bridge is \$100,000 and for 4-lane bridge \$160,000.

Which of the two alternatives should be recommended given a MARR of 6% per year?
**Solution (41:51)**
- Compute and compare the PW of the two alternatives. Note that the analysis period here is only 5 years, since the two alternative are identical after 5 years.
Alternative 1: One stage construction: 4 lane bridge right away
- Construction cost now = \$5,000,000
- Maintenance cost (4 lane) = \$160,000 per year
- Hence, PW = -\$5,000,000 - 160,000(P/A, 6%, 5) = -\$5,673,978
Alternative 2: Two stage: 2 lanes now, widen to 4 in year 5
- Construction cost now (2 lane) = \$3,000,000
- Maintenance costs = \$100,000 per year (2 lanes to year 5)
- Cost of widening bridge in the $5^{th}$ year has the three range of estimates, therefore, using the three-point estimation technique the expected cost of widening in year five
$= \frac{2,600,000 + 4(2,900,000)+3,600,000}{6}=\$2,966,667$
Hence, present worth, PW $= -\$3,000,000 - 2,966,667(P/F,6\%,5) - 100,000(P/A, 6\%, 5) = -\$5,638,102$
Now compare the two PW cost between alternative 1 and 2.
- We see that alternative 1 > alternative 2 and so it would be more economical to choose alternative 2 because this is in the context of cost.
![[Example 5 Solution.png]]