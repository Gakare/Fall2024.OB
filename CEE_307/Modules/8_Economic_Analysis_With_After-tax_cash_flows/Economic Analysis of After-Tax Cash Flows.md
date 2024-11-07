Presents methodologies for
- Calculating income and capital gain taxes for corporations and businesses;
- Economic analysis based on "after-tax cash flows".
# Types of taxes in the US
1. Income tax = $f($gross revenues - allowable deductions$)$
2. Capital gain tax = $f($capital gain$)$
3. Property tax = $f($property value$)$
4. Sales tax = $f($purchase price$)$
5. Excise tax = $f($sale price or quantity of "luxury" and other specialty goods$)$

- In this class:
	1. <u>Income tax</u>: Tax applied to regular (or ordinary) income, which is income generated from sale of goods or services a corporation offers; It <u>excludes</u> sale of capital assets at end of their service lives.
	2. <u>Capital gain tax</u>: This is tax applicable to revenue generated from sale of capital assets at the end of their service lives.
- Note that the following other taxes can be treated as follows
	- Property taxes can be included in annual costs as a tax deductible expense
	- Sales taxes for capital assets are normally included in the cost basis.
	- Sales taxes for non-capital goods can be included in the O&M costs.
# Calculation of After-tax Cash Flows (ATCF)
Calculation of income tax: General relationships
- Taxable income = Gross income - allowable tax deductible expenses
- Tax = (tax rate) $\times$ (Taxable income)
- Allowable tax deductible expenses for corporations and businesses include
	1. Operation and maintenance Costs
	2. Depreciation/depletion of capital assets
Note:
- Capital expenditures are not directly tax deductible (deducted only through annual depreciations)
- Taxable income in year k,
	- $TI_k=R_k-E_k-d_k$
		Where $R_k=$ Total regular (i.e., gross) income in year k;
	- $E_k=$ total O&M expenses in year k;
	- $d_k=$ depreciations in year k;
- Income tax, $Tax_k = (t_j)\times(TI_k)$
		$= (t_i)\times(R_k-E_k-d_k)$
		Where $t_i=$ Regular income tax rate

Calculation of ATCF from regular income:
- Two terms: BTCF and ATCF.
- Net income before paying taxes, i.e.,
	"Before-Tax Cash Flows ($BTCF_k$)" $= R_k-E_k$
Where
		$R_k$ = Gross income in year k;
		$E_k$ = O & M expense in year k;
- Net income after paying taxes, i.e.,
	"After-Tax Cash Flows ($ATCF_k$)" = $BTCF_k-Tax_k$
More on ATCF for regular (or ordinary) income:
$ATCF_k = BTCF_k - Tax_k$
	 $= (R_k-E_k) - (t_i)\times(R_k-E_k-d_k)$
	 $=(R_k-E_k)(1-t_i) + (t_i)(d_k)$
Note: The term $(t_i)(d_k)$ represents <u>tax savings</u> due to the depreciations of capital assets.
# Calculation of capital gain tax:
- Capital gain =  $S_k - B_k$
	Where $S_k=$ Sale price, i.e., Revenue from sale of capital assets in year k;
		$B_k =$ Book value of sold capital assets in year k;
- Taxable income = Capital gain = $S_k-B_k$
Then capital gain tax, $Taxg_k$ = tax rate $\times$ taxable income
	= $(t_g)\times(S_k-B_k)$
Where $t_g=$ capital gain tax rate.

More on ATCF for income from sale of capital assets
- "Before-Tax Cash Flows (BTCF)" = $S_k$
- "After-Tax Cash Flows (ATCF)" = $BTCF_k-Taxg_k$
$ATCF_k=BTCF_k-Taxg_k$
$= S_k - (t_g)\times(S_k-B_k)$
$= (S_k)(1-t_g)+(t_g)(B_k)$
Note: The term ($t_g$)($B_k$) represents <u>tax savings</u> due to the book values of the capital assets sold in year k.

General observations:
1) Since 2018, the federal corporate income tax rate is fixed at 21% of the taxable income. Before that, it used to be a function of the taxable income, the higher the taxable income the higher the tax rate.
2) Tax credit (i.e., negative tax) occurs when the taxable income is negative. It is applicable when analyzing
	1) Cost-only alternatives;
	2) Investment alternatives that loose money. For these, the tax credit is applicable only if a corporation is overall "profitable". Otherwise, negative tax means no income tax has to be paid.
3) The capital gain tax rate is often different from the regular income tax rate, depending on duration of ownership of the capital asset.
4) State taxes are a deductible expense when filing federal income tax, i.e.,
- Federal income tax = {Taxable income - state income tax}$\times$(Federal tax rate)
Where
- State income tax = (Taxable income)$\times$(State tax rate) = (TI)($t_s$)
Then
- Federal income tax = {TI - (TI)($t_s$)}$\times$($t_f$)
$t_s$ and $t_f$ are the state and federal income tax rates, respectively.

General comments:
- Total income tax = State income tax + Federal income tax
	= (TI)($t_s$) + {TI-(TI)($t_s$)}$\times$($t_f$)
	= (TI)($t_s$+$t_f$-$t_st_f$)
Therefore,
- The combined federal and state income tax rate,
	$t_c=t_s+t_f-t_st_f$
5) Normally, analysis done with ATCF should use a different value of MARR (normally a lower value) than the one used for BTCF analysis.
	The approximate relationship between "before-tax MARR (or IRR)" and "after-tax MARR (or IRR)" is:
		Before Tax MARR $\approx\frac{\text{After Tax MARR}}{(1-t)}$
	Or
		Before Tax IRR $\approx\frac{\text{After Tax IRR}}{(1-t)}$
Where
	$t=$ income tax rate