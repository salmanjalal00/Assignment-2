# Assignment 2: Cleaning Court Log & Reflection

Cleaning Code Court Verdicts

| AI Code Line / Suggestion | Verdict (Keep / Modify / Reject) | Evidence & Explanation |
| :--- | :--- | :--- |
| `df.fillna(df.mean(), inplace=True)` | **Reject** | Filling missing prices with the mean distorts price variance and item-specific trends. |
| `df['item_name'] = df['item_name'].str.strip()` | **Keep** | Verified before-and-after string lengths; safely removes trailing whitespace without altering labels. |
| `df = df[df['price'] > 0]` | **Keep** | Correctly removes invalid negative prices identified during the manual diagnosis phase. |

---

 Reflection

Differences from AI: The AI initially suggested filling all missing numerical values with column means. My decision differed because doing so on item-level prices creates false data points that distort individual item trends. Keeping rows with valid recorded prices or dropping unrecoverable records was better supported.
What would have been missed alone: Working alone, I might have spent significantly more time writing complex regex to clean text formatting inconsistencies. The AI provided quick, syntax-efficient string methods that sped up the cleaning process, provided every line was audited and understood.
