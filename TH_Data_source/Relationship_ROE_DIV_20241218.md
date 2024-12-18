#Scatter plot of stock data as of 18 Dec 2024#

#import libraly#
'''
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
'''

#import Data of stock#
'''
pe_de = pd.read_csv('https://github.com/firstfootstep/Data_source/raw/refs/heads/main/TH_Data_source/pe_de_20241217.csv')
pe_de.head()
'''

#Look around the data#
'''
pe_de.describe()
pe_de.info()
'''

#Scatter plot with Seaborn#
'''
sns.relplot(data = pe_de[pe_de['roe'] < 100],
            x = 'div',
            y = 'roe',
            kind = 'scatter',
            hue = 'sector')

plt.title("Relationship between ROE and Dividend(%)")
plt.xlabel("Dividend(%)")
plt.ylabel("roe")

plt.show()
'''


