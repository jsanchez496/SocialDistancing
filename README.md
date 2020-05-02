# State-level social distancing policies in response to the 2019 novel coronavirus in the US

This is a routinely-maintained data repository for US state-level distancing policies to the 2019 novel coronavirus (SARS-CoV-2), the cause of COVID-19. It was developed and is maintained by researchers at the University of Washington, Seattle, WA, USA. 

Note all data provided here are subject to updates or revisions based on continuing review of existing policy documentation as well as adoption of new policy mandates. All efforts will be made to clearly document and communicate any updates or revisions as they occur.

Analysis of these data is also underway; interested parties should contact us (see information below).

![Figure](https://github.com/COVID19StatePolicy/SocialDistancing/blob/master/figure/Figure.png)
## Organization


**data** : .csv files  
**source** : Currently compiled pdf documentation of policies identified; further compilation in-progress.

## State-level policy response:
- **File**: "USstatesCov19distancingpolicy.csv". Prior datasets are archived with date stamps in the format of YYYYMMDD.
- **location_id**: State-level unique identifier per the Global Burden of Disease (GBD) study.  
- **StateFIPS**: State-level Federal Information Processing Standard (FIPS) code.    
- **StatePostal**: Two-letter state postal code.  
- **StateName**: State name.  
- **StatePolicy** : String variable of state policies, as described below:   
      - **EmergDec**: Emergency declaration; currently includes State of Emergency, Public Health Emergency, and Public Health Disaster declarations.     
      - **GathRecomAny**: Any recommendation of against gathering that stops short of a formal mandate or restriction of gatherings.  Includes uses phrasing such as "advises against mass gatherings" and "constituents should avoid gatherings of more than 100" that imply a recommendation versus restriction.    
      - **GathRestrictAny**: Restriction of any gathering; includes formal mandate or an executive order that uses phrasing such as "prohibits all mass gatherings" (per definition of mass gathering) and "constituents must avoid gatherings of more than 100". The first issuance of a gathering restriction of any size is coded with this date.      
      - **GathRestrict1000**: Restriction of any gathering exceeding 1000 persons; coding followed the "GathRestrict" criteria. Some mandates include exceptions for essential businesses and organizations; these cases are still coded as a restriction applicable to the general public.     
       - **GathRestrict500**: Restriction of any gathering exceeding 500 persons; coding followed the "GathRestrict" criteria and used the same coding approach as "GathRestrict1000" (i.e., considered a restriction if applicable to the general public).      
       - **GathRestrict250**: Restriction of any gathering exceeding 250 persons; coding followed the same criteria as above.    
       - **GathRestrict100**: Restriction of any gathering exceeding 100 persons; coding followed the same criteria as above.    
       - **GathRestrict50**: Restriction of any gathering exceeding 50 persons; coding followed the same criteria as above.    
       - **GathRestrict25**: Restriction of any gathering exceeding 25 persons; coding followed the same criteria as above.         
       - **GathRestrict10**: Restriction of any gathering exceeding 10 persons; coding followed the same criteria as above.    
       - **GathRestrict5**: Restriction of any gathering exceeding 5 persons; coding followed the same criteria as above.    
       - **SchoolClose**: Formal closing of (at minimum) public schools. Where possible, additional information on types of school closings are provided in "PolicyCodingNotes".      
       - **RestaurantRestrict**: Restriction or limitation of restaurants and other venues where food is consumed on-premises. Coding a case as a restriction requires a formal restriction on operations (e.g., offsite consumption only, limiting services to only take-away, delivery, or curbside drop-off) or mandate for substantially reducing operations (e.g., restaurant closure must occur unless 10 or fewer patrons are dining at at time).      
       - **OtherBusinessClose**: Mandate to fully close operations of any category of business. Coding a case as an other business closure requires the executive order to use phrasing indicative of a mandate (e.g., "casinos must close", "operations at fitness centers and entertainment venues must cease by *date*"). A given state may have multiple cases of other business closures as they often occurred in phases (e.g., fitness centers and gyms on March 13, 2020; casinos and entertainment venues on March 15, 2020; personal service businesses like barbers and nail salons on March 19, 2020); thus, where possible, separate entries are provided for each mandate.    
       - **NEBusinessClose**: Mandate to close all non-essential businesses. Coding a case as a closure order requires the executive order to use phrasing indicative of a mandate (e.g., "non-essential businesses are required to close", "non-essential businesses must cease operations by *date*"). Coding does not distinguish among states' classification of essential versus non-essential businesses, as they vary substantially by state.      
       - **StayAtHome**: Mandate for individuals to stay at home for all non-essential activities. Coding a case as a stay-at-home order mandate requires the executive order to using phrasing indicative of a mandate (e.g., "must stay at home"); otherwise it is coded as 0 for the "Mandate" variable if it uses advisory phrasing. Coding does not distinguish among states' classification of essential versus non-essential activities, as they vary substantially by state. Shelter-in-place and stay-at-home orders are considered to be equivalent.       
       - **StateCurfew**: Mandates specific curfews at which residents are not to be outside their homes unless performing essential activities, as defined by the state. Coding a case as a state curfew requires specific curfew times (thus "stay-at-home" mandates were not considered curfews).      
       -**Quarantine**: Quarantines mandated for people entering the state, requiring a period of self-isolation. Quarantines may be imposed on all people entering the state, out-of-state residents, or travelers from a particular state or city. Quarantine length and who is covered by the policy can be found in the "PolicyNotes" variable. This policy type was added April 3, 2020.    
       -**TravelRestrictIntra**: Restrictions on travel within the state. These restrictions can be between cities or counties or within them. The "StateWide" variable reflects whether these restrictions are applicable to across the state (coded as 1) or only for local areas (coded as 0). This policy type was added April 3, 2020.    
       -**TravelRestrictExit**: Policies which prohibit residents of a state from leaving the state. These policies may have exceptions for essential businesses. This policy type was added April 3, 2020.    
       - **TravelRestrictEntry**: Travel restriction mandates that limit non-residents from entering a given state. These policies may have exceptions or exemptions for essential businesses or their employees, and they may include restrictions for commercial lodging for non-residents. This policy type was added April 8, 2020.    
      - **CaseIsolation**: Policy that requires individuals with confirmed COVID-19 infection (via testing) or suspected COVID-19 infection to self-isolate for a specified period of time, or when they no longer test positive for infection. This policy type may also include requirements for quarantine of individuals who have been identified as high-risk for developing COVID-19 due to their close contact to patients with confirmed or suspected infections, including sharing the same residence. This policy type is different from "Quarantine" in this dataset, which refers to policies that require self-quarantine for individuals entering a state from any or particular points of origin. This policy type was added April 25, 2020.    
      - **PublicMask**: Policy that requires individuals to wear masks or other mouth and nose coverings when they are outside their places of residence in the public. This policy type does not reflect requirements around mask use or other types of personal protective equipment mandated as part of business operations, either routine or under efforts to ease distancing policies to re-establish in-person operations of business establishments. This policy type was added April 25, 2020.   
- **Mandate**: Binary variable indicating whether the policy applied is a mandate (1) or is advisory or a recommendation (0). This is coded on the basis of the order's phrasing (e.g., "residents are advised to stay at home and avoid unnecessary travel" would be coded as 0 for mandate as a "StayAtHome" policy). This variable was added on March 30, 2020.   
- **DateIssued**: Date of policy issuance. The date of signing of the policy document (e.g., executive order) was used wherever possible. Format is YYYYMMDD (e.g., March 16, 2020 is 20200316). Entries are not currently included for most non-statewide policies; this documentation is in-progress.  
- **DateEnacted**: Date of policy enactment: the date of when the policy would be enforced, per descriptions available in policy documents. The format is YYYYMMDD. Entries are not currently included for most non-statewide policies; this documentation is in-progress.  
- **DateExpiry**: Date of policy expiry, if or as provided in the policy issuance or executive order. This date is meant to reflect when the policy or order would be in effect until or unless additional action is taken to extend, amend, or halt its status. The format is YYYYMMDD. This documentation is in-progress, as it was added on March 29, 2020 as a variable of interest.   
- **DateEased**: Date the policy is eased. This date is meant to reflect when a policy is eased, relative to its original mandate. This does not reflect the timing at which a policy is actively ended; instead, this reflects the timing at which original restrictions are no as strict or comprehensive without fully ending the mandate. The format is YYYYMMDD. This variable was added April 27, 2020.    
- **DateEnded**: Date the policy is ended. This date is meant to reflect when a policy is ended, particularly if it is halted or reversed prior to its expiry date. The format is YYYYMMDD. This documentation is in-progress.    
- **PolicyCodingNotes**: Coder notes. Information on specific businesses closed, type of emergency declaration, potential exceptions, etc., are provided here. 
- **PolicySource**: Currently available source for each policy issued. Sourcing by hard-copy PDF _versus_ hyperlinks is in-progress.    
- **StateWide**: Binary variable indicating whether the policy applied statewide (1) or for local areas (0).   
- **LastUpdated**: Date of last update for the given state-policy observation. The format is YYYYMMDD.    
- **LastUpdatedNotes**: Coder notes on last updates. This reflects notable changes since the last update, especially if a date has been recoded (e.g., switching to coding orders enacted at 11:59 pm on date1 to date1+1 for its enactment timing) or the "StatePolicy" type has been amended (e.g., some initial coding of "NEBusinessClose" policies were applicable to non-essential in-person retail businesses only, not all non-essential businessess as defined by state). 

## State-level policy response: _BETA DATASET_ (introduced May 2, 2020)
This dataset involves the transition of each state over to each policy action linked by policy ids, which enables better tracking of how policies have been enacted, expanded, eased, or ended over time. Our current dataset ("USstatesCov19distancingpolicy.csv") will be maintained in parallel while we move each state over to this new format. Once that is complete, the BETA dataset will use the same file name as before. We will provide regular status updates.

- **File**: "USstatesCov19distancingpolicyBETA.csv". Prior datasets are archived with date stamps in the format of YYYYMMDD.  
- **PID**: Policy id, or the unique id for each policy action. PIDs are used to link policy actions - Extends, Expands, Eases, Ends, Depends - to each other. They are six characters, with the first two characters being the two-letter state postal code and the next four being numerical format with leading zeros (i.e., PIDs of AK0001, AK0002 for two separate policies in Alaska). The numbers associated with each PID do not reflect the ordering of policy implementation, nor do they reflect the total number of mandates enacted by a given state. Multiple policy actions can come from a single executive order, and some earlier policies received "later" PIDs because they were identified upon further review. Instead, they should be viewed as **unique identifiers** for the different types of policy actions taken, which then can be linked together over time as they are extended, expanded, eased, or ended.  
- **location_id**: State-level unique identifier per the Global Burden of Disease (GBD) study.  
- **StateFIPS**: State-level Federal Information Processing Standard (FIPS) code.    
- **StatePostal**: Two-letter state postal code.  
- **StateName**: State name.  
      - **States currently included**: Alaska, Georgia, Tennessee, Texas.       
- **StatePolicy** : String variable of state policies, as described below:   
      - **EmergDec**: Emergency declaration; currently includes State of Emergency, Public Health Emergency, and Public Health Disaster declarations.     
      - **GathRecomAny**: Any recommendation of against gathering that stops short of a formal mandate or restriction of gatherings.  Includes uses phrasing such as "advises against mass gatherings" and "constituents should avoid gatherings of more than 100" that imply a recommendation versus restriction.    
      - **GathRestrictAny**: Restriction of any gathering; includes formal mandate or an executive order that uses phrasing such as "prohibits all mass gatherings" (per definition of mass gathering) and "constituents must avoid gatherings of more than 100". The first issuance of a gathering restriction of any size is coded with this date.      
      - **GathRestrict1000**: Restriction of any gathering exceeding 1000 persons; coding followed the "GathRestrict" criteria. Some mandates include exceptions for essential businesses and organizations; these cases are still coded as a restriction applicable to the general public.     
       - **GathRestrict500**: Restriction of any gathering exceeding 500 persons; coding followed the "GathRestrict" criteria and used the same coding approach as "GathRestrict1000" (i.e., considered a restriction if applicable to the general public).      
       - **GathRestrict250**: Restriction of any gathering exceeding 250 persons; coding followed the same criteria as above.    
       - **GathRestrict100**: Restriction of any gathering exceeding 100 persons; coding followed the same criteria as above.    
       - **GathRestrict50**: Restriction of any gathering exceeding 50 persons; coding followed the same criteria as above.    
       - **GathRestrict25**: Restriction of any gathering exceeding 25 persons; coding followed the same criteria as above.         
       - **GathRestrict10**: Restriction of any gathering exceeding 10 persons; coding followed the same criteria as above.    
       - **GathRestrict5**: Restriction of any gathering exceeding 5 persons; coding followed the same criteria as above.    
       - **SchoolClose**: Formal closing of (at minimum) public schools. Where possible, additional information on types of school closings are provided in "PolicyCodingNotes".      
       - **RestaurantRestrict**: Restriction or limitation of restaurants and other venues where food is consumed on-premises. Coding a case as a restriction requires a formal restriction on operations (e.g., offsite consumption only, limiting services to only take-away, delivery, or curbside drop-off) or mandate for substantially reducing operations (e.g., restaurant closure must occur unless 10 or fewer patrons are dining at at time).      
       - **OtherBusinessClose**: Mandate to fully close operations of any category of business. Coding a case as an other business closure requires the executive order to use phrasing indicative of a mandate (e.g., "casinos must close", "operations at fitness centers and entertainment venues must cease by *date*"). A given state may have multiple cases of other business closures as they often occurred in phases (e.g., fitness centers and gyms on March 13, 2020; casinos and entertainment venues on March 15, 2020; personal service businesses like barbers and nail salons on March 19, 2020); thus, where possible, separate entries are provided for each mandate.    
       - **NEBusinessClose**: Mandate to close all non-essential businesses. Coding a case as a closure order requires the executive order to use phrasing indicative of a mandate (e.g., "non-essential businesses are required to close", "non-essential businesses must cease operations by *date*"). Coding does not distinguish among states' classification of essential versus non-essential businesses, as they vary substantially by state.      
       - **StayAtHome**: Mandate for individuals to stay at home for all non-essential activities. Coding a case as a stay-at-home order mandate requires the executive order to using phrasing indicative of a mandate (e.g., "must stay at home"); otherwise it is coded as 0 for the "Mandate" variable if it uses advisory phrasing. Coding does not distinguish among states' classification of essential versus non-essential activities, as they vary substantially by state. Shelter-in-place and stay-at-home orders are considered to be equivalent.    
       -**Quarantine**: Quarantines mandated for people entering the state, requiring a period of self-isolation. Quarantines may be imposed on all people entering the state, out-of-state residents, or travelers from a particular state or city. Quarantine length and who is covered by the policy can be found in the "PolicyNotes" variable. This policy type was added April 3, 2020.    
       -**TravelRestrictIntra**: Restrictions on travel within the state. These restrictions can be between cities or counties or within them. The "StateWide" variable reflects whether these restrictions are applicable to across the state (coded as 1) or only for local areas (coded as 0). This policy type was added April 3, 2020.    
       -**TravelRestrictExit**: Policies which prohibit residents of a state from leaving the state. These policies may have exceptions for essential businesses. This policy type was added April 3, 2020.    
       - **TravelRestrictEntry**: Travel restriction mandates that limit non-residents from entering a given state. These policies may have exceptions or exemptions for essential businesses or their employees, and they may include restrictions for commercial lodging for non-residents. This policy type was added April 8, 2020.    
      - **CaseIsolation**: Policy that requires individuals with confirmed COVID-19 infection (via testing) or suspected COVID-19 infection to self-isolate for a specified period of time, or when they no longer test positive for infection. This policy type may also include requirements for quarantine of individuals who have been identified as high-risk for developing COVID-19 due to their close contact to patients with confirmed or suspected infections, including sharing the same residence. This policy type is different from "Quarantine" in this dataset, which refers to policies that require self-quarantine for individuals entering a state from any or particular points of origin. This policy type was added April 25, 2020.    
      - **PublicMask**: Policy that requires individuals to wear masks or other mouth and nose coverings when they are outside their places of residence in the public. This policy type does not reflect requirements around mask use or other types of personal protective equipment mandated as part of business operations, either routine or under efforts to ease distancing policies to re-establish in-person operations of business establishments. This policy type was added April 25, 2020.    
      - **BusinessHealthSafety**: Policies or government-developed guidelines involving specific types of social distancing, sanitation and hygiene, disinfectant and cleaning, and employee protocols (e.g., temperature checks and symptom screenings before shifts start, use of cloth facial coverings during shifts, requirements for employees if they are ill) above and beyond standard business and health safety requirements for a given industry. These policies or protocols are often instituted in relation to easing prior business restrictions, and such easing of restrictions depends on the existence and adherence to these protocols. Subsequently, "BusinessHealthSafety" is often a policy that is linked via "Depends" for easing various restrictions. This variable was added on May 2, 2020.  
- **Mandate**: Binary variable indicating whether the policy applied is a mandate (1) or is advisory or a recommendation (0). This is coded on the basis of the order's phrasing (e.g., "residents are advised to stay at home and avoid unnecessary travel" would be coded as 0 for mandate as a "StayAtHome" policy). This variable was added on March 30, 2020.   
- **StateWide**: Binary variable indicating whether the policy applied statewide (1), or whether the policy is only applicable to sub-state geographic areas (e.g., counties) or sub-populations within a state (e.g., individuals aged 65 and older).  
- **SWGeo**: Binary variable indicating whether the policy is applied for all geographic areas in the state (1) or whether the policy is only applicable to sub-state geographic areas (e.g., counties). If SWGeo is coded as 0, StateWide will also be coded as 0. This variable was added May 2, 2020.  
- **SWPop**: Binary variable indicating whether the policy is applicable to the state's full population (1) or whether the policy is only applicable to sub-populations (e.g., individuals aged 65 and older, individuals with chronic and/or severe health conditions). If SWPop is coded as 0, StateWide will also be coded as 0. This variable was added May 2, 2020.  
- **DateIssued**: Date of policy issuance. The date of signing of the policy document (e.g., executive order) was used wherever possible. Format is YYYYMMDD (e.g., March 16, 2020 is 20200316). Entries are not currently included for most non-statewide policies; this documentation is in-progress.  
- **DateEnacted**: Date of policy enactment: the date of when the policy would be enforced, per descriptions available in policy documents. The format is YYYYMMDD. Entries are not currently included for most non-statewide policies; this documentation is in-progress. In the beta dataset, if a policy is eased, the date of easement would be considered "DateEnact" for that particular policy action and then the policy it eases would be listed under "Eases."
- **DateExpiry**: Date of policy expiry, if or as provided in the policy issuance or executive order. This date is meant to reflect when the policy or order would be in effect until or unless additional action is taken to extend, amend, or halt its status. The format is YYYYMMDD. This documentation is in-progress, as it was added on March 29, 2020 as a variable of interest.     
- **DateEnded**: Date the policy is ended. This date is meant to reflect when a policy is ended, particularly if it is halted or reversed prior to its expiry date. The format is YYYYMMDD. This documentation is in-progress.  
- **Extends**: Policy id (PID) that a given mandate or policy action extends. This usually means that the previous policy will be in effect beyond its previous expiry date. An example: AK0004, a restaurant restriction in Alaska, was issued on 20200317, enacted 20200318, and had an initial expiry date of 20200401. AK0020, which was issued on 20200327 and enacted on 20200328, has AK0004 under the "Extends" variable, reflecting that this policy is extended until the DateExpiry listed for AK0020 (20200411). If (or when in this case) AK0020 is extended by a new order, AK0020 would be listed on that policy's "Extends" (which was AK0033). This variable was added on May 2, 2020.  
- **Expands**: Policy id (PID) that a new mandate or policy expands. This can mean different types of expansions: a policy now covers more populations or locations (e.g., expanding a local stay-at-home order to being statewide); a policy now includes a longer list of business types that must close in-person operations; a policy is now a mandate versus recommendations; and so on. This variable was added on May 2, 2020.  
- **Eases**: Policy id (PID) that a new mandate or policy eases. This means that while a previous policy is not fully ended yet, its earlier restrictions or mandates are no longer as strong. This could involve relaxing bans on mass gatherings (e.g., now groups of 25 or more are prohibited, versus 10); easing closure mandates on certain types of businesses so that they can limited in-person services (e.g., only up to 50% capacity); moving a stay-at-home order to a recommendation versus mandate; allowing some in-person instruction to occur for certain schools; and so on. As we code more policies that ease restrictions, we anticipate this variable to be refined further and we will document updates accordingly. This variable was added on May 2, 2020.  
- **Ends**: Policy id (PID) that a new mandate or policy ends. This means that the prior policy or executive order has either been formally ended, rescinded, or repealed. This variable was added on May 2, 2020.  
- **Depends**: Policy id (PID) that a new mandate or policy depends on. To date this typically links to a "BusinessHealthSafety" policy or protocol developed by the government or governmental agencies that details health and safety practices for in-person operations amid the ongoing COVID-19 epidemic. This variable was added on May 2, 2020.  
- **PolicyCodingNotes**: Coder notes. Information on specific businesses closed, type of emergency declaration, potential exceptions, etc., are provided here. 
- **PolicySource**: Currently available hyperlink for each policy issued.  
- **PolicySourceID**: Name of the PDF source used for each policy. For policies or orders wherein a website page is the only available source, the page was converted to a PDF and saved under "source" on GitHub.
- **LastUpdated**: Date of last update for the given state-policy observation. The format is YYYYMMDD.    
- **LastUpdatedNotes**: Coder notes on last updates. This reflects notable changes since the last update, especially if a date has been recoded (e.g., switching to coding orders enacted at 11:59 pm on date1 to date1+1 for its enactment timing) or the "StatePolicy" type has been amended (e.g., some initial coding of "NEBusinessClose" policies were applicable to non-essential in-person retail businesses only, not all non-essential businessess as defined by state).    
- **UpdatingSource1**: Primary source for updating policies for a given state.  
- **UpdatingSource2**: Secondary source for updating policies for a given state.  

## Citation
As the data are updated regularly, please check any relevant updates here:    

Nancy Fullman, Bree Bang-Jensen, Kenya Amano, Christopher Adolph, and John Wilkerson. "State-level social distancing policies in response to COVID-19 in the US". Version 1.32, May 2, 2020. http://www.covid19statepolicy.org

## Contributors
Policy data compiled here are primarily sourced by the National Governors Association (NGA) and Kaiser Family Foundation (KFF) online resources for coronavirus response in the US, and then supplemented with additional searches (e.g., governor websites). We greatly appreciate both NGA and KFF's ongoing maintenance of these in-depth resources, especially amid such rapidly evolving policy contexts.

National Governors Association (NGA):  https://www.nga.org/coronavirus/  
Kaiser Family Foundation (KFF):  https://www.kff.org/health-costs/issue-brief/state-data-and-policy-actions-to-address-coronavirus/


**Specific contributors**

| Name  | Affiliation | Email | Twitter | GitHub |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Christopher Adolph  | Department of Political Science, University of Washington  | cadolph@uw.edu | | |
| Kenya Amano  | Department of Political Science, University of Washington  | kamano@uw.edu | | |
| Bree Bang-Jensen  | Department of Political Science, University of Washington  | breebj@uw.edu | @breebangjensen | |
| Nancy Fullman  | Department of Health Metrics Sciences, University of Washington | nf4@uw.edu | @nwnancy | |
| Beatrice Magistro  | Department of Political Science, University of Washington | magistro@uw.edu | @BeaMagistro | |
| Grace Reinke  | Department of Political Science, University of Washington | reinkeg@uw.edu | | |
| Maitreyi Sahu | Department of Health Metrics Sciences, University of Washington | msahu@uw.edu | | |
| John Wilkerson  | Department of Political Science, University of Washington  | jwilker@uw.edu | | |



## Terms of Use:
This GitHub repo and its contents herein, including all data, mapping, and analysis, copyright 2020 by the COVID-19 State Policy Team, all rights reserved, is provided to the public strictly for educational and academic research purposes.  The Website relies upon publicly available data from multiple sources, that do not always agree. The COVID-19 State Policy Team hereby disclaims any and all representations and warranties with respect to the Website, including accuracy, fitness for use, and merchantability.  Reliance on the Website for medical guidance or use of the Website in commerce is strictly prohibited.
