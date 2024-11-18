# Definition - Inflation
It is the increase in prices of goods and services over time.
- The effect of inflation is to decrease in the purchasing power of the monetary currency (such as the dollar) over time, meaning that you have to pay more for the same service and/or goods as time goes by.
- Inflation is typically measured as the average percentage change in price (or cost) per unit of time.
- Negative inflation, i.e., when prices decrease over time, is known an "deflation".
# Calculation of Inflation Rates
Let
- $P_B=$ Price in base period, $B$
- $P_F=$ Price in the future period, $F$
- N = The number of periods (= F - B)
Then, the average inflation rate per period over the N periods,
- $f=(\frac{P_F}{P_B})^{1/N}-1$,
Therefore, given an inflation rate and base price, the future price after N Periods,
- $P_F=P_B(1+F)^N$
# Inflation Rates
<u>The Consumer Price Index (CPI)</u>
- It is a composite measure of changes of prices of consumer goods and services over time in the USA
- The CPI is a normalized value that represents the prices of selected goods and services that an "average" American consumer needs for their daily life.
- As prices of these goods and services increase/decrease over time, the CPI values also increases/decreases proportionally.
- Percentage change in the CPI value is used as a measure of the general inflation rate for the consumer goods and services.
- The CPI values are calculated, updated and maintained by th US Bureau of Labor and Statics (BLS)
- The following table is a partial list of urban CPI values that were downloaded from the BLS website.
- The complete list was from 1908-2020 by month.
![[CPI.png]]
# Calculation of Inflation Rates
Calculation of the general inflation rate based on CPI values
Let
- $CPI_B = CPI$ value for the base year B,
- $CPI_F = CPI$ value for the future year F,
	- $N = F - B$, this is number of years.
The average annual inflation rate in that time period,
- $f=(\frac{CPI_F}{CPI_B})^{\frac{1}{N}}-1$
# Cash Flow Terminologies in Inflation Analysis
- There are two definitions of cash flows designed to distinguis between cash flows that have been adjusted for inflation (typically known as "real dollars") from those thta have not been adjustet for inflation (typically known as "actual dollars").
	- **Actual dollars** (A\$): The actual number of dollars associated with a a cash flow (or a non-cash flow amount such as depreciation) as of the time it occurs. Also known as *nominal dollars*, *current dollars*, *then-current dollars*, and *inflated dollars.*
		- nominal dollars
		- current dollars
		- then-current dollars
		- inflated dollars
	- **Real dollars** (R\$): Dollars expressed in terms of the same purchasing power relative to a particular time. Also refererred to as *today's dollars*, *year zero dollars*, *constant dollars*, or *inflation-free dollars*.
		- today's dollars
		- year zero dollars
		- constant dollars
		- inflation-free dollars
- Relationship between "actual dollars" and "real dollars":
	- Actual \$ = (Real \$)$(1+f)^N$
	or
	- Real \$ = (Actual \$)$(1+f)^{-N}$
Where
- $f=$ average annual inflation rate per over the N years
- $N=$ the number of years from the base year to the future year
# Cash Flow Terminologies in Inflation Analysis
- Two additional definitions:
<u>Market interest rate</u> ($i_m$): The actual interest rate paid on borrowed money or the actual interest rate earned on an investment that is based on actual dollar cash flows. It is the interest rate you will normally see in the day-to-day transactions and financial statements. It is also sometimes called the <u>nominal</u> or <u>combined</u> interest rate.

<u>Real interest rate</u> ($i_r$): The interest paid on borrowed money or interest earned on investment that is based on constant purchasing power of the dollar, meaning, it is based on real dollar cash flows. It is the interest rate that would be calculated once all the cash flows are converted into real dollars. It is sometimes also called the inflation-free interest rate.

- Relationship between market interest rate ($i_m$) and real interest rate ($i_r$):
	- $i_m=i_r+f+i_r\times f$
- or
	- $i_r=\frac{i_m-f}{1+f}$
(For derivation, refer to the notes)
# Guidelines for Economic Analysis with Inflation Consideration
Between $i_r$ and $i_m$, when should each be used?
- If the cash flows are in <u>actual dollars</u>, analysis should use the <u>market interest rate</u>, $i_m$.
- If the cash flows are in <u>real dollars</u>, then the real <u>real interest rate</u>, $i_r$, should be used.
Conversely, this can also be stated in the following way:
- To do analysis using the <u>market interest rate</u>, all the cash flows have to be converted into <u>actual dollars</u> before performing the analysis.
- On the other hand, to do the analysis using the <u>real interest rate</u>, all the cash flows have to be converted into <u>real dollars</u> before performing the analysis.
## Notes
1. For the base year, real dollars are equal to actual dollars. In other words, if year zero is used as the base year, then PW(Real\$) = PW(Actual\$).
2. If a problem consists of cash flows that have different inflation rates, they will share the same market interest rate, but they will have different real interest rates that will correspond to their inflation rate.
3. Other common terms for **real dollars** are "year zero dollars", "today's dollars", or "constant dollars".
4. Other common terms for **actual dollars** are "nominal dollars", "then-current dollars", or "inflated dollars".
5. If a cash flow is not specifically stated as being in real dollars or actual dollars, the default is to assume that they are actual dollars.