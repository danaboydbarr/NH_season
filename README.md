# NH_season
Data from NH for RDC-mediated seasonal and regional variation analysis

Title: Variation in pesticide metabolites concentrations in urine explained by season and region

Duration: 19 months

Funding: NIH 1R03ES035184-01


Research question:

To what extent are the concentrations of pesticide metabolites found in urine samples explained by season and region in which sampling takes place? How do observed geographic and seasonal variations compare with urinary chemicals not considered to be seasonal?

Demonstrated Need*
Explain why the research question can only be addressed using the requested restricted-use microdata. Be as specific as possible, including listing key variables or methodological advantages of the restricted file compared to a public-use file (where available).
Currently, the chemical concentrations in urine for the six metabolites (URX) we are interested in studying are available for a large NHANES subpopulation. However,  the time of the year when sampling takes place and the region in which the subjects were sampled are not publicly available.  Without this information, one cannot assess the impact of time and place on human exposures to seasonal chemicals. We are seeking to assess whether the current approach to NHANES sampling captures human exposures consistent with exposures during pesticide applications, which requires season and location information.  Further, we plan to compare any observed signals related to pesticide exposure with levels of urinary chemicals not considered to be seasonal in terms of human exposure (i.e., control chemicals). We have selected a definition of region (Northeast, Appalachia, etc. (see list of derived variables)) that combines states into 11 geographical groups. Use of these regions recognizes the geographic variation in  pesticide application across the country.  If this is not permissible, we would be able to work with a coarser geographical subdivision that would be permitted.


Study Population

We would like to obtain statistical summaries for:

	US population (all)
	US males
	US females
	US adults 19-
	US children 6-18
	

Project Abstract

NHANES field operations are designed to achieve high response rates and high-quality data. Field operation activities include creating schedules for site locations, preparing for the arrival of MECs, and staffing and training. Each year, according to NHANES sampling protocols, 15 primary sampling units (sampling sites) are selected. Per NHANES Analytic Guidelines, scheduling site locations is a complex task that includes multiple considerations such as seasonal weather patterns and difficulties with MEC unit transit. Because MEC units cannot easily traverse difficult roadways with snow and ice patching, logistics require that sampling in areas often hit with harsh winter weather occur during the warmer months (i.e., spring and summer) whereas more temperate locations can be sampled in cooler months (i.e., winter and autumn). Given this, National Health and Nutrition Examination Survey (NHANES) data that may vary by season could be subject to both temporal and spatial bias. This potential bias could, in turn, lead to underestimates of population exposures that form the underpinnings for NHANES reference ranges. We hypothesize that the logistical practices in NHANES sampling may be related to an underestimate of human biomonitoring (HBM) results in chemicals – in particular, pesticides – that may be used seasonally. Specifically, if urine or blood samples are collected in locations and during seasons when certain pesticides or chemicals are not being applied/used, then the overall distributions of human biomonitoring (HBM) concentrations as reported by NHANES would not accurately reflect US population exposures and may not be sufficient for the purpose of setting national reference ranges or to fully interpret biomonitoring data in a health-based context. Our proposed study will evaluate whether CDC’s NHANES provides accurate population-based human biomonitoring levels for seasonal chemicals. It will provide information that will enable CDC to assess their sampling logistics when seeking to represent seasonal and regional variations. It will further enable us to quantify the extent to which NHANES estimates US population exposures to seasonal chemicals. This, in turn, may make it possible to apply a multiplicative factor to future exposure estimates from NHANES to obtain a more accurate assessment of exposure.


Data Linkages

It is unclear what is meant by data linkages. All data are from NHANES. Each analysis we propose will require data (demographic and lab data) that is linked by participant ID (SEQN). 


Software Requirements

We can use R for all of the analysis. We would use the following packages:

•	Hmisc
•	Survey
•	Foreign


Methodology*
Explain the methodology that will be used for the project. The methodology should be clearly stated and appropriate for the research questions. The metadata catalog, agency publications and statistical products, agency webpages describing the restricted access data, and agency contacts are valuable resources for background information for drafting a strong methodology. Expected length: 5-10 pages.

