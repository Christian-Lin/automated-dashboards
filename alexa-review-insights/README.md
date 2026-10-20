# Alexa Review Insights

An interactive dashboard of 2,435 de-duplicated Amazon reviews of Echo and Fire TV Stick products (May–July 2025), showing which product lines draw the most negative (1–2 star) reviews.

**Live page:** https://christian-lin.github.io/automated-dashboards/alexa-review-insights/

## What's here

- `index.html` – the whole dashboard in one self-contained file. React 18 and Tailwind CSS load from a CDN; the review data is embedded in the page, so it needs no server or build step.
- `reviews_cleaned.csv` – the cleaned dataset behind it.

## Features

- Headline figures: unique reviews, average rating, share negative, share 5-star
- Negative-review rate by product line (click a bar to filter the whole page)
- Rating mix and median review length by star rating
- Searchable, sortable review table with a "negative only" toggle
- Light and dark mode follow the system setting

## Data notes

- Exact duplicate rows were removed, broken characters repaired, and the `Variation` field split into product line and colour.
- Each product line was sampled to a similar number of reviews, so counts don't reflect popularity.
- Most review dates cluster in late July (likely the collection date), so the page shows no time trend.

To run locally, open `index.html` in a browser (an internet connection is needed for the CDN scripts).
