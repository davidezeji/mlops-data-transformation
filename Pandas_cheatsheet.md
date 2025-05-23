
# Pandas Cheat Sheet for MLOps 

## Load & Save Data

```python
import pandas as pd

# Load from CSV
df = pd.read_csv('data.csv')

# Save to CSV
df.to_csv('cleaned_data.csv', index=False)

# Load from Excel
df = pd.read_excel('data.xlsx')

# Load from SQL
df = pd.read_sql('SELECT * FROM table', connection)
```

---

## Quick Data Inspection

```python
df.head()        # First 5 rows
df.tail()        # Last 5 rows
df.info()        # Data types, non-null counts
df.describe()    # Summary statistics
df.columns       # Column names
df.shape         # (rows, columns)
```

---

## Data Cleaning

```python
df.isnull().sum()                  # Nulls per column
df.dropna()                        # Drop rows with nulls
df.fillna(0)                       # Fill nulls with 0

df['col'] = df['col'].astype(int)  # Convert type
df.rename(columns={'old': 'new'}, inplace=True)  # Rename columns
```

---

## Data Validation & Debugging

```python
df['col'].unique()            # Unique values
df['col'].value_counts()      # Frequency of values
df[df['col'] > 100]           # Filter rows
df.query("col == 'error'")    # Alternative filtering
```

---

## Merging, Joining, Comparing

```python
pd.merge(df1, df2, on='id')      # Inner join
df1.join(df2, how='left')        # Join on index
df1.equals(df2)                  # Check equality
```

---

## Grouping & Aggregation

```python
df.groupby('category').mean()              # Group & average
df.groupby(['dept', 'status']).size()      # Multi-column grouping
```

---

## Exporting for Logging/Monitoring

```python
df.to_csv('monitoring_output.csv', index=False)
df.to_json('output.json', orient='records')
```

---

## Drift & Data Quality Checks (Basic)

```python
baseline.describe()
incoming.describe()

# Compare distributions (visual)
baseline['score'].hist()
incoming['score'].hist()
```

---

## Best Practices

- Validate inputs before sending to models.
- Use `.info()` and `.describe()` in every pipeline.
- Use Pandas for fast prototyping before scaling with Spark or Airflow.