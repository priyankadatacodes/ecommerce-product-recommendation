# **E-Commerce Product Recommendation System**
**End-to-End Recommendation & Analytics Project (Python)**

---

## **Executive Summary**

This project builds a **personalized Product Recommendation System** for an e-commerce platform using **Collaborative Filtering** techniques.

The system analyzes historical **user–product interactions** to recommend relevant products, with the goal of improving **user engagement, repeat purchases, and average order value**.

The project follows a production-style data science workflow covering **data cleaning, exploratory analysis, feature engineering, user–item matrix construction, similarity modeling, and recommendation generation**.

---

## **Why I Built This Project**

E-commerce platforms collect large volumes of user interaction data, but without intelligent recommendations:
- Users struggle to discover relevant products
- Engagement drops quickly
- Conversion and repeat purchases suffer

I built this project to demonstrate how **data-driven personalization** can improve customer experience and business performance using **collaborative filtering**, a widely used industry approach.

This mirrors a real-world scenario where data analysts and data scientists support **growth and personalization teams**.

---

## **Business Context**

In competitive e-commerce environments:
- Personalization is a key differentiator
- Customers expect relevant suggestions
- Generic product listings reduce engagement

Recommendation systems help businesses:
- Increase session duration
- Improve cross-sell and up-sell
- Boost customer lifetime value (CLV)

---

## **Problem Statement**

Design a recommendation engine that predicts **which products a user is most likely to purchase next**, based on historical user–product interaction data, without relying on explicit product metadata.

---

## **Objectives**

- Personalize the shopping experience  
- Model user–product preferences using interaction data  
- Implement **Collaborative Filtering** with cosine similarity  
- Build a scalable and interpretable recommendation pipeline  

---

## **Hypotheses**

Before analysis, the following hypotheses were framed:

- **H1:** Users with similar behavior prefer similar products  
- **H2:** Products with similar rating patterns can be recommended together  
- **H3:** Collaborative filtering can generate relevant recommendations without product descriptions  
- **H4:** Interaction-based models scale better for large catalogs  

---

## **Dataset Overview**

- **File:** `product_recommendation_dataset.csv`
- **Initial Size:** **50,500 rows**
- **Final Cleaned Size:** **50,000 rows**
- **Columns:** **12**

### **Key Variables**

| Variable | Description |
|-------|------------|
| User_ID | Unique user identifier |
| Product_ID | Unique product identifier |
| Category | Product category |
| Rating | User rating (1–5) |
| Product_Price | Product price |
| User_Location | Customer city |
| Company_Name | Marketplace or brand |
| Payment_Method | Transaction mode |
| Delivery_Status | Delivered / Returned / Cancelled |
| Review_Text | Short user review |

- Missing values: ~**2%** across selected columns  
- Duplicates removed: **500**  
- Timestamp converted to **datetime**

---

## **Tools & Technologies**

- **Programming:** Python  
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn  
- **Modeling Technique:** Collaborative Filtering (Cosine Similarity)  
- **Environment:** Jupyter Notebook  

---

## **Data Cleaning**

- Mode imputation for categorical features  
- Median imputation for ratings  
- Timestamp conversion to datetime  
- Removed **500 duplicate records**  
- Final dataset shape: **50,000 × 12**

---

## **Exploratory Data Analysis (EDA)**

### **Univariate Insights**
- Ratings range from **1 to 5**, fairly balanced  
- Product prices range from **5 to 500**  
- **8 product categories** including Electronics, Clothing, Home, Toys, Grocery  

### **Categorical Insights**
- Top cities: **Philadelphia, New York, Los Angeles**
- Major brands: **Amazon, Walmart, Flipkart**
- Popular payment methods: **UPI, Debit Card**
- Most users shop via **Mobile devices**

### **Multivariate Insights**
- Delivered orders receive higher ratings  
- Electronics and Toys show higher engagement  
- Weak numeric correlations, indicating diverse customer behavior  

---

## **Feature Engineering**

- **Encoding:**
  - One-Hot Encoding for Category, Location, Brand, Payment Method, Device Type, Delivery Status  
  - Final encoded feature set: **39 columns**

- **Scaling:**
  - StandardScaler applied to **Product_Price** and **Rating**

---

## **User–Item Interaction Matrix**

- Constructed using pivot table:
  - **Rows:** 1,000 users  
  - **Columns:** 500 products  
  - Missing ratings filled with **0**

- Final shape: **1000 × 500**

This matrix forms the foundation for similarity calculations.

---

## **Collaborative Filtering Model**

- **Approach Used:**
  - Item-based Collaborative Filtering  
  - User-based Collaborative Filtering  

- **Similarity Metric:** Cosine Similarity  

### **Why Collaborative Filtering?**
- Learns from actual user behavior  
- No dependency on product metadata  
- Interpretable and scalable  

---

## **Recommendation Engine**

A custom recommendation function:
- Accepts a product or user as input  
- Identifies similar users or products  
- Returns top-N recommended products  

This design is **ready for integration** with web or mobile applications.

---

## **Key Outcomes**

- Built a scalable **collaborative filtering engine**
- Generated meaningful product recommendations  
- Demonstrated strong understanding of user behavior  
- Created a foundation suitable for production deployment  

---

## **Business Impact**

- Improves product discovery  
- Increases engagement and repeat purchases  
- Supports personalization-driven growth  
- Enhances customer experience without manual curation  

---

## **Future Enhancements**

- Model-based collaborative filtering (SVD, Matrix Factorization)  
- Hybrid recommendation (Content + Collaborative)  
- NLP-based sentiment-aware recommendations using reviews  
- REST API deployment (Flask / FastAPI)  

---

## **Final Takeaway**

Personalized recommendations are a critical growth driver for e-commerce platforms.  
This project demonstrates how **data-driven collaborative filtering** can convert raw interaction data into **actionable product recommendations**, improving both user experience and business outcomes.

---

## **Author**

**Priyanka Lakra**  
**Aspiring Data Analyst | Python | Recommendation Systems | Data Analytics**
