# CMSE202_G3
Health and Wellness Group Project (Obesity)

**How to run the code?** 
- The quantization of the data follows:
  - 'family_history_with_overweight', 'FAVC', 'SMOKE', 'SCC' ; yes = 1.0 , no = 0.0
  - 'CAEC', 'CALC' ;  'Always': 1.0, 'Frequently': 0.67, 'Sometimes': 0.33, 'no': 0.0
  - 'Gender' ; yes = 1.0 ,  no = 0.0
  - 'MTRANS' ; 'Public_Transportation': 1, 'Automobile': 0.75, 'Motorbike': 0.5, 'Bike': 0.25, 'Walking': 0.0
  - 'NObeyesdad' ; 'Obesity_Type_III': 1.0, 'Obesity_Type_II': 0.8333, 'Obesity_Type_I': 0.6666, 'Overweight_Level_II': 0.5, 'Overweight_Level_I':
    0.3333, 'Normal_Weight': 0.1666, 'Insufficient_Weight': 0.0  

- The `BMICalculator` class is designed to process various health-related parameters to calculate the Body Mass Index (BMI), determine obesity levels, and categorize an individual's weight. Directions on using this class follow:
  1.  **Initialization**: Instantiate the `BMICalculator` with parameters such as dietary habits, physical metrics (age, height, weight), family history, and lifestyle choices.
  2.   **Methods**:
       - `calculate_bmi()`: Returns the BMI based on height and weight.
       - `calculate_obesity_level()`: Computes a custom obesity level from multiple health factors.
       - `get_weight_category()`: Categorizes weight based on the BMI.
       - `print_summary()`: Displays a summary of health metrics, BMI, and weight category. 

**What each member contributed?**
- Atticus: Cleaning data frame and quantitating all non-numerical entries.  Created a correlation matrix between these variables with the takeaway of significant variables. Using these results created presentable visualizations between strongly correlated variables. Troubleshooting with data / visualizations as well.  
- Deeya: Finding the dataset, writing the class, and creating the OLS regression summary. Formatting the .ipynb file and helping create a visually appealing presentation. Troubleshooting with data / visualizations. Helped check over the abstract and make sure that it was in accordance with our final data. 
- Shreyas: Worked on the final presentation, created interpretable legends so the visuals could then be legible rather than numbers, and completed Abstract. Helped troubleshoot output errors with the classes. 
