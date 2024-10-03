- This modules presents techniques of economic evaluation of mutually exclusive alternatives using the PW, FW, or AW methods.
- The methods are presented in this video in that order.
# Economic Comparisons Using the PW Method
- Alternatives are compared based on the equivalent net present worth (PW) of the lifecycle cash flows at a given ==minimum attractive rate of return (MARR)==, i.e.,
	- Net PW = PW(revenues) - PW(Costs)
- For a typical alternative (see accompanying cash flow diagram) with an initial investment P, service life N, salvage value S and uniform periodic revenues and costs $A_R$ and $A_C$, respectively, the net present worth is calculated as follows:
	- Net $PW=A_R(P/A,i,N)+S(P/F,i,N)-A_C(P/A,i,N)-P$
Where $i$ is the MARR per period.
![[PW_Method.png]]
- In general, for each investment alternative,
	- A ==positive or zero net PW== means that the investment has a ==rate of return at least equal to the MARR==, and therefore it is an ==economical investment== and ==should be recommended for implementation==.
	- On the other hand, a ==negative net PW== means that the investment has a ==rate of return lower than MARR==, and the investmenent is not economical and ==should normally be rejected==.
- When comparing ==investment alternatives==, the alternative with the ==highest net PW== should be preferred.
- When comparing ==cost-only alternatives==, the one with the ==lowest PW of costs== should be preferred.
- Note that the comparisons should only be made based on the <u>same study period</u>, i.e., the PWs have to be calculated based on the same study period for all alternatives being compared.

# Summary of the PW Method
- Review Examples 3 to 6 in the Module 4a notes. These examples demontstrates other aspects and characteristics of the PW method.
Note that
- Analysis is done based on an interest rate equal to MARR.
- When comparing mutually exclusive investment alternatives, the alternative with the highest net PW is preferred over the others with lower net PW values.
- When comparing mutually exclusive cost-only alternatives, the alternative with the lowest net PW of cost is preferred over the others.
- The relative rankings of alternatives are dependenent on the value of MARR, i.e., changes in the value of MARR used can affect the economic rankings, and hence, economic preference of the alternatives.
- Comparing alternatives using the net PW method has to be done based on the <u>same analysis period</u> or lifetime for all the alternatives. If the service lives are different, the most common method is to use the LCM (Least Common Multiple) of the individual service lives as the common analysis period and assume identical  repeatability of alternatives.

# Economic Comparisons Using the FW Method
- For the FW method, alternatives are compared based on the equivalent net future worth (FW) of the lifecycle cash flows at a given minimum attractive rate of return (MARR), i.e.,
	- Net FW = FW(revenues) - FW(Costs)
- For a typical alternative with an initial investment $P$, salvage values $S$ at the end of service life of $N$ periods and uniform periodic revenues and costs $A_R$ and $A_C$, respectively
	- Net FW = $A_R(F/A,i,N)+S-A_C(F/A,i,N)-P(F/P,i,N)$
- All the rules for the PW method also apply to this method, so no further discussion of the method is presented here.
![[FW_Method.png]]

# Economic Comparisons Using the AW Method
- For the AW method, alternatives are compared based on the equivalent net annual (or periodic) worth (AW) of the lifecycle cash flows at a given minimum attractive of return (MARR), i.e.,
	- Net AW = AW(revenues) - AW(Costs)
- For a typical alternative with an initial investment P, salvage value S at the end of service life of N periods and periodic revenues and costs $A_R$ and $A_C$, respectively
	- Net AW = $A_R-S(A/F,i,N)-A_C-P(A/P,i,N)$
- For cost-only alternatives, $A_R=0$, and the equivalent annual worth is normally referred to as the Equivalent Uniform Annual Cost (EUAC) and is given by
	- EUAC$=A_C+P(A/P,i,N)-S(A/F,i,N)$
		- *Note that since these are all costs, a positive sign is used.*
- Note that, although the method is referred to as the "Annual" worth method, the periodic cash flows may be in any uniform repetitive interval, such as monthly, quarterly, etc. The more appropriate term for this method should have been equivalent uniform "periodic" worth method.

- In general, for each investment alternative,
	- A *positive* or *zero* net AW means that the investment has a rate of return at least equal to the MARR, and therefore it is an economical investment and should be recommended for implementation.
	- On the other hand, a *negative* net AW means that the investment has a rate of return *lower* than MARR, and the investment is not economical and should normally be rejected.
- when comparing investment alternatives, the alternative with the highest net AW should be preferred.
- When comparing cost-only alternatives, the one with the lowest AW of costs should be preferred.
- Although the method is referred to as the "Annual Worth" Method, it can be used to evaluate alternatives with on any other uniform cash flows periods, such as daily, monthly, quarterly, etc.
- Note that the comparisons should only be made based on the <u>same study period</u>, i.e., the AWs have to be the calculated for the same study period for all alternatives. <u>However, application of this method for alternatives with unequal service lives is simpler than that of the PW method, in that you do not have to explicitly do the AW calculations based on the common study period</u>.
# Summary of the AW Method
Note that, similar to the PW and FW methods.
- Analysis is done based on an interest rate ==equal to MARR==.
- When comparing mutually exclusive ==investment alternatives==, the alternative with the ==highest net AW== is preferred over the others with lower net AW values. For ==cost-only alternatives==, the alternative with the ==lowest net AW== of cost is preferred over the others.
- The ==relative rankings of alternatives are dependent on the value of MARR==, i.e., changes in the value of MARR used can affect the economic rankings, and hence, preference of the alternatives.
- The AW method has to be done based on the <u>same analysis period</u> for all the alternatives. However, unlike the PW method, for the AW method, ==there is no need to perform the extra calculations that would be required under the repeatability assumption==. The AW values can directly be compared even in cases of different service lives. However, <u>the repeatability assumption is still implied</u>.
- Using the ==AW method should result== in exactly the same rankings and recommendations as with the PW and FW methods. So it should not matter which of the three methods is used, they should always give same results.