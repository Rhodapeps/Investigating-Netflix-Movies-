# Netflix Movie Analysis 🎥📊

This project analyzes Netflix movie data to explore trends in movie durations over the years and provides visual insights into the dataset. The analysis includes line plots, scatter plots, and filtering techniques to uncover patterns in the data.

---

## 📌 Features

1. **Line Plot of Movie Durations (2011-2020):**  
   Visualizes the trend of average movie durations over the years.
   
2. **Scatter Plot of Movie Durations by Release Year:**  
   Explores the relationship between release year and movie duration.
   
3. **Genre-Based Color Coding:**  
   Highlights specific genres (e.g., Children, Documentaries, Stand-Up) in the scatter plot.
   
4. **Filtering Short Movies:**  
   Identifies movies with durations shorter than 60 minutes.

5. **Exploratory Data Analysis:**  
   Subsets and inspects key columns like title, country, genre, release year, and duration.

---

## ⚙️ Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.x
- Pip (Python package manager)

### Setup Instructions

1. **Clone the Repository**  
   Open a terminal and run:
   ```sh
   git clone https://github.com/Rhodapeps/netflix-movie-analysis.git
   cd netflix-movie-analysis

2. **Install Required Libraries**
    Install the necessary Python libraries using pip:
```python
pip install pandas matplotlib
```
3. **Add the Dataset**
   Place the netflix_data.csv file in the datasets/ directory. If the directory does not exist, create it:
```python
mkdir datasets
```
4. **Run the Script**
   Execute the Python script to generate visualizations and insights:
```python
python netflix_movie_analysis.py
```

---

## 🛠 Usage

After running the script, the following visualizations and outputs will be generated:

1. **Line Plot:** Average movie durations from 2011 to 2020.

2. **Scatter Plot:** Movie durations by release year.

3. **Genre-Based Scatter Plot:** Color-coded scatter plot based on movie genres.

4. **Filtered Data:** Movies shorter than 60 minutes.


---

## 📊 Visualizations and Insights

### 1. ** Netflix Movie Durations (2011-2020)**

This line plot shows the trend of average movie durations over the years.

```python
plt.plot(durations_df['years'], durations_df['durations'])
plt.title("Netflix Movie Durations 2011-2020")
plt.show()
```
**Insight:**
The average movie duration has decreased slightly over the years, from 103 minutes in 2011 to 90 minutes in 2020.

### 2. ** Movie Duration by Year of Release**

This scatter plot visualizes the duration of individual movies by their release year.

```python
plt.scatter(netflix_movies_col_subset["release_year"], netflix_movies_col_subset["duration"])
plt.title("Movie Duration by Year of Release")
plt.show()
```

**Insight:**
While most movies cluster around 90-120 minutes, there are outliers with much shorter or longer durations.

### 3. ** Short Movies (< 60 Minutes)**
Movies with durations shorter than 60 minutes are filtered and displayed.

```python
short_movies = netflix_movies_col_subset[netflix_movies_col_subset['duration'] < 60]
print(short_movies[0:20])
```

**Insight:**
Short movies are often documentaries or children’s content.

### 4. **Genre-Based Scatter Plot**
This scatter plot uses color coding to highlight specific genres:

- **Red:** Children
- **Blue:** Documentaries
- **Green:** Stand-Up
- **Black:** Other genres

```python
plt.scatter(netflix_movies_col_subset["release_year"], netflix_movies_col_subset["duration"], c=colors)
plt.title("Movie Duration by Year of Release")
plt.xlabel("Release Year")
plt.ylabel("Duration (min)")
plt.show()
```

**Insight:**
- Children’s movies tend to have shorter durations.
- Documentaries and Stand-Up specials vary widely in duration.

---

## 📈 Key Findings

- **Are movies getting shorter?**
The trend suggests a slight decrease in average movie duration, but the answer is inconclusive ("maybe").

- **Genre-specific patterns:**
Children’s movies are consistently shorter, while other genres show more variation.

- **Short movies:**
Movies under 60 minutes are rare and often belong to specific genres like documentaries or children’s content

---

## 📂 Project Structure

```text
netflix-movie-analysis/
├── datasets/
│   └── netflix_data.csv          # Netflix dataset
├── reports/
│   └── images/                   # Visualization images
├── netflix_movie_analysis.py     # Main analysis script
├── [README.md](http://_vscodecontentref_/0)                     # Documentation
```

---

## 📄 License

This project is licensed under the MIT License..

---

## 🔗 References

- **Netflix dataset:** Netflix Movies and TV Shows Dataset

