# germany-53-21-districts

--- this is an updated version of germany-53-17-districts using 2021 counties ---

This repository provides historic, comparable county-level election results for West Germany. The final dataset contains estimates for the vote share for each election since 1953 (within the boundaries of the 2021 counties). The conversion of past into current counties benefits from the way that German counties were modified: Usually two or more old counties were merged entirely into a new one.

In order to convert historic election results into the 2021 counties, I use geodata. More specifically, I calculate the share of historic counties that lie within the boundaries of 2021 counties. Subsequently, I multiply these shares with the election results of each year. This requires the assumption, that the vote share was distributed equally throughout the county. Note that the geographical share of a county is different to the population share of a county. The geographical changes are likely greater than the actual population changes as county borders are more likely redrawn in rural, less densely populated areas.

This repository also contains the conversion tables of (West) German districts (Landkreise und kreisfreie Städte) since 1953. The columns correspond to the 2021 counties, whereas the rows correspond to the counties of the specific year.

The final dataset "election-results-53-21.dta" contains the vote share for all major parties for each election since 1953. Counties can be merged to other data on the county level using the ID (AGS, Allgemeiner Gemeindeschlüssel).

### Example: Recklinghausen

In order to demonstrate the logic behind the conversion, the following image illustrates the conversion of 1953 counties to the 2021 county "Recklinghausen" (in red). We can see that most 1953 counties were almost entirely merged into the new county. Recklinghausen (2021) is made up of the former counties Recklinghausen, Stadt (1953), Recklinghausen (1953), Gladbeck (1953), and Castrop-Rauxel (1953).  For each of these counties, more than 90% of the former county area is now part of the new county. Only small fractions of other adjacent counties were added to the newly formed county. This is a pattern that can be observed throughout West Germany: tow or more smaller counties are merged into larger ones, often cities and the surrunding rural areas are combined. 

*Example of conversion of old into new counties for the county "Recklinghausen*
<img src="https://github.com/cornelius-erfort/germany-53-21-districts/raw/main/plots/conversion_example.png" width="80%">

## Measurement validity

The following map shows the 1953 West German counties. The color shading indicates the size of the largest chunk of old county that was incorporated into a new county. 100% or "dark green" signifies that the entire county was incorporated into a new one. Smaller percentages indicate that the county was broken up into smaller fragments with negative consequences for the validity of the measurement.

<!--- *Conversion of 1953 into 2021 counties: Share of largest coherent part of old county in new county*
<img src="https://raw.githubusercontent.com/cornelius-erfort/germany-53-21-districts/main/plots/coverage_map_1953-2021.png" width="80%"> --->

### Correlation of registered voters

The following graph shows the correlation of registered voters over time. There seem to be no sudden changes in the size of the electorate suggesting that the conversion works quite well.

*Correlation of the number of registered voters over time*
<img src="https://github.com/cornelius-erfort/germany-53-21-districts/raw/main/plots/corrgram_registered_voters.png" width="80%">

### Correlation of CDU/CSU vote share

The same applies to the correlation of the CDU/CSU vote share.

*Correlation of the CDU/CSU vote share over time*
<img src="https://github.com/cornelius-erfort/germany-53-21-districts/raw/main/plots/corrgram_CDU.png" width="80%">




### Author
- **Cornelius Erfort**  
  Post-doctoral Researcher  
  University of Witten/Herdecke  
  Department of Philosophy, Politics, and Economics  
  Alfred-Herrhausen-Straße 50, 58455 Witten, Germany  
  [cornelius.erfort@uni-wh.de](mailto:cornelius.erfort@uni-wh.de)  
  [ORCID: 0000-0001-8534-7748](https://orcid.org/0000-0001-8534-7748)

This work was supported by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) – 390285477/ GRK 2458.
