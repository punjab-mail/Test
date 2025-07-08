**Natural Catastrophe Events Analysis**

**Project Overview**
This project focuses on building a robust pipeline to identify and classify natural catastrophe (nat-cat) events from a large and noisy dataset of news article titles. The dataset, sourced from the GDELT API, initially contained over 91,000 entries, which were filtered and cleaned down to approximately 65,000, and eventually reduced to around 20,000 after applying strict criteria for event relevance and geographic reference.

**Objectives**
**Data Preprocessing:** Clean and filter noisy news article titles to extract relevant natural disaster events.

**Exploratory Data Analysis (EDA):** Analyze the dataset's structure, distribution, and trends.

**Classification:** Implement multiple NLP and machine learning approaches to classify disaster types (e.g., earthquakes, floods, wildfires).

**Geographical Tagging:** Identify and extract geographical locations mentioned in the titles.

**Model Evaluation:** Compare the performance of different modeling techniques.

**Dataset**
The dataset consists of news article titles related to natural disasters, obtained using the GDELT API. The raw data contained duplicates, missing values, and irrelevant entries, which were cleaned and filtered to ensure high-quality inputs for analysis and modeling.

**Methodology**
Data Preprocessing
Cleaning: Removed duplicates, special characters, and unnecessary whitespace. Applied lowercase conversion, stopword removal, and lemmatization.

**Filtering:** Retained only titles with valid geographical references and disaster-related keywords.

**Exploratory Data Analysis (EDA)**
Analyzed title length, word count, and temporal trends.

Visualized data distributions using histograms, bar charts, and word clouds.

**Modeling Approaches**
TF-IDF + Logistic Regression: Traditional keyword-based labeling with TF-IDF features.

BERT Embeddings + Random Forest: Contextual embeddings for improved semantic understanding.

Zero-shot Classification: Automated labeling using a pre-trained BERT model.

Fine-tuned BERT Classifier: End-to-end learning for high accuracy.

Unsupervised Methods (KeyBERT, BERTopic): Exploratory clustering and topic modeling.

**Results**
Approach	Accuracy (Train/Test)	Remarks
TF-IDF + Logistic Regression	99% / 98%	Fast but limited semantic understanding.
BERT + Random Forest	99% / 99%	Improved contextual understanding.
Zero-shot + Logistic	~98% / 98%	Flexible labeling without manual keywords.
Zero-shot + Random Forest	~99% / 99%	Best generalization with minimal manual intervention.
Fine-tuned BERT	~99% / 99%	Highest semantic learning, best performance. Computationally intensive.
KeyBERT / BERTopic	N/A	Useful for clustering but struggles with short texts and minority classes.

**Conclusion**
The project successfully demonstrated the feasibility of using supervised and unsupervised NLP techniques for classifying natural disaster events. The fine-tuned BERT classifier and zero-shot + Random Forest combination provided the most accurate results, while unsupervised methods like BERTopic and KeyBERT were useful for exploratory analysis.

**Future Improvements**
Dataset Augmentation: Include more diverse samples for underrepresented disaster types.

Advanced Location Detection: Integrate geolocation APIs for better accuracy.

Metadata Utilization: Use article body text and timestamps to enrich features.

Class-Balancing Techniques: Address imbalance with SMOTE or focal loss.

API Deployment: Package the pipeline into a real-time API for scalable inference.

Active Learning: Implement a feedback loop for continuous model improvement.

Real-time Dashboard: Visualize categorized events on a map with alerts.

