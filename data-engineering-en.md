### SQL and Python Fundamentals Questions:

#### Common Aggregation Functions in SQL and Python:
- **SQL**: 
  - `SUM()`: Adds up all values in a column.
  - `AVG()`: Calculates the average of the values.
  - `COUNT()`: Counts the number of rows.
  - `MIN()`: Finds the minimum value in a column.
  - `MAX()`: Finds the maximum value in a column.
  
- **Python** (Using Pandas/Numpy):
  - `sum()`: Sums the values.
  - `mean()`: Calculates the average.
  - `count()`: Counts the number of non-NA/null entries.
  - `min()`: Finds the minimum value.
  - `max()`: Finds the maximum value.

#### Common Data Structures in Python:
- **List**: Ordered, mutable collection.
- **Tuple**: Ordered, immutable collection.
- **Dictionary**: Unordered, mutable collection of key-value pairs.
- **Set**: Unordered, mutable collection of unique elements.
- **DataFrame** (Pandas): 2D labeled data structure similar to a table.

#### Common Data Processing Techniques:
- **Data Cleaning**: Removing duplicates, handling missing values, filtering data.
- **Data Transformation**: Normalizing, encoding, or scaling features.
- **Aggregation**: Summing or averaging data points to derive insights.
- **Feature Engineering**: Creating new features from existing data.
- **Data Merging**: Joining multiple data sources.

#### When is it Appropriate to Use Distributed Processing?
- **Distributed processing** is appropriate when:
  - You have large datasets that exceed the memory of a single machine.
  - You need to process data across multiple nodes for efficiency.
  - You require high availability and fault tolerance.

---

### Databricks Questions:

#### What is the Command to Remove a File in Databricks?
```bash
dbutils.fs.rm("/path/to/file", recurse=True)
```

#### What is the Name for Databricks to Measure Computing Cost?
- **Databricks Units (DBUs)** measure the cost of using compute resources.

#### During Your Work You Need to Install a PyPi Library. What Steps Do You Take?
- Go to the Databricks **Libraries** tab.
- Search for the library in **PyPi**.
- Select the library and install it on the cluster.

#### Do You Have to Specify Which Version?
- It is optional. If a specific version is required, you can specify it.

#### Do You Need to Reboot the Cluster?
- No, Databricks handles the installation without requiring a cluster reboot.

#### What Databricks Feature Can You Use to Integrate with Git?
- **Databricks Repos** allows integration with Git-based version control.

#### Where Can I Go to Review Process Jobs?
- **Jobs** tab in Databricks, where you can monitor and manage job runs.

---

### Spark Dataframe Questions:

#### How to Add One Column to an Existing DataFrame?
```python
df = df.withColumn("new_column", lit(0))
```

#### What is the Function(s) to Replace Null Values in a Column with 0?
```python
df.fillna(0, subset=["column_name"])
```

#### What is RDD?
- **RDD** (Resilient Distributed Dataset) is the core abstraction in Spark, representing an immutable, distributed collection of objects that can be processed in parallel.

#### Which SQL Keywords Can Be Used to Append New Rows to an Existing Delta Table?
- **`INSERT INTO`** can be used to append new rows to an existing Delta table.

#### Differences Between Structured Data vs Unstructured Data?
- **Structured Data**: Organized in a predefined schema (e.g., databases, spreadsheets).
- **Unstructured Data**: Lacks a predefined structure (e.g., images, videos, text).

#### The Most Used Supervised Learning Algorithms Are:
- **Linear Regression**
- **Logistic Regression**
- **Support Vector Machines (SVM)**
- **Decision Trees**
- **Random Forests**

#### Is K-Means a Type of Supervised or Unsupervised Learning?
- **K-Means** is an **unsupervised learning** algorithm used for clustering.

#### Describe the Medallion Architecture:
- The **Medallion Architecture** refers to a **multi-layered architecture** in which data is organized into Bronze, Silver, and Gold layers:
  - **Bronze**: Raw data.
  - **Silver**: Cleaned and enriched data.
  - **Gold**: Aggregated data used for analytics and reporting.

---

### BONUS:

#### What is DAG in Data Engineering?
- **DAG** (Directed Acyclic Graph) is a data structure used in Spark to represent the sequence of transformations to be executed on data. It is used to schedule and optimize the execution plan.

#### What is Spark Core?
- **Spark Core** is the foundation of Apache Spark, providing essential functionalities like task scheduling, memory management, fault recovery, and distributed storage.