---

# 📊 Bank Marketing Campaign Analysis: Uncovering What Works

In this project, I analyzed data from a bank’s marketing campaigns to reveal what drives customer engagement. Through a series of SQL queries, I explored patterns in demographics, behaviors, and previous responses to better understand who’s saying "yes" to a deposit. Each analysis here provides insights to guide future strategies, targeting the right people with the right messages.

---

### 📌 Analysis Highlights:
* **Who** is more likely to make a deposit?
* **Which demographics** engage more with the campaign?
* **How effective** are past campaign approaches in securing deposits?

---

## Key Insights and Visuals

### 1. Total Successful Deposits
My first step was to count how many customers made deposits. This serves as the foundation—understanding the overall response helps measure the success of other strategies.

```sql
SELECT COUNT(*) AS total_deposits
FROM bank
WHERE deposit = 'yes';
```

![Total number of successful deposits](https://github.com/DanieltheAnalyst1/Screenshots/raw/main/Total%20number%20of%20successful%20deposits.png)

**Takeaway:** This count serves as a baseline for all other comparisons, helping me gauge what drives these deposit decisions.

---

### 2. Deposits by Job Type
Next, I looked at the impact of job roles on deposits. Knowing which sectors engage more can shape targeted strategies.

```sql
SELECT job, COUNT(*) AS deposits
FROM bank
WHERE deposit = 'yes'
GROUP BY job
ORDER BY deposits DESC;
```

![Deposits by Job Type](https://github.com/DanieltheAnalyst1/Screenshots/raw/main/Number%20of%20deposits%20by%20job.png)

**Takeaway:** Some job roles show significantly higher engagement. This insight enables the bank to personalize messages, ensuring outreach is relevant to specific occupations.

---

### 3. Deposits by Education Level
I also analyzed deposit trends across educational backgrounds to see if this factor plays a role in customer engagement.

```sql
SELECT education, COUNT(*) AS deposits
FROM bank
WHERE deposit = 'yes'
GROUP BY education
ORDER BY deposits DESC;
```

![Deposits by Education Level](https://github.com/DanieltheAnalyst1/Screenshots/raw/main/Number%20of%20deposits%20by%20education%20level.png)

**Takeaway:** Education level appears to influence engagement, with some groups more receptive to banking products. This insight can help fine-tune messaging across educational demographics.

---

### 4. Deposits by Marital Status
Understanding how marital status impacts deposit rates provides a glimpse into customer priorities based on life stages.

```sql
SELECT marital, COUNT(*) AS deposits
FROM bank
WHERE deposit = 'yes'
GROUP BY marital
ORDER BY deposits DESC;
```

![Deposits by Marital Status](https://github.com/DanieltheAnalyst1/Screenshots/raw/main/Number%20of%20deposits%20by%20marital%20status.png)

**Takeaway:** Some marital statuses show higher deposit rates, indicating that life circumstances might influence financial priorities and receptiveness to banking offers.

---

This documentation showcases my analytical approach to understanding customer behavior in bank campaigns, supported by clear visuals. Each insight adds value to the overall understanding of engagement trends, guiding more targeted and effective marketing efforts.
