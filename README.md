# Multi-Brand-Customer-Satisfaction-Analytics-Pipeline
Customer Satisfaction Analysis: Acer, Asus, Dell, and Lenovo Laptops

📌 Overview

This project builds an end-to-end analytical pipeline to evaluate and compare customer satisfaction across four major laptop manufacturers — Acer, Asus, Dell, and Lenovo — by combining web-scraped customer reviews, transformer-based sentiment analysis, and statistical reliability scoring. Rather than relying on star ratings alone, this pipeline captures the emotional tone and context behind customer feedback to produce a more accurate, data-driven satisfaction ranking.

🎯 Objective

Star ratings alone fail to capture nuance, sarcasm, and the reasoning behind customer opinions. This project goes beyond surface-level metrics to determine which manufacturer delivers the highest genuine customer satisfaction.

🛠️ Pipeline

Web Scraping — Automated collection of 898+ customer reviews using Python and Selenium, handling dynamic page loads, brand-specific pagination, and anti-bot measures across manufacturer and retailer sites.
Data Cleaning & Preprocessing — Regex-based cleaning (lowercasing, punctuation/HTML removal), invalid rating filtering, and null-text handling.
Transformer-Based Sentiment Analysis — DistilBERT (via Hugging Face + TensorFlow) used to classify sentiment and generate confidence scores for each review's text.
Composite Satisfaction Scoring — A weighted formula combining normalized star ratings (60%) and sentiment scores (40%) to produce a unified satisfaction metric per review.
Wilson Lower Bound Scoring — Statistical confidence ranking (95% CI) to fairly compare brands despite uneven review volumes, preventing brands with few reviews from appearing artificially strong.
Power BI Dashboards — Interactive visualizations of ratings, sentiment, reliability, and satisfaction scores per brand, including word clouds and review-level scatter/distribution plots.

📊 Key Findings

Lenovo led across nearly every metric — highest average rating (4.7), sentiment score (0.62), Wilson score (0.90), and satisfaction score (0.80).
Dell ranked a close second, and actually topped the composite score (0.82) due to higher review volume.
Asus and Acer trailed in sentiment and satisfaction, with Acer scoring lowest overall.
🧰 Tech Stack

Python · Selenium · Pandas · TensorFlow · Hugging Face Transformers (DistilBERT) · scikit-learn · Power BI · Matplotlib/Seaborn

📈 Applications

The methodology generalizes to recommendation systems, market trend analysis, consumer behavior research, and competitive benchmarking beyond laptops.
