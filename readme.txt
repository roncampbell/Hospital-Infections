README

The Centers for Medicare and Medicaid Services posts statistics on Hospital-Acquired Conditions, sometimes known as Healthcare-Associated Infections, on several websites. The most prominent is Hospital Compare

https://data.medicare.gov/data/hospital-compare

The tables available there include:
- Healthcare Associated Infections - Hospital
- Healthcare Associated Infections - National
- Healthcare Associated Infections - State
- Hospital-Acquired Condition Reduction Program

The last is the single most useful table in Hospital Compare. It requires little manipulation beyond sifting among the hospitals in your state.

For those who know how to use database software, the best bet is to use CMS reference files or the cleaned versions I'm making available here. CMS provides a frequently updated list of hospitals that accept Medicare here:

https://data.medicare.gov/Hospital-Compare/Hospital-General-Information/xubh-q36u

"Hospital Reference 2015" is a cleaned version of this list. It includes latitudes and longitudes for virtually every hospital in the U.S., which should make mapping easy. The original file hid the lat/longs, making them a pain to extract.

CMS posts the raw HAC scores -- just the hospital ID numbers (CCN), each hospital's score on a 1-to-10 best-to-worst scale and a Y-N indicating whether they were in the worst quartile (earning a 1 percent penalty). You can find those scores online at this site:

http://www.cms.gov/Medicare/Medicare-Fee-for-Service-Payment/AcuteInpatientPPS/downloads/FY2015-FR-Table17.zip

Or you can take the data right now: HAC_Raw_Scores_2015 file.

I've combined the raw data and the cleaned up hospital reference and put them in this file:
HAC_Hospital_Basic_Scores

You will need to filter by state and possibly by county to find the hospitals you want. This file just lists the raw HAC score and a Y or N indicating whether a hospital was in the worst quartile.

If you want to know how hospitals did on CLASBI, CAUTI and the rest, I combined the CMS file with my cleaned up hospital reference file to produce this file:
HAC_Hospital_Detailed_Scores