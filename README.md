# Book recommender system

An applied recommender-systems study comparing user-based collaborative
filtering, item-based collaborative filtering, matrix factorisation, and a
simple ensemble on the Book-Crossing dataset.

The report walks through data quality checks, sparsity reduction, model
construction, RMSE evaluation, and example recommendations. In this experiment,
matrix factorisation achieved the strongest standalone RMSE; the unweighted
ensemble did not improve on it, highlighting why ensemble weights should be
learned rather than assumed.

**[Read the rendered report](https://tinomuzambi.github.io/BookRecommenderSystem/)**

## Reproduce the analysis

1. Install R, Quarto, `tidyverse`, and `recosystem`.
2. Download the [Book-Crossing dataset](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/).
3. Place `Books.csv`, `Ratings.csv`, and `Users.csv` in a local `data/` folder.
   The source dataset is intentionally not redistributed in this repository.
4. Run `quarto render "Book Recommender System.qmd" --to html`.

The committed `index.html` is the published, self-contained report. Generated
PDF output is intentionally not versioned so that the source and live HTML stay
canonical.

## Methods

- neighbourhood-based user and item collaborative filtering
- matrix factorisation with held-out validation
- RMSE-based model comparison
- qualitative inspection of top recommendations

Code and original prose are MIT licensed. The Book-Crossing data retains its
upstream terms and is not included here.
