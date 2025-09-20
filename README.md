## Summary of Level 1

### Inconsistencies Found and Fixed:

- **Gender**: Mixed formats ("M", "Male", "F", "Female") standardized to "male" and "female"
- **Country**: Inconsistent naming ("Rsa", "Norge", "Norway") standardized to proper country names
- **Previous Education**: Typos ("Barrrchelors", "Diplomaaa") corrected to "Bachelors" and "Diploma"
- **Residence**: Multiple variations ("BI-Residence", "BIResidence", "BI\_Residence") standardized to "BI Residence"


### Missing Values Handling:

- **Python scores**: 2 missing values filled with median (84.0)
- **DB scores**: 1 missing value filled with median (70.0)
- Used median instead of mean to be less sensitive to outliers


### Outliers Detection and Treatment:

- **Detection**: Used IQR method with boxplots to identify outliers
- **Treatment**: Removed rows where values fell outside Q1 - 1.5×IQR and Q3 + 1.5×IQR
- **Result**: Removed 7 rows containing extreme values in studyHOURS, Python, or DB scores


The cleaned dataset now has consistent categorical values, no missing data, and reasonable value ranges for all variables, making it suitable for further analysis and machine learning.

## Summary of Level 2:

1. **Feature Engineering**: Created 3 new features that capture different aspects of student performance and characteristics
2. **Feature Scaling**: Applied both StandardScaler and MinMaxScaler to numerical features
3. **Encoding**: Implemented both Label Encoding and One-Hot Encoding for categorical variables
4. **Final Export**: Created a fully processed dataset ready for machine learning modeling


The choice between scaling methods and encoding techniques should be based on the specific machine learning algorithm you plan to use. For most algorithms, StandardScaler with One-Hot Encoding provides a good starting point.
