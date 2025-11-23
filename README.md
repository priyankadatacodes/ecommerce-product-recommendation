# **E-Commerce Product Recommendation System**
*End-to-End Data Science Project*

---

## **1. Project Overview**

This project delivers a scalable Recommendation System for e-commerce platforms, utilizing Collaborative Filtering to personalize product suggestions.  
Key goals include improving user engagement, repeat purchases, and average order value. The pipeline covers Data Cleaning, EDA, Feature Engineering, User-Item Matrix Construction, and Similarity-based Recommendations.

---

## **2. Business Problem**

E-commerce businesses capture vast user–product interaction data, but lack intelligent recommendation systems to:
- Suggest relevant items
- Increase session duration
- Boost conversions and repeat purchases

**Objective:**  
Design a Recommendation Engine that predicts the next product a user may buy, based on historical activity.

---

## **3. Objectives**

- Enhance shopping experience through personalized recommendations
- Model user–product preferences with a rating matrix
- Implement Collaborative Filtering (cosine similarity)
- Deliver a scalable solution for large-scale datasets

---

## **4. Dataset Description**

- File: `product_recommendation_dataset.csv`
- Shape: 50,500 rows (final cleaned: 50,000), 12 columns

**Key Variables:**

| Variable       | Description                        |
|----------------|------------------------------------|
| User_ID        | Unique user identifier             |
| Product_ID     | Product unique identifier          |
| Category       | Product category                   |
| Rating         | User rating (1–5)                  |
| Product_Price  | Product price                      |
| User_Location  | Customer city                      |
| Company_Name   | Marketplace or brand               |
| Payment_Method | Transaction mode                   |
| Delivery_Status| Delivered/Returned/Cancelled       |
| Review_Text    | Short review text                  |

- Missing Values: ~2% per Rating, User_Location, Payment_Method, Review_Text  
- 500 duplicates removed  
- Timestamp: converted to datetime

---

## **5. Tools and Technologies Used**

- **Programming:** Python  
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Scikit-Learn  
- **Modeling:** Collaborative Filtering (Cosine Similarity)  
- **Environment:** Jupyter Notebook

---

## **6. Data Cleaning**

- Mode imputation for categorical columns  
- Median imputation for Rating  
- Converted Timestamp to datetime  
- 500 duplicates removed  
- Final format: 50,000 rows × 12 columns

---

## **7. Exploratory Data Analysis (EDA)**

- **Univariate Insights:**  
  - Ratings: 1–5, balanced distribution  
  - Prices: 5–500, uniform spread  
  - 8 categories: Electronics, Clothing, Home, Toys, Grocery, Sports, Books, Beauty

- **Categorical Insights:**  
  - Top cities: Philadelphia, New York, Los Angeles  
  - Major brands: Walmart, Flipkart, Amazon  
  - Most used payment: UPI, Debit Card  
  - Device type: predominantly Mobile

- **Multivariate Insights:**  
  - Delivery status impacts rating; delivered gets higher scores  
  - Toys and Electronics get higher engagement  
  - Weak correlations across features; diverse behaviors

- **Heatmap:** confirms minimal correlations among numerics

---

## **8. Feature Engineering**

- **Encoding:**  
  - One-Hot for Category, User_Location, Company_Name, Device_Type, Payment_Method, Delivery_Status  
  - Final encoded matrix: 39 columns

- **Scaling:**  
  - StandardScaler for Product_Price and Rating

---

## **9. User–Item Interaction Matrix**

- Pivot table:  
  - Rows: 1000 users  
  - Columns: 500 products  
  - Ratings: empty → 0
- Shape: 1000 × 500
- Used for similarity calculations

---

## **10. Collaborative Filtering Model**

- **Similarity Computation:**  
  - Item-based: cosine similarity on product vectors  
  - User-based: cosine similarity on user vectors

- **Benefits:**  
  - Doesn’t rely on product metadata  
  - Learns from user history  
  - Scalable and interpretable

---

## **11. Recommendation Engine**

Custom function fetches similar items for any given product:


---

## **12. Key Outcomes**

- Scalable collaborative filtering engine
- Strong user segmentation EDA
- High accuracy in similar product recommendations
- Ready for web/mobile production integration

---

## **13. Future Enhancements**

- Model-based collaborative filtering (SVD, Matrix Factorization)
- REST deployment (Flask/FastAPI)
- Sentiment-aware recommendations via NLP on Review_Text
- Hybrid (Content + Collaborative) recommendation

## **14. Conclusion**

This project demonstrates a complete, production-style workflow for e-commerce recommendation systems. It highlights advanced data processing, EDA, modeling, and feature engineering—skills aligned for business analyst and data science positions.

---

