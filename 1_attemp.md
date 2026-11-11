# Assignment 2: Attempt Before AI (Diagnosis & Plan)

 Part 1: Dataset Diagnosis (`teaching_prices_messy.csv`)
Before using any AI tool, I inspected the dataset using Python (`df.info()`, `df.isnull().sum()`, and `df.describe()`). The following problems were identified:
1. Missing Values: Found NaN entries in the `price` column for specific rows.
2. Data Type Mismatch:The `date` column was stored as an object/string instead of a datetime format.
3. Outliers / Typos: Extreme outlier values present in the `price` column (e.g., negative prices or implausibly high figures due to data entry errors).
4. Formatting Inconsistencies:Extra whitespace in text columns like `item_name`.

 Part 2: Planned Decisions Matrix
| Issue Found | Planned Decision | Reason / Justification |
| Missing `price` values | Exclude | Rows with missing target variables cannot be reliably imputed without introducing bias. |
| Text whitespace in `item_name` | Correct | Standardizing text formatting is necessary for accurate grouping. |
| Extreme price outliers | Investigate / Flag | Check if outliers are genuine market spikes or data entry errors before removing. |
| Date string format | Correct | Convert to datetime to enable correct chronological sorting and filtering. |

## Part 3:Snapshot Code

567d8ec
