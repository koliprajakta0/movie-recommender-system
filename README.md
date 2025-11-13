# 🎬 Movie Recommender System

This project presents a **scalable, intelligent, and user-friendly Movie Recommender System** built using Python. It leverages data from the **MovieLens dataset**, applying various recommendation techniques to deliver personalized and relevant movie suggestions. The system was developed without relying on `scikit-surprise` or `conda`, making it lightweight and easy to run across platforms.

---

## 🎯 Objective

The goal of this project is to create a recommendation engine that helps users discover movies aligned with their interests by analyzing:

- Movie metadata (genres, overviews, cast, crew)
- User ratings and popularity metrics
- Text content using NLP (Natural Language Processing)

This project implements:
- 📊 **Popularity-Based Filtering**
- 🧠 **Content-Based Filtering**
- 🔥 **Custom Hype Score Metric**

---

## 🚀 Key Features

- ✅ Personalized movie recommendations using content similarity
- 📈 Popularity-based suggestions using vote averages and vote count
- 🔥 Custom "Hype Score" combining rating & popularity for trending insights
- 📊 Visualizations: Hype Score bar charts and EDA charts using Matplotlib
- 🧹 Data cleaning and preprocessing of large movie metadata
- 🖼️ Extraction of genres, keywords, cast, and crew using JSON parsing
- 🧠 NLP with TF-IDF Vectorization for content-based filtering
- 📦 No heavy dependencies (no `scikit-surprise`, no `conda`)

---

## 🧠 Methodologies Used

### 1. Popularity-Based Filtering
Recommends movies that are globally well-rated using:
```python
Weighted Rating = (v / (v + m)) * R + (m / (m + v)) * C
Where:

R = average rating for the movie

v = number of votes for the movie

m = minimum votes required

C = mean vote across the dataset

2. Content-Based Filtering
TF-IDF is applied to the movie overviews

Cosine Similarity is used to find movies with similar textual descriptions

3. Custom Hype Score
Calculated as:

python
Hype Score = vote_average × log10(vote_count + 1)
This boosts movies that are both popular and high quality.

📁 Project Structure

movie-recommender-system/
├── movies_metadata.csv          # Movie metadata dataset
├── ratings_small.csv            # Ratings subset
├── app.py / notebook.ipynb      # Main implementation code
├── hype_chart.png               # Bar chart of top hyped movies
├── README.md                    # Project documentation
📊 Exploratory Data Analysis (EDA)
Distribution of movie ratings

Number of ratings per movie

Descriptive statistics of the ratings dataset

Cluster visualization with random sample preferences

📦 Libraries Used
pandas – for data loading and processing

numpy – numerical operations

matplotlib, seaborn – data visualization

scikit-learn – TF-IDF vectorization and cosine similarity

ast – parsing JSON-like strings in CSV files

math – for distance calculations and score formulas

▶️ How to Run
Clone this repository:


git clone https://github.com/your-username/movie-recommender-system.git
cd movie-recommender-system
Install the required packages:


pip install -r requirements.txt
Run the code:

Use jupyter notebook or VS Code to run notebook.ipynb

Or run a script like:


python app.py
📌 Dataset Source
The dataset used in this project is from the MovieLens GroupLens Project.

🔮 Future Enhancements
🎯 Collaborative Filtering for deeper personalization

🌐 Flask/Streamlit web interface for real-time recommendations

🕒 Time-based filtering (e.g., recent trends, release years)

👤 User login and saved preferences

📱 Integration with movie APIs (TMDB, OMDB)

🙏 Acknowledgements
This project was completed independently by Prajakta Koli as a hands-on learning initiative. It provided valuable experience in data preprocessing, recommendation systems, visualization, and Python programming.

📇 Contact
📧 Email: koliprjkt@gmail.com

📞 Phone: +91 9359988469

[LinkedIn Profile](https://www.linkedin.com/in/prajaktakoli)

