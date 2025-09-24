# EXPERIMENT-3 | JEGO MARCO E. GODOY | 2ECE-A  

---

## 🔍 Experiment Overview  

This experiment introduces the **Pandas Library** in Python.  
The goal is to apply different Pandas functions for **data loading, subsetting, slicing, and indexing**.  

This experiment comprises 2 problems:  

1. **PROBLEM 1** → Load a dataset (`cars.csv`) into a Pandas DataFrame and display the **first and last 5 rows**.  
2. **PROBLEM 2** → Use the same DataFrame (`cars`) to perform **subsetting, slicing, and indexing operations**.  

---

## ✏️ Coding Process  

### 📌 Problem 1: Load and Display Dataset  

#### Step 1: Import Pandas and load dataset  

```python
import pandas as pd
# Load the .csv file into a DataFrame named "cars"
cars = pd.read_csv('cars.csv')
cars
```

Explanation:

-import pandas as pd → loads the Pandas library.

-pd.read_csv('cars.csv') → reads the cars.csv file and stores it in the DataFrame cars.

-cars → displays the full dataset.

#### Step 2: Display first five rows

# Display the first five rows of the DataFrame

```python
cars.head()
```

Explanation:

-cars.head() → shows the first 5 rows of the dataset (index 0–4).

-Useful for quickly checking the start of a dataset.

#### Step 3: Display last five rows

# Display the last five rows of the DataFrame
```python
cars.tail()
```

Explanation:

-cars.tail() → shows the last 5 rows of the dataset.

-Useful for checking the ending records.

📌 Problem 2: Subsetting, Slicing, and Indexing

(a) First 5 rows with odd-numbered columns

# Display the first five rows with odd-numbered columns (1, 3, 5, 7, ...)
```python
odd_columns = cars.iloc[:5, ::2]
odd_columns
```

Explanation:

-.iloc[:5, ::2] → selects rows 0–4 (:5) and every second column (::2).

-This means columns 1, 3, 5, ... are included.

-Result → A smaller DataFrame with only odd-numbered columns.

(b) Row containing the model "Mazda RX4"

# Display the row that contains the Model 'Mazda RX4'
```python
cars.loc[0:0]
```

Explanation:

-cars.loc[0:0] → selects the row with index 0.

-Row 0 contains the Mazda RX4 data.

(c) Cylinders of "Camaro Z28"

```python
# Display the number of cylinders for the car model 'Camaro Z28'
cars.loc[[23], ['Model', 'cyl']]
```

Explanation:

-cars.loc[[23], ['Model', 'cyl']] → selects row 23 (Camaro Z28).

-Shows only the Model and cyl (cylinders) columns.

-Result → The number of cylinders in Camaro Z28.

(d) Cylinders and Gear type of selected models

# Display the cylinders and gear type of Mazda RX4 Wag, Ford Pantera L, and Honda Civic
```python
cars.loc[[1, 28, 18], ['Model', 'cyl', 'gear']]
```

Explanation:

-cars.loc[[1, 28, 18], ['Model', 'cyl', 'gear']] → selects rows 1, 28, and 18.

-These rows correspond to: Mazda RX4 Wag, Ford Pantera L, and Honda Civic.

-Displays only the Model, cyl (cylinders), and gear columns.

-Result → Shows how many cylinders and what gear type each model has.

🤓 Conclusion

Through this experiment, I learned how to:

1. Use Pandas to load datasets with read_csv().

2. Display parts of the dataset using .head() and .tail().

3. Perform subsetting (choosing specific rows/columns).

4. Use slicing and indexing with .iloc and .loc.

📌 Key Takeaway: Pandas makes it easy to filter, view, and manipulate tabular data efficiently.
-
🏁 End of Experiment 3
-
Thank you! 🙌
-
