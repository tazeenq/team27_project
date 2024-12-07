# Team 27: Retail Sales Data Analysis

**Name**: Tazeen Qureshi<br>
**DSI Cohort Number**: 04<br>
**Stream**: Data Science<br>
**Project Github**: https://github.com/tazeenq/team27_project<br>

## Description
This project analyzes the [Retail Sales Dataset](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset) to see whether I can **classify whether a customer will be a high spender** based on their demographics (age, gender) and purchase attributes (product category, quantity).<br>

***Project report*** detailing out methods, results, visualizations, and recommendations can be found [here](https://github.com/tazeenq/team27_project/blob/main/reports).<br>

## Business Case
The retail industry in Canada is very competitive. In a competitive industry, it is essential to understand customer spending behaviors to execute optimized marketing strategies and guide strategic decision-making. Classifying customers as high spenders based on their demographics and purchase attributes can help businesses target the right audience and allocate their resources efficiently. 

## Answer to the Research Question
My research question was:<br>

*Can we classify whether a customer will be a high spender based on their demographics (age, gender) and purchase attributes (product category, quantity)?*<br>

After running the KNN Model on the dataset, I can conclusively say that yes, the KNN model can effectively classify high spenders based on the purchase attributes.<br>

I can also confidently say that:
- The model has an overall accuracy of 95%, indicating reliable predictions.
- It identifies high spenders with 98% recall, meaning nearly all high spenders are correctly classified.
- The slightly lower precision (85%) for high spenders suggests a small proportion of over-predictions, but this is balanced by the very high recall and F1-score.

Therefore, customer demographics (age, gender) and purchase attributes (product category, quantity) are strong predictors for classifying high spenders.

## Answers to Potential Questions After Reviewing the Dataset
**1. What are they key variables and attributes in the dataset?**<br>

The key variables and attributes in the dataset are:<br>

- **Transaction ID**: Unique identifier for each transaction.<br>
- **Date**: Date of the transaction.<br>
- **Customer ID**: Unique identifier for each customer.<br>
- **Gender**: Gender of the customer.<br>
- **Age**: Age of the customer. <br>
- **Product Category**: Category of the product sold.<br>
- **Quantity**: Number of units sold in the transaction.<br>
- **Price per unit**: Price of one unit of the product.<br>
- **Total Amount**: Total transaction amount (calculated as Quantity x Price per unit).<br>

**2. How can we explore the relationships between different variables?**<br>

In this project, I have explored relationships between different variables using the following statistical methods:
1. Class Imbalance Analysis
2. Categoric and Numeric Variability Analysis
3. Chi-Squate Testing
4. Analysis of Average Spending by Age and Gender
5. Analysis of Average Spending by Product Category and Age Groups
6. Correlation Analysis

**3. Are there any patterns or trends in the data that we can identify?**<br><br>
I was able to identify the following patterns in the data:<br>
- Customers spend more on "Beauty" and "Electronics" as compared to "Clothing".
- Spending decreases consistently with age, where younger age groups spend the most on all three product categories (Beauty, Clothing, and Electronics).
- There is no variability between men and women's spending behaviours, but there is some variability in spending behaviour within the three product categories.
- There is a significant class imbalance in sales in this Comapny, there were about 80% low spenders as compared to some 20% high spenders (who spent the top 25% of total_amount spent).
- There is a strong correlation between price_per_unit and total_amount, indicating no economies of scale.

**4. Who is the intended audience for our data analysis?**<br>

The intended audience includes retail managers, marketing teams, and data analysts who can use the insights from this project to make informed decisions that help improve customer engagement and target revenue strategies.<br>

**5. What is the question our analysis is trying to answer?**<br>

*Can we classify whether a customer will be a high spender based on their demographics (age, gender) and purchase attributes (product category, quantity)?*<br>

**6. Are there any specific libraries or frameworks that are well-suited to our project requirements?**<br><br>
I've used the following libraries/frameworks for this project:<br>
- Pandas and Numpy for data processing
- Matplotlib and Seaborn for exploration and visualizations
- Scikit-learn for normalizing and modelling (KNN and Random Forest classifiers)
- Scipy for statistical analysis

**7. How can we iterate on our design to address feedback and make iterative improvements?**<br><br>
I can iterate on my design in the following way (I did not have time to do this for now):
- Handling the class imbalance by using tools like SMOTE or creating a balanced subset of the data.
- Enhancing features by incorporating engineered features like combining age and product category.
- Validating metrics by improving precision for high spenders by fine tuning hyperparameters.

**8. What best practices can we follow to promote inclusivity and diversity in our visualization design?**<br><br>
Some of the inclusivity and diversity practices that I have tried to apply to this project are:
- Using color palettes that are accessible to those with color vision deficiencies.
- Avoiding overloading the report with graphs and text, clearly labeling sections and detailing what is in each section.
- Providing contextual information in plots, including labels, legends, and more.
- Using different types of visualizations to cater to differences in expertise of the readers.

**9. How can we ensure that our visualization accurately represents the underlying data without misleading or misinterpreting information?**<br><br>
I've ensure that the visualizations are accurately representative of the data by:
- Validating data processing steps (sometimes manually), making sure that the results are not skewed.
- Providing normalized scales for numeric features.
- Clearly labeling axes and including summaries of preprocessing steps in comments.

**10. Are there any privacy concerns or sensitive information that need to be addressed in our visualization?**<br><br>
No, this dataset does not include any sensitive information, it was anonymized. However, I did drop the unique identifiers like transaction ID and customer ID in pre-processing. I have also tried to consider privacy concerns and used aggregated statistics instead of individual level data in the plots.

**11. Are there any missing values or outliers that need to be addressed through preprocessing?**<br><br>
I've handles missing values and outliers in pre-processing using the following:
- Dropping rows with missing date or null values
- Dropping rows with data from 2024 (the entire dataset has data from 2023, with only 2 rows with data from 2024).
- Normalizing the dataset.

**12. What techniques can we use to validate and tune the hyperparameters for our models?**<br><br>
Although I haven't explored validation and tuning hyperparameters in this project in great detail, some effective techniques are to:
- Use Grid Search or Randon Search to find optimal hyperparameters.
- Cross-validating using k-fold, for example, to ensure stable performance across training and validation sets.<br><br>
In the project I've used the Train-Test Split to evaluate the model on unseen data (which is kind of a basic validation technique). I have also used the default number of n_neighbors in the model. 

**13. How should we split the dataset into training, validation, and test sets?**<br><br>
The dataset was split into training and testing sets with an 80/20 split using train_test_split. If I had more time I would create a validation set by further splitting the trainign data (e.g., 70/15/15 for training/validation/testing).


## Project Folder Structure
The folder structure for the project is as follows:<br>
```markdown
|-- data
|---- processed
|---- raw
|-- reports
|-- src
|-- README.md
|-- License
```
* **Data:** Contains the raw and processed dataset files in CSV.
* **Reports:** Include PDF and HTML files with visualizations.
* **src:** Project source code.
* **README**: This file.
* **LICENSE**: Apache 2.0.









