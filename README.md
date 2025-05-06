# Product Recommendation System

This project implements a product recommendation system using collaborative filtering based on customer purchase history.

## Dataset

The dataset used for this project is the "Online Retail" dataset. This dataset contains transactional data of an online retail store. It includes information about customer purchases, such as product descriptions, quantities, unit prices, countries, and invoice dates.

**Data Source:** The dataset is publicly available. https://www.kaggle.com/datasets/tunguz/online-retail

**Data Cleaning:**

The following data cleaning steps were performed:

- Removed rows with missing customer IDs or product descriptions.
- Removed canceled orders (InvoiceNo starting with 'C').
- Removed rows with invalid quantities or unit prices (less than or equal to 0).
- Removed irrelevant product descriptions (e.g., 'DISCOUNT', 'POSTAGE').
- Stripped extra spaces and converted product descriptions to uppercase.

## Procedure

1. **Data Loading and Cleaning:** The dataset is loaded and cleaned as described above.
2. **Customer-Item Interaction Matrix:** A matrix is created where rows represent customers, columns represent products, and values represent the quantity of each product purchased by each customer.
3. **Item-Customer Matrix:** The interaction matrix is transposed to create an item-customer matrix.
4. **Cosine Similarity:** Cosine similarity is calculated between products based on their purchase patterns across customers.
5. **Recommendation Function:** A function is defined to recommend similar items to a given product based on the similarity scores.
6. **Execution:** The user can input a product name, and the system recommends similar products.

## Results

The recommendation system provides a list of similar products for a given product based on the purchase history of other customers. The similarity scores indicate the level of similarity between products.
