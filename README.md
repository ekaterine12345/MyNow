# MyNow
# L2
import pandas as pd
df = pd.DataFrame(people)
df['email']
df[['last', 'email']]
df.columns
df.describe().transpose()
df.iloc[[0, 1], 2] df.iloc[0:2] df.iloc[[0, 1]] df.iloc[[0, 1], 2] df.iloc[1:-1] df.iloc[0, 1] df.loc[[0, 1], ['email', 'last']]
df.set_index('email', inplace=True)
df.index 
df.columns
df.loc['JaneDoe@email.com', 'last']
df.reset_index(inplace=True)   df[df['last'] == 'Doe']   
flt_2 = (df['last'] == 'Schafer') | (df['first'] == 'John')         df.loc[~flt_2, 'email']
df['full_name'] = df['first'] + " " + df['last']
df['full_name'].str.split(' ', expand=True)
df.drop(columns=['first', 'last'], inplace=True)
new_row = pd.DataFrame({'first': 'Tony'}, index=[len(df)])
df = pd.concat([df, new_row], ignore_index=True)

