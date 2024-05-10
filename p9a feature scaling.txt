import pandas as pd
from sklearn.preprocessing import StandardScaler, MinMaxScaler
data = {'Feature1': [10, 20, 30, 40, 50],
        'Feature2': [1, 2, 3, 4, 5]
        }
df = pd.DataFrame(data)
object = StandardScaler()
df_standardized = object.fit_transform(df)
min_max_scaler = MinMaxScaler()
df_normalized = min_max_scaler.fit_transform(df)
print("Original DataFrame: ")
print(df)
print("Dataframe after standardization: ")
print(pd.DataFrame(df_standardized, columns=df.columns))
print("DataFrame after :")
print(pd.DataFrame(df_normalized, columns=df.columns))
