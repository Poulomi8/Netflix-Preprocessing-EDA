# Netflix-Preprocessing-EDA
Data preprocessing and EDA on Netflix  Movies &amp; TV Shows dataset using Python,  Pandas, Matplotlib and Seaborn.  Handled missing values, text cleaning,  feature extraction and data visualization.


## Netflix Movies & TV Shows
## Data Preprocessing & EDA

###  Project Overview
This notebook performs complete data 
preprocessing and exploratory data analysis 
on the Netflix Movies and TV Shows dataset
containing 8807 titles.

---

###  Problem Statement
The Netflix dataset contained multiple data 
quality issues including:
- Missing values in key columns
- Inconsistent date formats
- Mixed data in wrong columns
- Text values needing conversion
- Multiple genres in single cells

---

###  Issues Found & Solutions

#### Missing Values
| Column | Missing | Solution |
|--------|---------|----------|
| Director | 2634 (30%) | Dropped |
| Cast | 825 (9%) | Dropped |
| Country | 831 (9%) | Filled with 'Unknown' |
| Date Added | 10 | Filled with mode |
| Rating | 4 | Filled with mode |
| Duration | 3 | Filled with mode |

#### Columns Dropped
- director → 30% missing, not useful
- cast → 9% missing, too complex
- description → just text summary
- show_id → just an ID number

#### Data Type Issues Fixed
- type → Movie/TV Show converted to 0/1
- rating → TV-MA, PG-13 etc to numbers
- country → kept top 10, rest = Other
- duration → split into value and type
- date_added → extracted year and month
- listed_in → extracted main genre only

#### Special Issues Fixed
- Wrong values in rating column
  (74 min, 84 min, 66 min removed)
- Mixed date formats handled
  using format='mixed'
- Kids' TV apostrophe typo fixed

---

### Key Insights From EDA

#### Content Type
- Netflix has 70% Movies, 30% TV Shows
- Movies dominate the platform!

#### Countries
- United States produces most content
- India is 2nd largest contributor 🇮🇳
- Netflix is heavily US dominated

#### Genres
- Dramas most popular genre (1600 titles)
- Comedies 2nd (1210 titles)
- Action & Adventure 3rd (859 titles)

#### Ratings
- TV-MA most common (3200+ titles)
- Netflix targets adult audience primarily
- Content getting more mature over time

#### Correlations
- type & duration strongly related (-0.89)
- Country doesn't affect other features
- Newer content = slightly mature rating

---

### Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

###  Dataset Source
Kaggle - Netflix Movies and TV Shows
by Shivam Bansal

###  Author
Student of BSc Data Science
Poulami Bhowmick
