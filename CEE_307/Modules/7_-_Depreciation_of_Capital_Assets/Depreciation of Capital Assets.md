# Topics
- Definition and reasons for depreciation
- Importance in economic analysis
- Time-based classical methods of calculating depreciation
- Depreciation for tax purposes in the US, The MACRS Method
# Definition - Depreciation
- Depreciation is the loss in value of an asset over time. This is normally applicable to capital assets as they get used in business activities.
- It is equivalent to a cost, but it is a non-cash cost.
# Definition - Depletion
- This is similar to depreciation, but it is the term used when the "assets" being depreciated are natural resources. It is the "exhaustion of natural resources" such as mining properties, oil and gas well, etc...
- However, depletion is <u>outside the scope of this class</u>.
# Why do assets depreciate in value?
1) Aging of the asset: As an asset, such as equipment, gets old, the wear and tear makes them less productive and more costly to operate and maintain, hence the asset becomes less valuable than when it was newer.
2) Reduction in value to the owner: the product or service that the asset produces becomes less valuable in the market. For example, a machine that produces flip phones may be the best in the business, but since the product itself has is no longer very marketable, the machinery that produces it is also of little value.
3) Asset becomes obsolete: for example, the asset being superseded by more efficient and/or cheaper technology or one that produces a better quality product.
# Why is depreciation important in economic analysis?
- Depreciation, though a non-cash cost, it is still a real cost that is incurred by the owner of the asset. It therefore has to be factored into the cost of production and included in setting the prices of service or goods produced by the asset.
- In addition, depreciation is a "tax deductible" expense, meaning that the owner of the asset gets tax credit (i.e., a reduction in corporate income tax to be paid) in proportion to the depreciation amount.
# Definitions of Variables related to Depreciation
- **Cost Basis**, B = Cost of acquiring the property
	- It includes the purchase price, sales taxes, shipping and delivery and all other initial costs necessary for the asset to start service or start producing.
- **Market Value**, $MV_k$
	- How much the asset can be sold for in the open market at the end of year $k$ of service.
- **Salvage Value**, S
	- How much the asset is worth to the owner at end of its service life or at the end of the depreciation deductions.
- **Recovery Period**, N = The number of years required to recover the entire depreciable value of the asset, which is often equal to (Cost basis - Salvage Value).
- **Annual depreciation**, $d_k$ = the depreciation amount applicable for year $k$;
	- It is calculated based on the cost basis, the recovery period, and the salvage value.
- **Book value at end of year**, k = The value of the asset in the accounting books;
	- $BV_k=$ Cost basis - Total depreciations through year $k = B - \sum_{j=1}^k d_j$
# Classical time-based methods of depreciation
- Two such methods will be presented, namely
1. Straight line depreciation
2. Declining balance depreciation
# Straight line depreciation (SL)
- The annual depreciation is constant (i.e., it does ==not== vary from year to year)
- It is defined as: Annual depreciation = $\frac{\text{Total amount to be depreciated}}{\text{Depreciation recover period}}$, i.e.,
	- $d_k=\frac{B-S}{N}$
- The corresponding book value at the end of year $k$,
	- $BV_k=$ Cost basis - Sum of all depreciation through year $k$
		- $= B - kd_k$
