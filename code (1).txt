import pandas as pd
import zipfile

# Extract real-world data
with zipfile.ZipFile('C:/Users/fawzy/OneDrive/Desktop/project/archive.zip', 'r') as archive:
    archive.extractall('C:/Users/fawzy/OneDrive/Desktop/project/')
real_data = pd.read_csv('C:/Users/fawzy/OneDrive/Desktop/project/healthcare-dataset-stroke-data.csv')

# Display clinical features
print('ID:', real_data['id'].unique())
print('Gender:', real_data['gender'].unique())
print('Age:', real_data['age'].unique())
print('Hypertension:', real_data['hypertension'].unique())
print('Heart Disease:', real_data['heart_disease'].unique())
print('Ever Married:', real_data['ever_married'].unique())
print('Work Type:', real_data['work_type'].unique())
print('Residence Type:', real_data['Residence_type'].unique())
print('Avg Glucose Level:', real_data['avg_glucose_level'].unique())
print('BMI:', real_data['bmi'].unique())
print('Smoking Status:', real_data['smoking_status'].unique())
print('Stroke:', real_data['stroke'].unique())

# Extract synthetic data
with zipfile.ZipFile('C:/Users/fawzy/OneDrive/Desktop/project/playground-series-s3e2.zip', 'r') as archive:
    archive.extractall('C:/Users/fawzy/OneDrive/Desktop/project/')
synth_data_train = pd.read_csv('C:/Users/fawzy/OneDrive/Desktop/project/train_2v.csv')
synth_data_test = pd.read_csv('C:/Users/fawzy/OneDrive/Desktop/project/test_2v.csv')

# Display clinical features for synthetic data
print('ID:', synth_data_train['id'].unique())
print('Gender:', synth_data_train['gender'].unique())
print('Age:', synth_data_train['age'].unique())
print('Hypertension:', synth_data_train['hypertension'].unique())
print('Heart Disease:', synth_data_train['heart_disease'].unique())
print('Ever Married:', synth_data_train['ever_married'].unique())
print('Work Type:', synth_data_train['work_type'].unique())
print('Residence Type:', synth_data_train['Residence_type'].unique())
print('Avg Glucose Level:', synth_data_train['avg_glucose_level'].unique())
print('BMI:', synth_data_train['bmi'].unique())
print('Smoking Status:', synth_data_train['smoking_status'].unique())