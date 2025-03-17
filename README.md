# Restaurant Comparison Analysis Across Multiple Food Delivery Platforms

## Authors  
- **Priyadharshini Ganeshkumar**  
- **Bhuvana Ravi Kumar**  
- **Sakshi Singh**  
- **Date:** 16th March, 2025  

---

## Overview  
This project compares restaurant data across three major food delivery platforms: **Uber Eats, GrubHub, and DoorDash**. The goal is to analyze **restaurant ratings, delivery times, and menu diversity** to identify platform-specific trends in food delivery services.  

The project involves **web scraping and API-based data retrieval** to extract structured restaurant data. We encountered platform-specific challenges such as **anti-scraping measures, authentication barriers, dynamically loaded content, and rate limiting**, which were addressed using advanced scraping techniques.  

---

## Data Collection & Methodology  

### **Uber Eats & DoorDash:**  
- Web scraping was performed using **Selenium WebDriver** since both platforms do not offer a public API.  
- Techniques like `undetected_chromedriver`, **randomized delays, WebDriver masking, and smooth scrolling** were used to bypass bot detection.  
- **Restaurant details extracted:** Name, Rating, Reviews, Delivery Time, Menu Items.  

### **GrubHub:**  
- Unlike Uber Eats and DoorDash, **GrubHub provided an API but required HMAC authentication**.  
- Due to API restrictions, **session-based authentication methods** were implemented to collect data.  
- A combination of **API calls and network traffic analysis** was used to extract restaurant information.  

---

## Ranking Criteria  

### **Ratings-Based Ranking:**  
- Restaurants were sorted based on **highest ratings and the number of reviews**.  

### **Delivery Time-Based Ranking:**  
- Restaurants were ranked based on **fastest delivery times**, with **distance as a secondary factor**.  

### **GrubHub Weighted Ranking:**  
- A **weighted scoring system** (**60% rating, 40% delivery time**) was used to determine the best restaurants.  

---

## Cross-Platform Analysis  
To compare restaurant performance across **Uber Eats, GrubHub, and DoorDash**, we:  
- **Loaded scraped restaurant data** into Pandas DataFrames.  
- **Merged results** based on common attributes (**restaurant name, ratings, delivery time**).  
- **Created visualizations** to highlight key differences between platforms.  

---

## Visualizations & Insights  
The study involved in-depth visual analyses on multiple aspects:  

- **Cuisine Popularity:** Identifying the most common cuisines on each platform.  
- **Delivery Time Distribution:** Comparing how quickly food is delivered on different services.  
- **Rating Distribution:** Analyzing the consistency of high-rated restaurants across platforms.  
- **Price Trends:** Understanding menu price differences among top-ranked restaurants.  

---

## Key Findings  
- **Best Platform for Ratings:** GrubHub had the highest-rated restaurants overall.  
- **Fastest Delivery:** Uber Eats had the shortest delivery times, but with a wider variation.  
- **Most Reliable Delivery Times:** DoorDash was the most consistent in predicting delivery times.  
- **Most Popular Cuisine:** American and Breakfast dishes dominated Uber Eats, while Chinese food was the most frequent on GrubHub.  

---

## Challenges Encountered  

### **Anti-Scraping Measures:**  
- **Uber Eats & DoorDash** used bot-detection techniques, requiring **WebDriver masking, randomized delays, and JavaScript execution** to evade detection.  
- **GrubHub’s API** required authentication tokens and had **rate-limiting issues**.  

### **Lazy Loading Issues:**  
- Both **Uber Eats and DoorDash dynamically load content**, making it difficult to extract full datasets.  
- **Smooth scrolling automation and JavaScript event tracking** were used to load and capture complete restaurant lists.  

### **Data Filtering:**  
- Uber Eats **does not have a separate Grocery Store category**, which resulted in irrelevant data.  
- A manually curated **exclusion list of grocery stores** was created to filter out non-restaurant entries.  

---

## Future Work  
- **Expand Geographic Scope:** The current study is focused on one location; future work could compare multiple cities.  
- **Real-Time Data Updates:** A live data collection pipeline can be implemented to track restaurant trends over time.  
- **Sentiment Analysis:** Using **NLP techniques** to analyze customer reviews for deeper insights into restaurant quality.  

---

## References  
- [Selenium Documentation](https://selenium-python.readthedocs.io/)  
- [GeeksforGeeks - Selenium Python Tutorial](https://www.geeksforgeeks.org/selenium-python-tutorial/)  
- [Matplotlib for Visualizations](https://matplotlib.org/stable/index.html)  
- [GrubHub Developer API](https://developer.grubhub.com/)  
- [ZenRows - Selenium Web Scraping Guide](https://www.zenrows.com/blog/selenium-python-web-scraping#build-basic-scraper/)  
- [ScrapFly - Scraping Hidden APIs](https://scrapfly.io/blog/how-to-scrape-hidden-apis/)  
- [FoodSpark - UberEats Web Scraping Guide](https://www.foodspark.io/ultimate-guide-to-scraping-data-from-ubereats-with-the-help-of-python-and-selenium/)  
    

---


