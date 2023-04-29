# Pandas-AI
#PandasAI 🐼

Pandas AI is a Python library that adds generative artificial intelligence capabilities to Pandas, the popular data analysis and manipulation tool. It is designed to be used in conjunction with Pandas, and is not a replacement for it.
![image](https://user-images.githubusercontent.com/120645302/235294167-40e46cb2-224d-452a-a5fd-39772697a11d.png))


# Installation
pip install pandasai

Usage

PandasAI is designed to be used in conjunction with Pandas. It makes Pandas conversational, allowing you to ask questions about your data and get answers back, in the form of Pandas DataFrames. For example, you can ask PandasAI to find all the rows in a DataFrame where the value of a column is greater than 5, and it will return a DataFrame containing only those rows:

import pandas as pd

from pandasai import PandasAI

import pandas as pd
from pandasai import PandasAI

Sample DataSet

df=pd.DataFrame({'Country':['United States','United Kindom','France','Germany','Italy','Spain',
                            'Canada','Australia','Ireland','Denmark'],
                'GDP':[21400000,2940000,2830000,3870000,2160000,1350000,1780000,516000,1400000,1200000],
                'Happiness_Index':[7.3,7.2,6.5,7.0,6.0,6.0,3.7,3.7,5.9,5.0]
                })
# Instantiate a LLM
from pandasai.llm.openai import OpenAI
llm= OpenAI(api_token="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")
pandas_ai=PandasAI(llm)
pandas_ai.run(df,prompt='which are the 5 happies countries?')

# Instantiate a LLM
from pandasai.llm.openai import OpenAI
llm = OpenAI()

