# Flight Distance Analysis

## Overview
Case study for my recruitment process analyzing air travel data to verify the accuracy of the distances between departure and arrival destinations.

### Columns names explained:
- `dep_coords`/`arr_coords`: Coordinates of airports of departure/arrival calculated using an external database.
- `dep_coords_original`/`arr_coords_original`: Original departure/arrival coordinates provided for the test.
- `distance_in_miles_calculated_with_original_coords`: Distance in miles calculated using original departure/arrival coordinates provided for the test.
- `distance_in_miles_calculated_between_airport_codes`: Distances calculated based on `dep_coords` and `arr_coords` (external database).
- `distance_diff`: Absolute value of the distance difference.

### Conclusion:
1. **Data inconsistencies**: Many of the provided coordinates don't match the airports codes (as shown in an earlier submitted PDF file), indicating errors in the input data or outdated information.
2. **Distance differences**: There are significant differences between distances calculated using provided coordinates and distances calculated using actual coordinates of airports. This suggests errors in provided airport codes or coordinates.

For further analysis, it should be considered to include a margin of error due to rounding in the provided latitude of departure (`dep_coords_original`). Rounding to one decimal place can cause deviations in distance calculations, which is unwanted because it compromises the reliability of the comparison and could distort the distance measurements.

Overall, all of the above aspects make it impossible to reliably check whether carriers are intentionally extending their quoted mileage for routes. There's a clear need for more rigorous verification of the data used for calculations.

### Useful Links and References:
* [Getting distance between two points based on latitude/longitude](https://stackoverflow.com/questions/19412462/getting-distance-between-two-points-based-on-latitude-longitude)
* [Airport codes](https://www.ccra.com/airport-codes/)
* [Get address from given coordinate using python](https://stackoverflow.com/questions/60928516/get-address-from-given-coordinate-using-python)
* [How to Use SQL in pandas Using pandasql Queries](https://www.datacamp.com/tutorial/how-to-use-sql-in-pandas-using-pandasql-queries)
* [Using an API to calculate distance between two airports](https://stackoverflow.com/questions/37572731/using-an-api-to-calculate-distance-between-two-airports-two-columns-within-r)
* [Database of airports](https://raw.githubusercontent.com/jpatokal/openflights/master/data/airports.dat)
