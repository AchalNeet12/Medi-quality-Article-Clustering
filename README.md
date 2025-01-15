# Medi quality Article Clustering
---

### 📜 Description and Overview

- **Medi-quality-Article-Clustering** is a machine learning-based project aimed at clustering and analyzing medical articles to uncover patterns and generate meaningful insights. By leveraging natural language processing (NLP) techniques and unsupervised learning algorithms, the project organizes a large corpus of medical texts into distinct groups or clusters. This categorization facilitates easier analysis, exploration, and visualization of the articles, aiding researchers and professionals in gaining a deeper understanding of the content.
---
### 📦 Dataset

The dataset used in this project comprises XML files containing multiple medical articles. Each XML file has structured information, including text enclosed in specific tags. The dataset includes:
- A minimum of 15 XML files.
- Each XML file contains several paragraphs of text, usually under tags like `<para>`.
---
### 🤖 Technology Used

**Libraries and Tools:**
- **Python:** The core programming language for the project.
- **Pandas and NumPy:** Used for data manipulation and numerical operations.
- **BeautifulSoup:** For parsing XML files and extracting relevant text.
- **NLTK and spaCy:** For natural language processing tasks like tokenization, lemmatization, and stopword removal.
- **scikit-learn:** Used for vectorization, TF-IDF transformation, clustering with KMeans, and other machine learning operations.
- **Matplotlib and WordCloud:** For visualizing the clustering results and generating word clouds.
- **Streamlit:** For creating an interactive frontend dashboard.
---
### ⚙ Model

**KMeans Clustering:**
- The project employs KMeans clustering to categorize articles into distinct clusters based on their content similarity.
- The number of clusters is determined using the Elbow Method, which identifies the optimal number of clusters by minimizing within-cluster sum-of-squares (WCSS).
---
### 🔍 Data Preprocessing

**Steps Involved:**
1. **XML Parsing:**
   - The XML files are parsed using `xml.etree.ElementTree` and `BeautifulSoup` to extract the text content from `<para>` tags.

2. **Text Cleaning:**
   - Removal of special characters, numeric references, and punctuation.
   - Conversion to lowercase and removal of stopwords using NLTK's stopword list.
   - Lemmatization using `WordNetLemmatizer` to reduce words to their base forms.

3. **Vectorization and TF-IDF Transformation:**
   - The cleaned text data is vectorized using `CountVectorizer` and transformed into TF-IDF representation.
   - The resulting matrix is normalized to ensure consistent scaling for clustering.
---
### 📚 Backend Code

The backend involves:
- **File Uploading and Parsing:** Users upload XML files through the Streamlit interface. The uploaded files are parsed, and text is extracted.
- **Data Cleaning and Preprocessing:** Functions are implemented to clean and preprocess the text data, including stopword removal, lemmatization, and vectorization.
- **KMeans Clustering:** The processed text data is clustered using the KMeans algorithm, with the optimal number of clusters determined by the Elbow Method.
- **Visualization:** Word clouds are generated for each cluster to visualize the most frequent terms.
---
### 🌐 Frontend

The frontend is built using Streamlit, providing an interactive dashboard with the following features:
- **File Uploader:** Allows users to upload multiple XML files.
- **Elbow Method Visualization:** Displays an interactive plot to help users determine the optimal number of clusters.
- **Cluster Selection:** Users can select the number of clusters for KMeans clustering.
- **Word Cloud Generation:** Displays word clouds for each cluster, providing a visual summary of the main topics.
---
### 📈 Results

**Cluster Visualization:**
- The project outputs clusters of medical articles, each represented by a word cloud. These visualizations highlight the most prominent terms in each cluster, aiding in the identification of underlying themes.
- The clustering results are displayed in a DataFrame, with each article assigned to a specific cluster.
---
### 🎯 Conclusion

The **Medi-quality-Article-Clustering** project successfully demonstrates the power of machine learning and NLP in organizing and analyzing large collections of text data. By automating the clustering of medical articles, the project provides a valuable tool for researchers and professionals to quickly identify patterns, trends, and themes in the literature. The interactive dashboard enhances the user experience, making it accessible and easy to use for individuals without deep technical expertise.

