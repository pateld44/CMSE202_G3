# CMSE202_G3
Health and Wellness Group Project (Obesity)

## **How to run the code?** 
- The quantization of the data follows:
  - 'family_history_with_overweight', 'FAVC', 'SMOKE', 'SCC' ; yes = 1.0 , no = 0.0
  - 'CAEC', 'CALC' ;  'Always': 1.0, 'Frequently': 0.67, 'Sometimes': 0.33, 'no': 0.0
  - 'Gender' ; yes = 1.0 ,  no = 0.0
  - 'MTRANS' ; 'Public_Transportation': 1, 'Automobile': 0.75, 'Motorbike': 0.5, 'Bike': 0.25, 'Walking': 0.0
  - 'NObeyesdad' ; 'Obesity_Type_III': 1.0, 'Obesity_Type_II': 0.8333, 'Obesity_Type_I': 0.6666, 'Overweight_Level_II': 0.5, 'Overweight_Level_I':
    0.3333, 'Normal_Weight': 0.1666, 'Insufficient_Weight': 0.0  

- The `Obesity` class is designed to process various health-related parameters to calculate the Body Mass Index (BMI), determine obesity levels, and categorize an individual's weight. Directions on using this class follow:
  1.  **Initialization**: Instantiate the `BMICalculator` with parameters such as dietary habits, physical metrics (age, height, weight), family history, and lifestyle choices.
  2.   **Methods**:
       - `calculate_bmi()`: Returns the BMI based on height and weight.
       - `calculate_obesity_level()`: Computes a custom obesity level from multiple health factors.
       - `get_weight_category()`: Categorizes weight based on the BMI.
       - `print_summary()`: Displays a summary of health metrics, BMI, and weight category. 

## **What each member contributed?**
- Atticus: Cleaning data frame and quantitating all non-numerical entries.  Created a correlation matrix between these variables with the takeaway of significant variables. Using these results created presentable visualizations between strongly correlated variables. Troubleshooting with data / visualizations as well.  
- Deeya: Finding the dataset, writing the class, and creating the OLS regression summary. Formatting the .ipynb file and helping create a visually appealing presentation. Troubleshooting with data / visualizations. Wrote part of the abstract and then double-checked to make sure that it was in accordance with our final data. Helped coordinate group meeting times.
- Shreyas: Worked on the final presentation, created interpretable legends so the visuals could then be legible rather than numbers, and completed Abstract. Helped troubleshoot output errors with the classes.


## **Abstract** 

  What factors impact obesity the most? How do different strategies to alleviate obesity compare? Addressing these questions about obesity typically necessitates a multifaceted approach incorporating dietary modifications, increased physical activity, behavior adjustments, and sometimes medical interventions.  By examining these factors, a more holistic approach to tackling obesity and promoting healthier lifestyles can be developed. 

  To identify primary factors influencing obesity and assess different strategies, we analyzed a Kaggle dataset containing demographic, biological, and historical information alongside weight class. Using a Correlation Matrix, we examined relationships between factors. Pandas visualizations indicated most overweight individuals were among the youth, potentially due to limited data for older age groups. Lifestyle features like preferred mode of transportation (MTRANS) and food consumption between meals (CAEC) were assessed, showing public transportation's significant correlation with obesity levels (Type I, Type II, and Type III). Notably, individuals reporting "sometimes" eating between meals showed the strongest correlation with Obesity Type III. Family history of overweight correlated significantly with weight class (0.51 on the correlation matrix), confirming a strong positive correlation between family history and weight class. All individuals with Obesity Type III had a family history of being overweight, providing insights into obesity factors. 

  After our initial data analysis, we conducted an Ordinary Least Squares (OLS) regression summary using the statsmodels library. This summary identified significant features, including gender, age, height, weight, family history of overweight, number of main meals (NCP), consumption of food between meals (CAEC), frequency of physical activity (FAF), consumption of alcohol (CALC), and mode of transportation (MTRANS), in relation to weight class (NObeyesdad), from the dataset (P >= 0.05). The OLS Regression summary yielded an R-squared value of 0.951, indicating that the regression model explained our observed data extremely well. This high R-squared value suggests that the model closely aligns with the data and has minimal differences between observed and fitted values. 

 Subsequently, we constructed an object class named "Obesity" based on significant features identified from the OLS Regression summary. This class was utilized to analyze individual profiles, incorporating factors such as weight, height, gender, age, eating habits, and exercise frequency. Obesity levels were determined using two factors: Body Mass Index (BMI) scores and an Obesity Level calculation. Individuals categorized as "Normal weight" exhibit an obesity level of 0.32 or less, indicating overall healthy habits and balanced BMI scores. Conversely, individuals classified as "Overweight" have BMI scores of 0.35 and above, signaling imbalanced habits leading to adverse health effects. This approach proved most effective in determining weight class categorization, as cross-checking the BMI score result with the obesity level ensured consistency in individual profiles. For example, an individual profiled as overweight, with a BMI of 27.78 and an Obesity Level of 0.35, aligns with health reports for individuals at that height, weight, and age. 

  Regarding effective obesity management strategies, our data analysis challenges common beliefs by revealing that physical activity (FAF) exhibits only a minimal correlation of -0.05 with weight. Instead, the most impactful methods include monitoring calorie consumption (SCC) and avoiding food consumption between meals (CAEC). SCC shows a correlation of -0.20, indicating that monitoring calorie intake effectively reduces weight. Similarly, CAEC demonstrates the strongest correlation of -0.29, suggesting that refraining from additional meal consumption beyond standard meals is highly effective in reducing calorie intake and alleviating obesity symptoms. Physical activity remains crucial, with a correlation of -0.20 with NObeyesdad, highlighting its importance in weight regulation. While the correlations are not particularly strong, they provide valuable insights into the directionality of features concerning weight classification. 

  In conclusion, there are many factors found to be significant in causing obesity found from our dataset and analysis. Some of which include family history with overweight, mode of transportation, age, and weight. With thorough research we found that the most effective strategies for weight alleviation involve calorie monitoring and avoiding extra meal consumption. Maintaining a calorie deficit or maintenance level is crucial in preventing weight gain. Altogether, our methodology proved to be insightful in this project, and in the future if given the chance we would like to explore more about it using predictive analytics as a diagnostic tool. 