Your methodology may include, but is not limited to, the following information, as appropriate
•	How each requested data set will be used
•	Model equations to be estimated
•	Estimation methods
•	How previous research supports the feasibility of the methodology of the project
•	How model variables will be constructed
•	Strategies for addressing data quality issues
•	Expected sample size and subsamples
•	Unit of analysis including level of geography
•	Ability to link datasets
•	Availability of the study population in the data
•	Use of sample weights, design variables, and adjustments for use of complex survey design
•	Expected outcomes


Proposed methodology
The aim of the proposed analyses is to quantify the degree to which variation in metabolite concentrations in urine is explained by season and place of collection. The metabolites we consider are 2,4-D (URX24D), 3,5,6-trichloropyidinol (URXCPM), 3-phoxybenzoic acid (URXOPM), 3-benzophenone (URXBP3), mono-ethyl phthalate (URXMEP) and 1-pyrene (URXP10). The first four of these are used seasonally and the last two are not. The non-seasonal chemicals have been included for comparative control purposes.
Our focus is on 5 different populations (US overall, US males, US females, US adults, US children). For each population, we focus on the 6 above-mentioned metabolite concentrations measured in urine. NHANES provides publicly available data on all of these metabolites in every one of the 5 two-year cycles from 2007-2016 except for one: 3,5,6-trichloropyridinol is not available in the 2011-2012 cycle but is available for the other four cycles. We request that the NHANES survey years of interest be combined in order to have a robust sample size.  All of the analyses proposed would combine data for all years in the range of 2007-2016 for which a given metabolite is available.  Combining data from multiple survey years has been performed by many researchers (e.g., Di et al. 2023; Gillezeau et al. 2019; Fry and Power 2017), including members of this research team. 

All of the proposed analyses can be carried out in R.  Scripts will be provided with the analyses to perform with outputs being comma-delimited tables, with each resultant table in a separate file.
Analysis for a given population/metabolite pair
The description of the analyses we request for each of the 5x6=30 population/metabolite pairs is identical, so for illustrative purposes, we focus here on the entire US population and a single metabolite,  2,4-D (URX24D).
Two analyses are envisioned – a stratified analysis and a regression analysis.
Stratified analysis
In the stratified analysis, the strata consist of all possible geographical/season pairs. In the following description, it is assumed that we will be permitted to split up the sample data into the 11 possible regions (derived from sampling state) and 4 seasons (derived from sampling date) as shown in Table 1. This way of subdividing the US states can be found in various publications including https://www.ers.usda.gov/webdocs/publications/93026/eib-208.pdf?v=2357.2 (page 8).
Please note that we recognize that we may not be permitted to use such a fine partitioning into geographical regions, and we are prepared to carry out an analogous analysis using a coarser partitioning, i.e., into a smaller number of geographical regions. That said, we are not seeking raw data, but rather statistical summaries for 4 or 5  2-year NHANES cycles in aggregate, so perhaps the subdivision into the finer regions we propose will be viewed as acceptable and respectful of privacy concerns. 

	Winter	Spring	Summer	Fall
