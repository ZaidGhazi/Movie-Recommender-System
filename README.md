# Hybrid Movie Recommender System

## Overview
This project builds and evaluates a hybrid movie recommender using MovieLens-style ratings and metadata. The report compares popularity-based recommendations, content-based tag affinity, collaborative filtering with sparse SVD embeddings, and an ensemble approach to show how multiple signals can improve recommendation coverage and relevance.

## Problem Statement
Recommend movies a user is likely to enjoy by combining historical ratings, movie metadata, tag relevance, and latent collaborative patterns from a large sparse user-item matrix.

## Key Features
- Popularity baseline using Bayesian weighted scores.
- Content-based recommendations from genres, tags, and movie metadata.
- Collaborative filtering with sparse matrix construction and `TruncatedSVD` movie embeddings.
- Hybrid/ensemble recommendation comparison.
- Evaluation discussion with ranking metrics such as HitRate@10 and NDCG@10.
- Rendered report and presentation deck for portfolio review.

## Data Source
The analysis uses the MovieLens 20M dataset, including movie metadata, ratings, tags, links, genome scores, and genome tags. The raw CSV files are not committed because of size and licensing considerations. Download the dataset locally and place the CSVs in a local data directory before reproducing the notebook.

Expected CSV names:

- `movie.csv`
- `link.csv`
- `genome_scores.csv`
- `genome_tags.csv`
- `rating.csv`
- `tag.csv`

## Methods and Tools
- Python notebook rendered to HTML
- pandas, numpy, scipy, scikit-learn, matplotlib
- Sparse matrices, cosine similarity, KMeans, t-SNE, `TruncatedSVD`
- Popularity, content-based, collaborative filtering, and hybrid recommendation strategies

## How to Run Locally
The repository currently includes the rendered HTML report and presentation deck, not the original notebook source. To reproduce the analysis after adding the source notebook:

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install pandas numpy scipy scikit-learn matplotlib seaborn
```

Then copy `.env.example` to `.env`, update `MOVIELENS_DIR`, and place the MovieLens CSV files in that directory.

## Required Packages
- `pandas`
- `numpy`
- `scipy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

## Main Files to Review
- `Project_Zaid.html`: rendered final report with code, visuals, and recommender outputs.
- `Hybrid Movie Recommender System.pptx`: presentation deck.
- `.env.example`: placeholder local data directory configuration.

## Screenshots
Screenshots are not committed yet. Suggested additions:

- `screenshots/svd-tsne-movie-embeddings.png`
- `screenshots/recommender-comparison-table.png`
- `screenshots/evaluation-metrics.png`

## Limitations
- Source notebook/script is not committed, so the rendered report is reviewable but not fully reproducible from this repository alone.
- Raw MovieLens data is not committed.
- The report references local CSV filenames, so reproduction requires matching local data setup.
- Evaluation should be expanded with more users, stronger validation splits, and production-style offline ranking metrics.

## Future Improvements
- Add the source notebook or Python scripts used to generate the HTML report.
- Add `requirements.txt` and a reproducible data download/preparation script.
- Add screenshots and a concise table of headline ranking metrics.
- Add a data dictionary for the MovieLens files used.

