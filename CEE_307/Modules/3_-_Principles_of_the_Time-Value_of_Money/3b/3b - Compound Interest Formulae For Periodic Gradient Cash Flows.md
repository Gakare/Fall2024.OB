- Gradient cash flows are cash flows that consistently increase or decrease over time.
- Two types of gradient cash flows,
1. <u>Arithmetic gradient</u> cash flows - increase (or decrease) by a **fixed amount** every subsequent period.
2. <u>Geometric gradient</u> cash flows - increase (or decrease) by a **fixed rate** every subsequent period.
# Example. <u>Arithmetic</u> gradient cash flows
"Maintenance cost for a truck are estimated to be \$1,200 in the first year and to increase by \$500 every subsequent year over the five years of its service life. What is the present worth of these maintenance costs at an interest rate of 8%."

cash flow diagram:
![[Arithmetic gradient cash flow.png]]
# Example. <u>Geometric</u> gradient cash flows
"Ann Doe plans to make 30 regular annual deposits into her retirement account. She will start with a \$1,000 deposit in the first year and increase that by 6% each subsequent year. How much will her retirement account have immediately after making her $30^{th}$ deposit if the account earns 4% per year?"

cash flow diagram:
![[Geometric gradient cash flow.png]]
# Things that will be covered
1. The future worth of arithmetic gradient cash flows
2. The present worth of arithmetic gradient cash flows
3. The annual worth of arithmetic gradient cash flows
4. The present worth of geometric gradient cash flows
5. The future worth of geometric gradient cash flows

# Formulae for Arithmetic Gradient Cash Flows
## <u>Finding F in terms of G</u>
- Cash Flow Diagram:
![[AGCF.png]]
- Note that
	- The cash flows increase by a fixed amount G every subsequent period
	- The first G occurs at period 2, not period 1. The reason for this will be apparent later in the examples
	- Therefore, there are $N-1$ periodic cash flows
- The formula for finding F, given G, i and N:
	- $F=G[\frac{(1+i)^N-1}{i^2}-\frac{N}{i}]$
- This means that the factor for converting G into an equivalent F, i.e.,
	- $(F/G,i,N)=[\frac{(1+i)^N-1}{i^2}-\frac{N}{i}]$
- This can also be rewritten as
	- $F=\frac{G}{i}[\frac{(1+i)^N-1}{i}-N]$
- Which is can also be in the form of
	- $F=\frac{G}{i}[(F/A,i,N)-N]$

## <u>Finding P in terms of G</u>
- Cash Flow Diagram:
![[Finding P in terms of G CFD.png]]
- Note that, as before
	- The cash flows increase by a fixed amount G every subsequent period
	- The first G occurs at period 2, not period 1. The reason will be apparent later in the examples
	- Therefore, there are $N-1$ periodic cash flows
- The formula for finding P, given G, i and N:
	- $P=G[\frac{(1+i)^N-1}{i^2(1+i)^N}-\frac{N}{i(1+i)^N}]$
- This means that the factor for converting G into P, i.e,
	- $(P/G,i,N)=[\frac{(1+i)^N-1}{i^2(1+i)^N}-\frac{N}{i(1+i)^N}]$
- This can also be rewritten as
	- $P=\frac{G}{i}[\frac{(1+i)^N-1}{i(1+i)^N}-\frac{N}{(1+i)^N}]$
- Note that the two terms inside the brackets are $(P/A,i,N)$ and $(P/F,i,N)$, hence
	- $P=\frac{G}{i}[(P/A,i,N)-N(P/F,i,N)]$