# Classical time-based methods of Depreciation
- Straight line depreciation
Graphical representation
![[Depreciation.png]]
![[linear depreciation.png]]
# Declining balance depreciation (DB)
- The annual depreciation are non-linear and decreasing from year to year
- It is defined as:
	- Annual depreciation in year $k=$ (constant factor)$\times$(Book value at end of year $k-1$ i.e., $d_k=R(BV_{k-1}$)
	- Where $R$ = constant *rate* of depreciation, $0<R<1$
	- $BV_{k-1}$ = book value at end of year $k-1$ (or beginning of year $k$)
	- Note that $BV_0=B=$ Cost basis
- This translates into the following general equations
Depreciation in year $k$, $d_k$ = $BR(1-R)^{k-1}$; and
Book value at end of year $k$, $BV_k = B(1-R)^k$
- Both $d_k$ and $BV_k$ are non-linear decreasing functions over time.
- Normally, the variable $R$ is defined in terms of the "straight line" rate, $\frac{1}{N}$
	- i.e., $R=P(\frac{1}{N})$ where $p$ defines the rate of depriciation.
	- Typical values of $p$ used in practice are 2 and 1.5
- If $p=2$, then $R=\frac{2}{N}$ and it is referred to "double declining balance" or "200\% declining balance)".
	- If $p=1.5$, then $R=\frac{1.5}{N}$ and this is known as "150% declining balance".
- Declining Balance Depreciation
Graphical representation
![[DB depreciation.png]]
# Example 1 (12:51)
- Calculate the annual depreciations and book values for an asset with a cost basis of \$40,000 which is to be depreciated over 8 years with a salvage value of \$10,000. Use both the SL and DB methods of depreciation. For the DB method, use double declining balance (DDB).
# Declining balance method with switch to straight line
- With the DB method, the book value at the end of the depreciation can never reach zero. This is because the annual depreciation is always a fraction of the remaining book value.
- Therefore, if there is a desire to use the DB method but also to have a final book value equal to zero, a method that combines the DB and the SL methods has been developed for that.
- The method is known as "Declining balance with switch to a straight line"
- With this method, one starts with DB depreciations for a number of years, and then later switches to SL depreciations in order to drive the final book value to zero.
- Below is a detailed description of this method.
- <u>Objective</u>: To use the DB method but have the final book of the asset coincide with the desired salvage value (typically zero) at the end of the depreciation recovery period.
- <u>Method</u>: Combines the use of declining balance (DB) and straight line (SL) methods.
- <u>Steps</u>:
	1. Compute DB depreciation, $d_{DB,k} = R\times BV_{k-1}$
		and SL depreciation, $d_{SL,k}=\frac{BV_{k-1}}{N-k+1}$ for year k, (instead of $\frac{B}{N}$)
		where
			$BV_{k-1} =$ book value at beginning of year k (end of year k-1)
			$N-k+1=$ number of years remaining for depreciation
	2. Compare the two depreciation values, and select the higher of the two, i.e.,
		$d_k=$ max($d_{DB,k},d_{SL,k}$).
		- If $d_{DB,k}>d_{SL,k}$, then set $d_k=d_{DB,k}$ and return to Step 1 to calculate the depreciations for the following year $k=k+1$.
		- If $d_{DB,k}\le d_{SL,k}$, then set $d_k=d_{SL,k}$, and go to step 3. This is the year that the depreciations will switch from DB to SL.
	3. The depreciations for the remaining years will be constant at a value equal to $d_{SL,k}$
Note that it is always the case that the first few years of depreciation, the DB depreciation are going to be higher and therefore the ones selected, and the straight lines depreciation s are going to be in the last few years.

# Part 2
# Depreciation for tax purposes in the USA
Introduction
- In the USA, depreciation is a ==tax-deductible expense==, meaning that depreciation expenses are deducted from gross income before calculating the income tax.
- Only for ==assets used for business activities== (i.e., for income generation) are allowed to claim depreciation as a tax-deductible expense. As such, you cannot, for example, claim depreciation of your personal vehicle or home on your taxes.
- ==Depreciable assets must have a determinable useful life== that is longer than one year. Assets with service lives of a year or less are considered part of ==operation== and ==maintenance costs==. Assets that do not a determinable useful life, such as "land", are not depreciable for tax purposes.
- Assets must wear out, decay, get used up, become obsolete, or lose value from natural causes
- Depreciation method:
	- **Modified Accelerated Cost Recovery System (MACRS)**
	- Passed by the US Congress in <u>1986</u> and modified under the "Tax Cuts and Jobs Act (TCJA)" in 2017.
	- Depreciation method and factors depend on type of asset, namely:
		1. ==Non-real estate property==, such as equipment, furniture, vehicles, etc., and
		2. ==Real-estate property==: Residential and non-residential
- This class will cover depreciation only for **non-real estate capital assets**.
# The MACRS Methods for Non-real Estate Capital Assets
# General Information
- Depreciation recovery period
	- It is a function of "class life" of the asset
	- Class life: It is the **median service life** of the asset, also known as Asset Depreciation Range (ADR) and is typically shorter than the average service life. **Table 7-2** in the textbook has a partial list of assets and their class lives. The complete list is available in Internal Revenue Service (IRS) publications.
- Methods of calculation: A business has the option of selecting one of the following MACRS methods
1. The **General Depreciation System (GDS)** or
2. The **Alternative Depreciation System (ADS)**
![[Table 7-2.png]]
# The General Depreciation System (GDS)
- <u>Recovery period</u>, N, which is also known as "<u>property class</u>", is based on the class life of the asset (Tables 7-2, 7-4).
	For example, an asset with a <u>5-year recovery period under GDS</u> method of depreciation is said to be in the "<u>5-year GDS property class</u>".
- <u>Method</u> of calculating annual depreciations is based on **DB method with switch to SL**, such that
	- 200% DB is used for 10 years and under property classes, and
	- 150% DB is used for 15- and 20-year property classes
	- All calculations are based on salvage <u>value of zero</u>.
	- Depreciation factors are <u>summarized in Table 7-3</u> in the textbook
- Calculations of GDS depreciations
	- Table 7-3 has a summary of the annual depreciation factors, which are based on the DB with switch to straight line, as mentioned earlier
	- Depreciation in year $k$, $d_k=$ (factor for year $k$)$\times$(cost basis)
	- The "half-year convention": This refers to the application of only half of the full-year depreciation for the <u>first year</u> of depreciation and either the <u>last year</u> of ownership or the last year of depreciation, whichever comes first, i.e.,
	- Therefore, if the recovery period is N years, depreciations are going to be spread over N+1 calendar years. For example, for a 5-year recovery period, depreciations are spread over six calendar years, as shown below.
	![[six calendar years.png]]
![[Table 7-3.png]]
# Example:
Cost basis, $B=\$30,000$
GDS Recovery Period = 5 years
Depreciation in year 1 = 0.2(\$30,000) = \$6,000
Depreciation in year 2 = 0.32(\$30,000) = \$9,600
# The Alternative Depreciation System (ADS)
- <u>Recovery Period</u>, N, is based on the class life of the asset (Tables 7-2), and is normally longer than the GDS recovery period. Stretching the depreciation for a longer period is designed to be preferable to business that may not be profitable enough in the early years to be able to take advantage of the tax benefits of depreciation.
- <u>Methods</u> of depreciation - Straight line depreciation
- Similar to the GDS method, the **half-year convention** has to be applied for the first year of depreciation and either the last year of depreciation or the last year of ownership, whichever comes first.
# Example (15:55)
A property with a cost basis of \$30,000 and 6-year ADS recovery period will have the following depreciations:
# Summary
- Depreciations for tax purposes are based on ==**calendar years**==. For example, an asset bought in June 2018 and kept for <u>two years</u> until May 2020, will have <u>three years</u> of depreciation, namely, 2018, 2019, and 2020.

- Steps for application of the MACRS method of depreciation:
	1. Determine depreciation recovery period from Table 7-2 or 7-4.
	2. Determine the depreciation factors for each year of depreciation, i.e.,
		a. For GDS, the factors are given in Table 7-3
		b. For ADS, calculate the factors using straight line depreciations based on the recovery period from Table 7-2.
		In both cases use the <u>half-year convention</u> whenever appropriate.
	3. Calculate the depreciations and book values based on the factors determine from step 2.
- Choosing between the GDS and ADS methods of depreciation
	- For any given asset, a taxpayer may elect to use any of the two methods, i.e., GDS or ADS.
	- However, the decision has to be made in the first year of depreciation of the property, and whatever method is selected then, it has to be used throughout the period of ownership or of depreciation recovery.
	- In general, a company will choose the depreciation method that gives the company a tax advantage, i.e., the method that will result in higher tax <u>savings</u>.
		- Module 8 has a more detailed example that illustrates this concept.
# Example 5 (20:07)
- In April 2020, Jane Doe bought office equipment for use in her company headquarters. The equipment was bought for \$58,800 plus \$1,200 for delivery. She plans to use it for **three years** and sell it in March 2023 for an estimated \$25,000. Determine the equipment's annual depreciations and its book value at the time of disposal in 2023 if she chooses to use the MACRS-GDS method of depreciation for tax purposes.