Northeast				
Appalachia				
Southeast				
DeltaStates				
CornBelt				
LakeStates				
NorthernPlains				
SouthernPlains				
Mountain				
Pacific				
FarWest				
Table 1. Proposed strata for statistical summaries are represented by the 11 x 4 = 44 blank cells shown.
For typical metabolites,  urine concentrations have heavy right tails and taking logs  reduces the skewness considerably. A preliminary analysis has been performed and shows that most of the  metabolite concentrations appear to be roughly log-normally distributed. There are exceptions however as log 2,4-D has a roughly exponential distribution, while log of 3,5,6-trichloropyidinol, 3-phoxybenzoic acid, and  1-pyrene have distributions in which the value at the detection limit is pronounced in some cycles. Nevertheless,  for all metabolites under consideration, the geometric mean provides a better overall measure of central tendency, so we propose to compute all summary statistics for every urinary metabolite concentration in every stratum for the entire 2007-2016 time period on a log scale. Thus, we propose to compute 
•	the weighted mean of log-concentration for all observations in the stratum
•	the weighted standard deviation of log-concentration for all observations in the stratum.
For all of the metabolites under consideration, again, from preliminary analysis, taking logs removes the effect of any outliers. 
In our experience, when the log-concentrations are calculated for NHANES chemical concentration data, they are log-normally distributed.
Here, the weighting utilized will follow the guidelines published by the CDC at this site: 
https://wwwn.cdc.gov/nchs/nhanes/tutorials/weighting.aspx
From these guidelines, the following statement: 
Selecting the Correct Weight in NHANES
Various sample weights are available on the data release files – such as the interview weight (wtint2yr), the MEC exam weight (wtmec2yr), and several subsample weights. Use of the correct sample weight for NHANES analyses depends on the variables being used. A good rule of thumb is to use "the least common denominator" where the variable of interest that was collected on the smallest number of respondents is the "least common denominator." The sample weight that applies to that variable is the appropriate one to use for that particular analysis.
suggests that we should utilize weights that are provided in the laboratory file  (WTSA2YR, WTSB2YR, WTSC2YR) for each metabolite and for each 2 year cycle.
In addition, since we only consider survey years after 2001, the following statement from this site becomes relevant:
For any combination of survey cycles from 2001-2002 and beyond that does not include 1999-2000 data, the multiyear sample weight constructed using the formulas in the above table is a linear scaling of the two-year weight, i.e. the weight is multiplied by a constant equal to (1 / number of survey cycles.) Weighted estimates of most population parameters (e.g. proportions, means, percentiles) and their standard errors produced using this scaled multiyear weight should match the weighted estimates that would be produced by using the two-year weight variable directly.

