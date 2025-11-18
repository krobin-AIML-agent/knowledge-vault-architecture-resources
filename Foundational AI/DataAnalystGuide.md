# Data Analyst Micro-Steps Guide
A comprehensive operational guide to data analytics concepts before pivoting into learning AI fundamentals.

## Table of Contents
- [Foundational Mathematics & Statistics](#foundational-mathematics--statistics)
  - [Statistics and Probability](#statistics-and-probability)
  - [Algebra and Linear Algebra](#algebra-and-linear-algebra)
  - [Calculus and Discrete Mathematics](#calculus-and-discrete-mathematics)
- [Excel Fundamentals](#excel-fundamentals)
  - [Text Editing and Formulas](#text-editing-and-formulas)
  - [Functions and Lists](#functions-and-lists)
  - [Worksheets and Pivot Tables](#worksheets-and-pivot-tables)
  - [Data Formatting and Validation](#data-formatting-and-validation)
  - [Charts and Templates](#charts-and-templates)
  - [Lookup Functions, Macros, and VBA](#lookup-functions-macros-and-vba)
- [Quick Reference](#quick-reference)

---

## Foundational Mathematics & Statistics

### Statistics and Probability
**Understanding probability distributions, statistical tests, and data interpretation.**

#### Key Concepts

**Probability Distributions**
- **Normal Distribution** → Bell curve, most values cluster near the mean (e.g., height of people)
- **Binomial Distribution** → Fixed number of trials, two outcomes (success/fail). Example: coin flips
- **Poisson Distribution** → Probability of events happening in a fixed interval (e.g., calls per minute)

**Statistical Tests**
- **t-test** → Compare means between two groups (small sample sizes)
- **Chi-square test** → Compare observed vs expected frequencies (categorical data)
- **ANOVA** → Compare means of 3+ groups

**Correlation & Regression**
- **Correlation** 
  - Pearson = straight-line relationship
  - Spearman = rank-order relationship
- **Regression** → Fit a line/equation to predict one variable from another (Y = a + bX)

#### Preprocessing Emphasis
- Normalization & standardization before statistical modeling
- Detecting outliers to avoid skewed results
- Converting categorical → numerical (e.g., dummy variables) before regression

#### Operational Application: CI Workflow

**Real-World Scenario: Defect Analysis Across Shifts**

```
t-Test → Is one shift's defect rate significantly worse?
Chi-Square → Are defects by type distributed differently than expected?
Correlation → Which process inputs correlate most with defect rate?
Regression → Build predictive model: which levers matter most?
Pareto Analysis → Prioritize the "vital few" root causes
Root Cause Analysis → Dig in with Fishbone / 5 Whys
```

**Key Insights**
- t-test = means across shifts
- chi-square = counts vs. expected
- correlation/regression = inputs → outputs
- Pareto/Root Cause = prioritization & action

**Example**: Batch of 20 defects within a shift across two shifts
- One-sample vs two-sample t-test determines if shift performance differs significantly
- Chi-square captures actual vs expected from categorical standpoint (defect types)
- Multi-level correlation with multiple X variables impacts the Y variable (defect rate)

---

### Algebra and Linear Algebra
**Working with linear equations, matrices, and transformations relevant to analytics.**

#### Key Concepts

**Matrix Operations**
- **Matrix multiplication** → Combine two grids of numbers (e.g., transform coordinates)
- **Determinant** → A scalar that indicates if a system of equations has a unique solution
- **Eigenvalues/vectors** → Show "directions of stretch" in data (used in PCA to reduce dimensions)

**Solving Systems**
- **Linear systems** → Example: 2x + 3y = 10; 5x – y = 7 → solve simultaneously

#### Operational Application

**Arrays, Vectors & Dimensionality Reduction**

Understanding matrix multiplication through arrays, rows, columns:
- Use `MMULT` and `TRANSPOSE` functions in Excel
- Arrays function as vectors
- Eigenvalues show direction of stretch using PCA to denoise data

**Real-World Example: Multi-Input Optimization**
```
Given: 2x + 3y = z (two inputs evaluating sensitivity to output)
Goal: Reverse engineer the right parameter/tolerance to achieve target output
Application: Regression quantifies sensitivity of outputs to inputs
```

**CI/Finance Connection**
- **Regression** = quantify sensitivity of outputs to inputs
- **PCA** = denoise high-dimensional data to focus on what matters
- **Linear algebra** = engine underneath optimization models (like LP for CapEx selection)

---

### Calculus and Discrete Mathematics
**Learning calculus concepts (differentiation/integration) and discrete math foundations.**

#### Calculus Concepts

**Derivatives**
- **Slopes/gradients** → Derivative gives the rate of change. Example: slope of a cost curve (S-curve)
- **Partial derivatives** → Gradient in multivariable functions (used in optimization)
  - Think: weighted input and how that impacts the output

**Integration**
- **Area under a curve** → Total cost across production levels
  - Application: Capturing surplus and shortages (the delta)
  - Lean concept: Heijunka (leveling/balancing production)

#### Discrete Mathematics

**Combinatorics**
- **nCr (combinations)** → Number of ways to pick items ignoring order
  - Formula: n! / (r!(n-r)!)
  - Application: Micro-motion analysis - different ways to grab an item
  - Optimization for ergonomics AND speed
  
- **nPr (permutations)** → Number of ways to arrange items with order
  - Formula: n! / (n-r)!
  - Algorithm mindset: multiple paths to same outcome

**Graph Theory**
- **Shortest path** → Find minimum cost/distance between nodes (Dijkstra's algorithm)
  - Correlation with Manhattan/Euclidean distance
  - Related to Critical Path Method (CPM)
  
- **Adjacency matrix** → Grid showing connections in a graph (1 = connected, 0 = not)
  - Strong correlation with semantic searches

#### Data Memory Concepts
- **Bits and powers**: 3 bits = 2³ = 8 possible states
- Understanding data representation for computational efficiency

---

## Excel Fundamentals

### Text Editing and Formulas
**Basic text manipulation and formula creation within Excel.**

#### Core Text Functions

| Function | Purpose | Example |
|----------|---------|---------|
| `TRIM(text)` | Deletes extra spaces | `TRIM(" hello ")` → "hello" |
| `CLEAN(text)` | Removes nonprintable characters | Clean imported data |
| `UPPER()` / `LOWER()` / `PROPER()` | Change casing | `UPPER("hello")` → "HELLO" |
| `CONCATENATE()` / `TEXTJOIN()` | Join text values | Combine first + last name |
| `LEN(text)` | Length of string | `LEN("hello")` → 5 |
| `LEFT(text, n)` | First n characters | `LEFT("hello", 2)` → "he" |
| `RIGHT(text, n)` | Last n characters | `RIGHT("hello", 2)` → "lo" |
| `MID(text, start, num_chars)` | Extract substring | `MID("hello", 2, 3)` → "ell" |
| `TEXT(value, format)` | Reformat a number | `TEXT(0.25, "0%")` → "25%" |
| `FIND()` / `SEARCH()` | Locate text within string | Find position of substring |

#### Advanced Techniques

**Text to Columns**
- Segment, clean, trim data efficiently
- Parse delimited data (CSV imports)

**Combination Strategies**
- Use multiple text functions together
- Example: `TRIM(UPPER(LEFT(A1,10)))` for standardized codes

#### Preprocessing Best Practices
- Remove duplicates before analysis
- Trim whitespace from imported data
- Standardize formats (dates, phone numbers, IDs)
- Use data validation to constrain entry

---

### Functions and Lists
**Using built-in functions and creating structured lists for data handling.**

#### Conditional Functions

| Function | Purpose | Syntax |
|----------|---------|--------|
| `SUMIF()` | Sum values matching criteria | `SUMIF(range, criteria, sum_range)` |
| `COUNTIF()` | Count items matching criteria | `COUNTIF(range, criteria)` |
| `IF()` | Conditional logic | `IF(condition, true, false)` |
| `IFERROR()` | Handle errors gracefully | `IFERROR(value, fallback)` |

#### Advanced List Functions

**SEQUENCE Function**
- Generate automatic numbering sequences
- Useful for creating dynamic ranges
- Example: `SEQUENCE(10)` → generates 1 through 10

**Array Formulas**
- Perform calculations on entire ranges
- Dynamic array spilling in modern Excel
- Powerful for batch operations

---

### Worksheets and Pivot Tables
**Summarizing and analyzing data using pivot tables.**

#### Pivot Table Capabilities

**Aggregation & Summarization**
- Quick summaries of large datasets
- Group by categories automatically
- Calculate sums, averages, counts, etc.

**Data Exploration**
- Slice and dice data interactively
- Identify patterns and trends
- Compare across multiple dimensions

**Best Practices**
- Clean data before creating pivots
- Use appropriate aggregation functions
- Refresh pivots when source data changes
- Consider calculated fields for complex metrics

---

### Data Formatting and Validation
**Ensuring clean, consistent data entry with formatting and validation tools.**

#### Data Validation

**Dropdown Lists**
- Constrain inputs to predefined options
- Reduce data entry errors
- Maintain consistency across dataset

**Data Type Constraints**
- Number ranges (e.g., 0-100 for percentages)
- Date ranges (fiscal year boundaries)
- Text length limits

#### Conditional Formatting

**Visual Indicators**
- Color scales for heat maps
- Icon sets for KPI dashboards
- Data bars for quick comparisons

**Industrial Psychology Application**
- Use red/green thoughtfully (colorblind considerations)
- Visual hierarchy guides attention
- Consistent formatting aids cognition

---

### Charts and Templates
**Building effective charts and re-using templates for reporting.**

#### Chart Types & Use Cases

| Chart Type | Best For | Example Use |
|------------|----------|-------------|
| Line | Trends over time | Monthly sales performance |
| Bar | Categorical comparisons | Defects by product line |
| Scatter | Correlation analysis | Input vs output relationship |
| Histogram | Distribution analysis | Cycle time frequency |

#### Template Strategy

**Standardized Reports**
- Create template workbooks
- Pre-formatted charts and tables
- Formula-driven updates
- Version control for templates

**Decimal Presentation**
- Control decimal places for clarity
- Use float data types appropriately
- Consider audience needs (precision vs readability)

---

### Lookup Functions, Macros, and VBA
**Using lookup functions and automating tasks with macros and VBA scripts.**

#### Lookup Functions

| Function | Purpose | When to Use |
|----------|---------|-------------|
| `VLOOKUP()` | Vertical lookup | Traditional table lookups |
| `HLOOKUP()` | Horizontal lookup | Row-based data |
| `XLOOKUP()` | Modern lookup | Replaces VLOOKUP (more flexible) |
| `INDEX(MATCH())` | Two-function combo | Most powerful lookup method |

**INDEX/MATCH Advantages**
- No column position counting
- Can look left (VLOOKUP can't)
- More flexible for dynamic ranges
- Better performance on large datasets

#### Power Query

**ETL Capabilities**
- Extract data from multiple sources
- Transform with intuitive interface
- Load cleaned data to worksheets
- Refresh connections automatically

**Advanced Transformations**
- Conditional columns (IF logic in GUI)
- Text operations (LEFT, RIGHT equivalents)
- Merge queries (like SQL joins)
- Append queries (union data)

#### VBA & Macros

**Automation Opportunities**
- Repetitive formatting tasks
- Complex multi-step processes
- Custom functions
- Workflow orchestration

---

## Quick Reference

### Statistics Cheat Sheet

```
t-test         → Compare 2 group means (small samples)
Chi-square     → Observed vs expected frequencies
ANOVA          → Compare 3+ group means
Correlation    → Measure relationship strength
Regression     → Predict Y from X
Pareto         → 80/20 rule, prioritize vital few
```

### Excel Formula Quick Reference

```
Text:     TRIM, CLEAN, UPPER, LOWER, CONCATENATE, LEFT, RIGHT, MID
Logic:    IF, IFERROR, AND, OR, NOT
Lookup:   VLOOKUP, XLOOKUP, INDEX, MATCH
Math:     SUM, SUMIF, SUMIFS, AVERAGE, COUNT, COUNTIF
```

### Linear Algebra Applications

```
Matrix Ops     → MMULT, TRANSPOSE in Excel
PCA            → Dimensionality reduction, denoising
Optimization   → Sensitivity analysis, parameter tuning
Regression     → Foundation for predictive models
```

### Discrete Math Applications

```
Combinations   → Micro-motion analysis, task optimization
Permutations   → Process sequencing, routing
Graph Theory   → Critical Path Method, network optimization
Adjacency      → Semantic search, relationship mapping
```

---

## Learning Path

### Beginner Foundation
1. Master Excel basics (formulas, functions, formatting)
2. Understand descriptive statistics (mean, median, mode, std dev)
3. Learn basic probability distributions
4. Practice with small datasets

### Intermediate Development
1. Statistical testing (t-test, chi-square, ANOVA)
2. Correlation and regression analysis
3. Pivot tables and advanced Excel features
4. Power Query for ETL
5. Basic VBA for automation

### Advanced Mastery
1. Multivariate analysis
2. Optimization techniques
3. Predictive modeling
4. Advanced statistical methods
5. Integration with Python/R for complex analysis

---

## Operational Excellence Framework

### CI Integration Points

**Problem Solving Flow**
```
1. Define Problem     → What is the defect/issue?
2. Collect Data       → Measurements, observations
3. Analyze Data       → Statistical tests, visualization
4. Identify Root Cause → Pareto, Fishbone, 5 Whys
5. Implement Solution → Countermeasures
6. Verify Results     → Statistical confirmation
7. Standardize        → Update procedures, training
```


**Last Updated**: November 2025  
**Version**: 1.0  
**Author**: Based on operational CI/manufacturing analytics experience
