<h1 align="center">Hi, I'm Arun 👋</h1>

<p align="center">
  <b>MS Data Analytics Engineering @ Northeastern University</b> · May 2026 · GPA 3.8<br/>
  AI Engineer · Data Scientist · ML Engineer · BI Developer<br/>
  📍 Boston, MA · Open to full-time roles & relocation
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/arun-valliappan-990334263/">
    <img src="https://img.shields.io/badge/LinkedIn-Arun%20Valliappan-0077B5?style=flat-square&logo=linkedin"/>
  </a>
  <img src="https://img.shields.io/badge/GPA-3.8%2F4.0-brightgreen?style=flat-square"/>
  <img src="https://img.shields.io/badge/Open%20To-Full%20Time%20Roles-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Location-Boston%2C%20MA-orange?style=flat-square"/>
</p>

---

## About Me

I build end-to-end AI and data systems — from raw data pipelines to deployed products. My work spans **RAG systems and LLM applications**, **deep learning and computer vision**, **NLP and transformers**, **BI dashboards and analytics**, and **geospatial data science**. I care about measurable results — every project I build gets evaluated, not just demoed.

Previously a **Data Analyst at Cholamandalam Investment & Finance** and **Data Analyst Intern at Pon Pure Chemicals**.

---

## Featured Projects

### 🤖 AI & LLM Systems

---

#### 💊 [PharmaRAG](https://github.com/v-arun2002/pharma-rag) — FDA Drug Label Intelligence
> Production-grade RAG chatbot over 22 FDA oncology drug labels

