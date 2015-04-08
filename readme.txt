README

The Centers for Medicare and Medicaid Services posts statistics on Hospital-Acquired Conditions, sometimes known as Healthcare-Associated Infections, on several websites. The most prominent is Hospital Compare:

https://data.medicare.gov/data/hospital-compare

The tables available there include:
- Healthcare Associated Infections - Hospital
- Healthcare Associated Infections - National
- Healthcare Associated Infections - State
- Hospital-Acquired Condition Reduction Program

The last is the single most useful table concerning hospital-acquired conditions in Hospital Compare. It requires little manipulation beyond sifting among the hospitals in your state.

The Healthcare Associated Infections website in Hospital Compare contains data on six conditions. Unfortunately, it is organized so that the reader has to scan six lines to get data for a single condition for a single hospital; the key data point for any condition is the "SIR" (Standardized Infection Ratio) on a 0-to-10 scale.

The Hospital-Acquired Condition Reduction Program website is simpler, though it contains less data. The user gets all the information for a single hospital in one line. 

For those who know how to use database software, the best bet is to use CMS reference files or the cleaned versions I'm making available here. CMS provides a frequently updated list of hospitals that accept Medicare here:

https://data.medicare.gov/Hospital-Compare/Hospital-General-Information/xubh-q36u

I've provided a cleaned version:

Hospital_Reference_2015.txt  

It includes latitudes and longitudes for virtually every hospital in the U.S., which should make mapping easy. The lat/longs are hard to extract from the original file.

CMS posts the raw HAC scores -- just the hospital ID numbers (CCN), each hospital's score on a 1-to-10 best-to-worst scale and a Y or N indicating whether they were in the worst quartile (earning a 1 percent penalty). You can find those scores online at this site:

http://www.cms.gov/Medicare/Medicare-Fee-for-Service-Payment/AcuteInpatientPPS/downloads/FY2015-FR-Table17.zip

Or you can get that data right here: HAC_Raw_Scores.txt 

I've combined the raw data and the cleaned up hospital reference and put them in this file: 

HAC_Hospital_Basic_Scores.txt

You will need to filter by state and possibly by county to find the hospitals you want. This file just lists the raw HAC score and a Y or N indicating whether a hospital was in the worst quartile.

If you want to know how hospitals did on CLASBI, CAUTI and the rest, I combined the CMS file with my cleaned up hospital reference file to produce this file:

HAC_Hospital_Detailed_Scores.txt