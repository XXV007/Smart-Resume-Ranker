Smart Resume Ranker

 

A simple AI/ML-powered tool to automatically rank candidate resumes against a given job description using NLP techniques (TF-IDF & Cosine Similarity). Ideal for recruiters and hiring managers to streamline the screening process.

📋 Table of Contents

Features

Project Structure

Getting Started

Prerequisites

Installation

Usage

Example

Configuration

Extending the Project

Contributing

License

Acknowledgements

✨ Features

Resume Parsing: Extract text from PDF and DOCX files.

NLP Preprocessing: Clean and normalize text data.

TF-IDF Vectorization: Convert resumes and job description into feature vectors.

Similarity Scoring: Compute cosine similarity between job description and each resume.

Ranking & Insights: Display ranked list and top keywords driving each score.

🗂️ Project Structure

smart-resume-ranker/
├── data/                   # Sample resumes & job descriptions
├── notebooks/              # Google Colab notebook for interactive demo
│   └── Smart_Resume_Ranker.ipynb
├── src/                    # Core Python scripts if using .py mode
│   ├── parser.py           # Functions to extract text from resumes
│   ├── ranker.py           # Vectorization & ranking logic
│   └── main.py             # Example CLI or script entrypoint
├── requirements.txt        # Python dependencies
├── README.md               # Project overview & instructions
└── LICENSE                 # MIT License

🚀 Getting Started

Follow these steps to set up and run the Smart Resume Ranker.

Prerequisites

Python 3.8 or higher

pip (Python package installer)

Installation

Clone the repository

git clone https://github.com/<your-username>/smart-resume-ranker.git
cd smart-resume-ranker

Create & activate a virtual environment (optional but recommended)

python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

Install dependencies

pip install -r requirements.txt

Usage

You can choose between two workflows:

1. Google Colab Notebook

Open notebooks/Smart_Resume_Ranker.ipynb in Google Colab.

Run Runtime → Run all to execute all cells.

Upload your resumes when prompted.

View the ranked output and keyword insights.

2. Local Script Mode

If you prefer working locally with .py scripts:

# Run the main script (example)
python src/main.py \
  --jd "path/to/job_description.txt" \
  --resumes "data/resumes/*.pdf" \
  --top_n 5 \
  --threshold 0.1

📝 Example

Sample output in Colab:

Filename

Score

Top Keywords

Alice_Software_Engineer.pdf

0.85

python (0.60), nlp (0.52), tensorflow (0.48)

Bob_Data_Scientist.docx

0.78

sklearn (0.55), machine (0.49), learning (0.47)

⚙️ Configuration

top_n: Number of top keywords to extract per resume (default: 5)

threshold: Minimum similarity score to include resume in final list (default: 0.0)

Stop Words: Currently using English stop words via scikit-learn’s TF-IDF. You can customize the stop word list.

🔧 Extending the Project

BERT Embeddings: Use sentence-transformers to compute semantic embeddings for deeper matching.

Web UI: Build a Flask or Streamlit frontend for interactive uploads and live ranking.

Batch Processing: Integrate with cloud storage (AWS S3, GCS) to process large resume batches.

Database Integration: Store results in a database (PostgreSQL, MongoDB) for audit and history.

🤝 Contributing

Contributions are welcome! Please follow these steps:

Fork the repository

Create a feature branch (git checkout -b feature/YourFeature)

Commit your changes (git commit -m 'Add feature')

Push to your branch (git push origin feature/YourFeature)

Open a Pull Request

📜 License

This project is licensed under the MIT License. See LICENSE for details.

🙏 Acknowledgements

Scikit-learn for TF-IDF & similarity metrics

pdfminer.six for PDF parsing

python-docx for DOCX parsing

Inspiration: Automated screening tools in HR tech