And consequently, we estimate population log-normal distribution parameters in each stratum using the weighted mean of the sampled log-concentrations, and weighted standard deviation of the sampled log-concentrations. The R Hmisc package can be used for this purpose.  In addition, we want to determine the weighted 95th percentile for each log-concentration distribution. Again, this calculation is available using the Hmisc package.
Furthermore, where possible, we seek 95% confidence intervals for the mean log-concentration and for the 95th percentile. We will use the R survey package for this purpose and follow the guidelines found at this link for NHANES SurveyDesign that use variance estimates and degrees of freedom that account for the complex survey design used in NHANES.  When a stratum has insufficient sample size, we will not compute confidence intervals.
In conclusion, our analysis for the 2,4-D metabolite and the entire US population should lead to the following deliverables, each being a table of the form in Table 1 with cells filled in as follows:
•	sample size table – for each cell (stratum) the number of participants with measured urinary 2,4-D 
•	weighted mean of log 2,4-D concentration table for stratum
•	weighted standard deviation of log 2,4-D concentration for stratum
•	weighted 95th percentile of log 2,4-D concentration for stratum
•	lower 95% confidence interval for the stratum mean log 2.4-D concentration
•	upper 95% confidence interval for the stratum mean log 2.4-D concentration
•	lower 95% confidence interval for the stratum 95th percentile for log 2.4-D concentration
•	upper 95% confidence interval for the stratum 95th percentile for log 2.4-D concentration
The results for the other urinary metabolites would follow the same pattern.
In the metabolite exposure literature, it is a common practice to account for variation in urine dilution by  converting the volume-based concentrations  to creatinine adjusted levels (reference), i.e., the measured metabolite concentration is divided by the measured creatinine concentration. For example, NHANES presents its urinary concentration data using both volume-based and creatine-adjusted approaches in its National Reports on Human Exposure to Environmental Chemicals (https://www.cdc.gov/exposurereport/index.html).  While this practice has been questioned due to the intra-individual variability in urinary creatinine levels and its impact on the interpretation of the resultant “corrected” concentration data (Barr et al. 2005; LaKind and Naiman 2015), we will be comparing our results to that in the published literature, much of which will be available only as creatinine-corrected data. In terms of log concentrations this amounts to correcting by the log metabolite concentration by subtracting the log creatinine (URXUCR) concentration, i.e., using the derived variables LURX24D (log 2,4-D concentration) and LURXUCR (log creatinine concentration) we create the creatinine-adjusted log 2,4-D concentration:
	LURX24DCADJ = LURX24D – LURXUCR
and produce the following tables, again one entry for each stratum:
•	weighted mean of adjusted log 2,4-D concentration table for stratum
•	weighted standard deviation of adjusted log 2,4-D concentration for stratum
•	weighted 95th percentile of adjusted log 2,4-D concentration for stratum
•	lower 95% confidence interval for the stratum mean adjusted log 2.4-D concentration
•	upper 95% confidence interval for the stratum mean adjusted log 2.4-D concentration
•	lower 95% confidence interval for the stratum 95th percentile for adjusted log 2.4-D concentration
•	upper 95% confidence interval for the stratum 95th percentile for adjusted log 2.4-D concentration
The methodology for producing the entries in these 2,4-D tables as well as those for the other metabolites is identical to that used for the unadjusted log-concentration tables.
Regression Analysis
The aim of the proposed regression analysis is to determine whether there is a significant region/season interaction in predicting the log concentration of a metabolite in urine in the population of interest. Such a finding would provide evidence suggesting that in order to predict chemical concentration in a population, correcting for region and season by themselves is insufficient. 
For each population, e.g., all US and each metabolite, we propose to fit a weighted linear regression model predicting the log concentration of a metabolite in a given population using as predictors:
•	Male indicator (derived from RIAGENDR)
•	Age group indicators (derived from RIDAGEYR) with AGE1 (19-29 years) as a reference
o	AGE0
o	AGE2
o	AGE3
o	AGE4
o	AGE5
•	Survey cycle indicators (Y0910,Y1112,Y1314,Y1516) with survey cycle 2007-2008 as reference
•	log-creatinine (LURXUCR derived from URXUCR)
•	race group indicators (variables derived from RIDRETH1) with Non-Hispanic White as a reference
o	MexicanAmer indicator
o	OtherHispanic indicator
o	NonHispanicBlack indicator
o	Other indicator
•	region – 10 indicators, one for each of the 11 regions except for Northeast (used as a reference)
•	season 3 indicators, one for each of the 4 seasons except Winter (used as a reference)
•	region/season interactions (30 – one for each region/season with region not Northeast and season not Winter)
Race, and age group are included as it is suggested in the chemical exposure literature that creatinine adjustment should include race,  gender, and age (O’Brien et al).
The lm (linear model) package in R would be used to perform the model fit. 
The output we are interested in consists of
•	table of estimated regression coefficients with standard errors, p-values
•	result of F-test for season/region interaction (simultaneous test for all interactions)

Barr DB, Wilder LC, Caudill SP, Gonzalez AJ, Needham LL, Pirkle JL. Urinary creatinine concentrations in the U.S. population: implications for urinary biologic monitoring measurements. Environ Health Perspect. 2005 Feb;113(2):192-200. doi: 10.1289/ehp.7337. PMID: 15687057; PMCID: PMC1277864. 

Di D, Zhang R, Zhou H, Wei M, Cui Y, Zhang J, Yuan T, Liu Q, Zhou T, Liu J, Wang Q. Exposure to phenols, chlorophenol pesticides, phthalate and PAHs and mortality risk: A prospective study based on 6 rounds of NHANES. Chemosphere. 2023 Jul;329:138650. doi: 10.1016/j.chemosphere.2023.138650. Epub 2023 Apr 8. PMID: 37037349.

Gillezeau C, Alpert N, Joshi P, Taioli E. Urinary Dialkylphosphate Metabolite Levels in US Adults-National Health and Nutrition Examination Survey 1999-2008. Int J Environ Res Public Health. 2019 Nov 20;16(23):4605. doi: 10.3390/ijerph16234605. PMID: 31757049; PMCID: PMC6926828. 

Fry K, Power MC. Persistent organic pollutants and mortality in the United States, NHANES 1999-2011. Environ Health. 2017 Oct 10;16(1):105. doi: 10.1186/s12940-017-0313-6. PMID: 29017533; PMCID: PMC5634885.


LaKind JS, Naiman DQ. Temporal trends in bisphenol A exposure in the United States from 2003-2012 and factors associated with BPA exposure: Spot samples and urine dilution complicate data interpretation. Environ Res. 2015 Oct;142:84-95. doi: 10.1016/j.envres.2015.06.013. Epub 2015 Jun 26. PMID: 26121292.



