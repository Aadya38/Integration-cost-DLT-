# README

## Files
- **Input Files**:
  - `sona_dep.csv`: Original input file.
  - `sona_dep1.csv`: Intermediate file after initial cleaning.
  - `sona_dep2.csv`: Intermediate file after adding suffixes to column values.

- **Output Files**:
  - `sona_dep1.csv`, `sona_dep2.csv`, `sona_dep3.csv`: Processed data saved at each stage.

## Processing Steps

1. **Initial Cleaning (sona_dep.csv -> sona_dep1.csv)**:
   - Load `sona_dep.csv` as a tab-separated file.
   - Remove the "word." prefix from the first column without affecting decimal values.
   - Save the cleaned file as `sona_dep1.csv`.

2. **Adding Suffix to Column Values (sona_dep1.csv -> sona_dep2.csv)**:
   - Load `sona_dep1.csv`.
   - Define a suffix based on the first column’s numeric prefix and append it to values in the fourth column.
   - Save the updated data to `sona_dep2.csv`.

3. **Distance Calculation (sona_dep2.csv -> sona_dep3.csv)**:
   - Load `sona_dep2.csv` with column headers `index`, `word`, `pos`, `value`, `connect`.
   - Initialize a `distance` column.
   - Calculate the distance between rows where `value` matches another row's `index` and update the `distance` column.
   - Save the final result to `sona_dep3.csv`.
