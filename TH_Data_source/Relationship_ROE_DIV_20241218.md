# Scatter plot of stock data as of 18 Dec 2024

# import library
```{python}
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```

# import Data of stock
```{python}
pe_de = pd.read_csv('https://github.com/firstfootstep/Data_source/raw/refs/heads/main/TH_Data_source/pe_de_20241217.csv')
pe_de.head()
```

# Look around the data
```{python}
pe_de.describe()
pe_de.info()
```

# Scatter plot with Seaborn 
```{python}
sns.relplot(data = pe_de[pe_de['roe'] < 100],
            x = 'div',
            y = 'roe',
            kind = 'scatter',
            hue = 'sector')

plt.title("Relationship between ROE and Dividend(%)")
plt.xlabel("Dividend(%)")
plt.ylabel("roe")

plt.show()
```
# Result
![image](https://github.com/user-attachments/assets/7f19f8d3-fb33-489a-8abd-3cfa554cfdc4)