![Faithfulness](https://img.shields.io/badge/RAGAS%20Faithfulness-0.939-brightgreen?style=flat-square)
![Answer Relevancy](https://img.shields.io/badge/Answer%20Relevancy-0.871-green?style=flat-square)
![Context Recall](https://img.shields.io/badge/Context%20Recall-0.722-yellowgreen?style=flat-square)

- Section-aware FDA label parsing → 6,328 dense vector chunks in **FAISS IndexFlatIP**
- **Cross-encoder re-ranking** (top-20 → top-5) via ms-marco-MiniLM
- **Semantic cache** with FAISS similarity lookup at 0.92 cosine threshold
- **LangGraph single-agent** with citation-grounded Groq llama-3.3-70b inference
- Full **RAGAS evaluation** — faithfulness 0.939 means 93.9% of claims trace to source

`FAISS` `BAAI/bge-small` `Cross-Encoder` `LangGraph` `Groq` `RAGAS` `Streamlit`

---

#### 📈 [FortuneRAG](https://github.com/v-arun2002/fortune-rag) — Fortune 500 Financial Intelligence
> Serverless RAG pipeline over SEC EDGAR filings and Yahoo Finance data — built on AWS

- **AWS Step Functions** orchestrating: web scraping → Glue ETL → Bedrock Knowledge Base sync → RAG endpoint
- Parallel Lambda scrapers for **SEC EDGAR** (10-K, 10-Q, iXBRL) and **Yahoo Finance** (financials, analyst ratings)
- **AWS Glue** jobs for HTML-to-JSON conversion and document chunking
- **AWS Bedrock** Knowledge Base with Claude for retrieval-augmented generation
- Cost-optimized: automatic S3 cleanup, Express workflows, Haiku for routine queries

`AWS Step Functions` `AWS Bedrock` `AWS Glue` `Lambda` `S3` `RAG` `Claude` `SEC EDGAR`

---

#### ⚽ [MatchAgent-AI](https://github.com/v-arun2002/MatchAgent-AI) — World Cup RAG Agent
> LangChain ReAct agent over 145 years of FIFA World Cup history

- **6-tool ReAct pipeline**: dataset discovery → data ingestion → semantic retrieval → H2H reasoning → LLM synthesis → prediction report generation
- **FAISS index** over ~900 World Cup matches embedded with all-MiniLM-L6-v2
- **ConversationBufferMemory** for coherent multi-turn sessions
- Powered by **Gemini 2.5 Flash** for synthesis and prediction generation
- Deployed via Streamlit + localtunnel

`LangChain` `ReAct Agent` `FAISS` `Gemini 2.5 Flash` `Streamlit` `Pandas`

---

### 🧠 Deep Learning & Computer Vision

---

#### 👗 [Fashion Diffusion Model](https://github.com/v-arun2002/Fashion_Diffusion_Model) — Text-to-Image Generation
> Systematic evaluation of Stable Diffusion v1.5 vs Kandinsky v2.2 for fashion product synthesis

- **Best config**: SD v1.5 · Guidance Scale 9.0 · 50 steps · Euler scheduler → **FID: 185.22 · CLIP: 0.401**
- Grid search across guidance scales (7.5, 9.0, 12.0), schedulers (Euler, DDIM, PNDM), inference steps (30, 50)
- Evaluated on 4,000-sample fashion dataset using **CLIP Score, FID, and Inception Score**
- **Gradio web UI** for real-time interactive prompt-to-image generation in Colab

`Stable Diffusion v1.5` `Kandinsky v2.2` `Hugging Face Diffusers` `CLIP` `FID` `PyTorch` `Gradio`

---

#### 🎯 [Multi-Class Object Detection](https://github.com/v-arun2002/Multi-Class-Object-Detection-Classification-using-Deep-Learning) — Celebrity Recognition
> YOLOv8 detection + VGG16 classification pipeline for celebrity face recognition

- Two-stage pipeline: **YOLOv8** for face detection bounding boxes → **VGG16** for identity classification
- Transfer learning with ImageNet pre-trained weights, fine-tuned on celebrity face dataset
- End-to-end inference: raw image → detected faces → classified identities

`YOLOv8` `VGG16` `Transfer Learning` `PyTorch` `OpenCV`

---

#### 🧠 [EEG Classification Model](https://github.com/v-arun2002/EEGClassificationModel) — Brain Signal Classification
> Deep learning for EEG signal classification across cognitive states

- CNN and LSTM architectures for time-series EEG signal processing
- Signal preprocessing: bandpass filtering, epoch extraction, normalization
- Cross-subject generalization evaluation

`PyTorch` `CNN` `LSTM` `Signal Processing` `NumPy`

---

### 🏥 NLP & Biomedical AI

---

#### 🏥 [Clinical Notes Disease Classification](https://github.com/v-arun2002/Clinical-Notes-Disease-Classification-using-NLP-Transformers) — NLP Transformers
> Multi-model NLP framework for automated disease identification from 160,000+ clinical notes

- **XGBoost on TF-IDF achieves 98.12% accuracy** — outperforming BERT, RoBERTa, BiLSTM
- Full model ladder: Logistic Regression → Random Forest → CNN → LSTM → BiLSTM → **BERT → RoBERTa → BioClinicalBERT**
- Medical abbreviation expansion (htn→hypertension, dm→diabetes mellitus), negation detection
- 10-class disease classification: cancer, hypertension, diabetes, fracture, infection and more

`BioClinicalBERT` `RoBERTa` `BERT` `XGBoost` `TF-IDF` `BiLSTM` `HuggingFace`

---

#### 🧬 [Genomic Sequencing NLP](https://github.com/v-arun2002/Genomic-Sequencing-using-NLP) — DNA Promoter Classification
> Treating DNA sequences as biological text for promoter region classification

- **CNN with one-hot encoded 6-mers achieves 91.3% accuracy** on 22,598 Drosophila sequences
- k-mer tokenization (biological equivalent of NLP n-grams), TF-IDF for classical ML
- Model comparison: Random Forest → LightGBM → LSTM → BiLSTM → **CNN**

`CNN` `BiLSTM` `k-mer tokenization` `TF-IDF` `LightGBM` `Scikit-learn`

---

### 📊 Data Analytics & BI

---

#### 🛒 [BlinkIT Sales Dashboard](https://github.com/v-arun2002/BlinkIT-Sales-Performance-Dashboard) — Power BI
> Multi-page Power BI dashboard over $1.20M in grocery sales across 8,523 transactions

- **Star schema** data model: Fact_Sales + Dim_Outlet + Dim_Item + Dim_Date
- Advanced **DAX**: time intelligence (YoY growth, SAMEPERIODLASTYEAR), RANKX, What-If parameter
- **Row-Level Security** with 3 roles filtering by outlet tier
- 4 report pages: main dashboard, drill-through outlet detail, What-If sales target analysis, executive summary
- Key insight: Supermarket Type1 drives 65% of revenue across Tier 3 locations

`Power BI` `DAX` `Star Schema` `RLS` `Power Query` `Time Intelligence`

---

#### 🚦 [Arizona Traffic Crash Analysis](https://github.com/v-arun2002/Arizona-Traffic-Crash-Analysis) — Geospatial Analytics
> 51,000+ high-severity crash records (2012–2024) analyzed for Tempe Vision Zero initiative

- **DBSCAN clustering** for hotspot detection along Southern Ave, Broadway Rd, University Dr
- Animated heatmaps, 3D hexbin density maps, treemaps, dropdown-filtered dashboards
- Evening peak (3–8 PM) identified as highest-risk window
- Interactive dashboards deployed on **AWS S3**

`GeoPandas` `DBSCAN` `Plotly` `Folium` `Shapely` `AWS S3`

---

#### 🏠 [Zillow Home Value Prediction](https://github.com/v-arun2002/Zillow-Home-Value-Project) — ML Regression
> Predicting real estate prices from 2M+ property records

- **Gradient Boosting achieves RMSE 0.0847 and R² 0.908** — best across 9 models
- 15% improvement over baseline; 12% variance reduction vs linear models
- Geospatial analysis of LA County prediction errors; full feature importance pipeline

`XGBoost` `Gradient Boosting` `GridSearchCV` `Pandas` `Scikit-learn` `Seaborn`

---

#### 🏫 [US Public School Analysis](https://github.com/v-arun2002/US-Public-School-Analysis) — Education Analytics
> 101,390 school records with advanced clustering and XGBoost prediction

- **XGBoost R² = 0.978** on enrollment prediction; GSLO identified as dominant feature (57.4% importance)
- K-Means 3-cluster solution: large schools (28K), small schools (45K), medium schools (27K)
- Full preprocessing: geographic validation, zip code standardization, IQR outlier capping

`XGBoost` `K-Means` `Seaborn` `Scikit-learn` `PCA`

---

#### 📊 [US Census Data Analysis](https://github.com/v-arun2002/US-Census-Data-Analysis) — Health Analytics
> 72,337 census tracts analyzed for health metric patterns and disease prevalence

- **Random Forest R² = 0.981** on diabetes prevalence prediction; SHAP feature importance
- ARIMA forecasting for time-series health trends; K-Means county clustering
- Strong correlations: mobility↔self-care (r=0.81), obesity↔diabetes (r=0.72)

`Random Forest` `SHAP` `ARIMA` `K-Means` `Scikit-learn` `Plotly`

---

#### 🚨 [LA Crime Data Analysis](https://github.com/v-arun2002/LACrimeDataAnalysis) — LAPD Open Data
> 890,000+ crime records from LAPD (2020–present) with time series forecasting

- **ARIMA 30-day forecast** with 60% predicted decline aligned to actual 2024 trend
- Geographic heat mapping of Downtown LA, South LA, Hollywood hotspots via Folium
- Policy impact analysis: AB 109 and Prop 47 effects on crime type distributions

`ARIMA` `Folium` `Pandas` `Matplotlib` `Time Series`

---

#### 🌱 [Carbon Emissions & Renewable Energy](https://github.com/v-arun2002/Carbon-Emissions-and-Renewable-Energy-Analysis) — Climate Analytics
> Global CO2 emission trends correlated with renewable energy adoption

- Country-level analysis of emissions vs. renewable energy share (Global Carbon Atlas)
- Sector-specific breakdown across regions; Tableau interactive dashboards
- Identified leading emitters and energy transition leaders

`Python` `Pandas` `Tableau` `Matplotlib` `Global Carbon Atlas`

---

#### 🏎️ [F1 Team Performance Tracker](https://github.com/v-arun2002/F1-Team-Performance-Tracker) — Hybrid Database System
> Full database management system for F1 performance data (2019–2023)

- **Hybrid architecture**: MySQL for structured queries + MongoDB for flexible document storage
- Complex SQL: correlated subqueries, NOT EXISTS, window aggregations across seasons
- Python analytics pipeline connecting MySQL → Pandas → Matplotlib visualizations

`MySQL` `MongoDB` `Python` `Pandas` `Matplotlib`

---

#### 👥 [Customer Segmentation Analysis](https://github.com/v-arun2002/CustomerSegmentationAnalysis) — Unsupervised ML
> Customer segment identification using clustering for targeted marketing

- K-Means + PCA for dimensionality reduction and segment visualization
- RFM (Recency, Frequency, Monetary) feature engineering
- Actionable segment profiles for marketing strategy

`K-Means` `PCA` `RFM Analysis` `Scikit-learn` `Seaborn`

---

## Skills

**AI / LLM Engineering**
`RAG Systems` `LangChain` `LangGraph` `FAISS` `Sentence Transformers` `Cross-Encoders` `RAGAS` `Prompt Engineering` `Groq` `AWS Bedrock` `Gemini` `Ollama`

**Machine Learning**
`Scikit-learn` `XGBoost` `LightGBM` `Gradient Boosting` `Random Forest` `ARIMA` `K-Means` `SHAP` `GridSearchCV`

**Deep Learning & Computer Vision**
`PyTorch` `TensorFlow` `CNN` `LSTM` `BiLSTM` `YOLOv8` `VGG16` `Stable Diffusion` `Kandinsky` `Hugging Face Diffusers`

**NLP & Transformers**
`BERT` `RoBERTa` `BioClinicalBERT` `TF-IDF` `k-mer tokenization` `HuggingFace` `spaCy`

**Data Analytics & BI**
`SQL` `Power BI` `DAX` `Tableau` `Pandas` `NumPy` `Plotly` `Seaborn` `Matplotlib`

**Databases**
`MySQL` `MongoDB` `PostgreSQL`

**Geospatial**
`GeoPandas` `Folium` `Shapely` `DBSCAN` `Plotly Maps`

**Cloud & Engineering**
`AWS (Step Functions, Bedrock, Glue, Lambda, S3)` `Docker` `Git` `Streamlit` `FastAPI` `Gradio`

---

## Experience

**Data Analyst Intern** · Pon Pure Chemicals
Data analysis, ML model development for chemical process optimization and predictive analytics pipelines

**Data Analyst** · Cholamandalam Investment and Finance
Financial data analysis, BI reporting, and lending portfolio analytics

---

## Education

**MS Data Analytics Engineering** · Northeastern University · GPA 3.8 · May 2026
*Applied Generative AI · Deep Learning for AI · Applied NLP · Data Management · Computation and Visualization*

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=v-arun2002&show_icons=true&theme=default&hide_border=true&count_private=true" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=v-arun2002&layout=compact&hide_border=true&theme=default" height="150"/>
</p>

---

<p align="center">
  <i>Open to full-time roles in AI Engineering · ML Engineering · Data Science · BI & Analytics · Boston or Remote or Relocation</i>
</p>
