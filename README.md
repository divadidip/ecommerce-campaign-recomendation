# E-Commerce Campaign Recommendation

Hello! I'm using Google Colab to create an analysis of e-commerce sales performance to recommend campaigns & growth opportunities.
I'm mainly using SQLlite (for data manipulation) and Pandas (for visualization)

Dataset: https://www.kaggle.com/datasets/shreyanshverma27/online-sales-dataset-popular-marketplace-data

## Content
1. Sales Performance: by month, by product category, by revenue, by region
2. Payment Method Analysis: pattern by month, pattern by product, AOV per method, revenue contribution per method, sales volume per method
3. Correlation between payment method & AOV
4. Marketing campaign recommendation

## Packages used
Pandas, SQLlite, Seaborn, Matplotlib, Pearsonr, Spearmanr

## Process
1. Creating a connection between the Dataframe to SQLlite database
2. Data Preparation (No data cleaned up was done because I picked a dataset that's already cleaned)
3. Exploratory Data Analysis (EDA) - explore possible patterns and trends to produce insights
4. Correlation test
5. Suggest growth opportunities based on data analysis

## Sales Performance

### Monthly revenue trend
![image](https://github.com/user-attachments/assets/f4b677eb-02f0-4e5b-b66c-72126600dbc7)

Interpretation on sales trend:
- The best sales happened in the first half of the year
- Judging by the type of items we sold, it can be connected to the behavior of making 'big-purchases' at the start of the year as a part of 'new years resolution'
- The spike in month 3 & 4 can be further investigated. For example - we hypothesize that the spike in month 3 & 4 is from the Asia region due to many festives being held at that month.

### Revenue per category in accordance to unit sold
![image](https://github.com/user-attachments/assets/e0667c82-9fe7-41e9-82cd-aa6936df73bc)

Interpretation on product category performance:
- It's quite hard to judge the performance if we're only looking at 'revenue'. We should collaborate with sales & finance to look at 'margin' per category data
- For example, Electronics might bring the most revenue without having large inventory, but what about the margin contribution?
- Books and clothing stock must be tended frequently as they need a lot of stocks but contribute to small number of revenue

### Product category by region
![image](https://github.com/user-attachments/assets/7e80c6c7-a333-4373-a399-5b5114af76e4)
![image](https://github.com/user-attachments/assets/4d977353-af18-4b0e-9f8a-ba476fe02208)
![image](https://github.com/user-attachments/assets/4da0f17f-ec24-4c5d-9262-b66758e8c8db)

Interpretation on region performance:
- Each region can determine their own focus on whether they want to optimize for revenue or quantity (units sold) metrics
- For example, North America might want to focus on selling electronics only as they bring the most revenue while keeping a low stock


## Payment Method Analysis
![image](https://github.com/user-attachments/assets/d4fdd966-afdc-4cef-90b7-30b887dabcef)
![image](https://github.com/user-attachments/assets/5fc22e00-c136-40ec-8d0f-4ec4252d2d72)

Interpretation on payment method analysis
- No trends or patterns found in payment method usage by month and payment method by category
- Credit cards and debit cards are used for higher volumes of sales compared to PayPal (mainly used for higher-value items like electronics and sports).
- PayPal transactions are relatively consistent and involve fewer units per sale.
- PayPal transactions show potential of high-value transactions from Home Appliances, like credit cards.
- Debit card method for clothing shows consistent number of sales volume

## Correlation Between Payment Method & AOV
Pearson Correlation Coefficient: -0.697377808166478

Pearson P-value: 0.5086999783770505

Spearman Correlation Coefficient: -0.5

Spearman P-value: 0.6666666666666667


Interpretation:
- Payment method doesn't affect AOV that much, however further investigation is required by using more data or testing the correlation of AOV with other variables
- Although in this test it is not statistically significant, we can test AOV again with a specific customer segmentation (e.g. AOV for customer with preferred payment method - we don't have this data tho)
- In the previous analysis stored in df_average_order_value, we can also take notes that Credit Card brings higher AOV - we can consider similar Credit or Pay Later payment methods to high-price unit items

## Campaign Recomendation & Growth Opportunities
### 1. Target High-Value Category/Products with Credit Cards:
- Electronics can be an entry point here, given its high median sales and potential for large transactions
- Sports also shows potential like electronics, just not as high
- Consider to partner with banks to provide low interest rate for high value products
- Consider to create promo and loyalty programs to capitalize high-value customers
- Consider to create campaign for brand awereness with Eletronics and Sports brands to gain more traffic for these type of purchases
### 2. Optimize PayPal to increase AOV
- Home appliances purchase with PayPal has shown potential for higher sales
- We can test by creating special promo for high-value products with PayPal, just like what we are doing with Credit Card
- Consider to partner with PayPal's BNPL to offer low interest and cashbacks for high-value products
### 3. Build Promo Around Clothing Purchase with Debit Card to Increase Sales Volume
- Customer's are using debit card to purchase clothes, no matter in how many quantities
- To increase sales volume, we can create campaign for discounts, cashback, loyalty points for every > 5 item purchase
### 4. Bundle Products to Increase AOV
- Bundle products from high-performing categories (e.g. Electronics and Sports) to increase average order value.
- Need to test and analyze to check whether they can be sold as a bundle or not








