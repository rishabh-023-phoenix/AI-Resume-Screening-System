# AI-Based Resume Screening and Candidate Shortlisting System

An AI-powered resume screening prototype that extracts candidate information from PDF resumes, identifies relevant skills, recommends suitable job roles, and generates candidate screening scores using Natural Language Processing and Machine Learning techniques.

## Project Overview

Recruitment teams often receive large numbers of resumes, making initial candidate screening time-consuming. This project aims to streamline the initial screening process by analyzing resumes against predefined job descriptions and role requirements.

The system combines PDF text extraction, skill identification, experience detection, TF-IDF-based similarity matching, and a weighted scoring mechanism to generate structured candidate screening reports.

## Key Features

- **PDF Resume Parsing:** Extracts text from uploaded PDF resumes.
- **Skill Extraction:** Identifies technical and professional skills.
- **Experience Detection:** Extracts years of experience from resume content.
- **Job Role Recommendation:** Matches resumes with job descriptions using TF-IDF and cosine similarity.
- **Candidate Scoring:** Calculates a weighted score based on job similarity, skills, and experience.
- **Interactive Web Interface:** Provides resume screening through Gradio.
- **Human-in-the-Loop:** Keeps final recruitment decisions with human reviewers.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| PDF Processing | PDFMiner |
| NLP | TF-IDF, Regular Expressions |
| Machine Learning | Scikit-learn |
| Similarity Matching | Cosine Similarity |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Web Interface | Gradio |
| Development Environment | Google Colab |

## Candidate Scoring Method

The prototype combines three scoring components:

| Component | Weight |
|---|---:|
| Job Description Similarity | 50% |
| Skills Match | 30% |
| Experience Match | 20% |

**Final Score = (Similarity × 0.50) + (Skills × 0.30) + (Experience × 0.20)**

These weights and role requirements are configurable prototype settings, not validated hiring criteria.

## Sample Results

| Candidate Resume | Recommended Role | Similarity | Final Score |
|---|---|---:|---:|
| Data Analyst | Data Analyst | 76.43% | 88.22 |
| QA Engineer | QA Engineer | 91.37% | 95.68 |
| Software Engineer | Software Engineer | 88.20% | 90.35 |

*Results obtained using three fictional sample resumes.*

## Application Screenshot

![Resume Screening Application](screenshots/application.png)

## Dataset

The project uses a synthetic dataset containing 500 records and 8 features.

The dataset includes:
- Resume ID
- Job Role
- Years of Experience
- Skills Matched
- Education Score
- Keyword Density
- Predicted Score
- Shortlisted Status

The dataset is intended for prototype development and experimentation.

## Project Structure

```text
AI-Resume-Screening-System/
│
├── AI_Resume_Screening_System.ipynb
├── README.md
├── requirements.txt
│
├── dataset/
├── sample_resumes/
├── screenshots/
└── output/
```

## How to Run

1. Clone this repository:

   `git clone https://github.com/YOUR-USERNAME/AI-Resume-Screening-System.git`

2. Open the notebook in Google Colab.
3. Install dependencies:

   `pip install -r requirements.txt`

4. Upload the required dataset and sample PDF resumes.
5. Execute the notebook cells in order.
6. Launch the Gradio application.
7. Upload a PDF resume to generate a screening report.

## Ethical Considerations

- The system assists human reviewers and does not replace human decision-making.
- Candidate scores should not be treated as definitive hiring decisions.
- The prototype uses synthetic data and requires further validation before real-world deployment.
- Fairness, privacy, transparency, and bias evaluation remain important considerations.

## Future Enhancements

- Batch resume screening.
- Advanced NLP-based entity extraction.
- Database integration for candidate management.
- Bias auditing and fairness evaluation.
- REST API integration.
- Cloud deployment.

## Project Status

**Working Prototype — Further validation and production improvements required.**
