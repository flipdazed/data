Penny Stock Challenge
======================

We taken a few low value penny stocks that performed okish for the period `2017-11-29` until `2018-12-13`
The challenge is to design a trading strategy around this dataset using machine learning methods

# Rules
 - You must use at least one regression or a classification algorithm to generate signals
 - You do not have to limit youself to just this dataset (although it is notewothy that this data has enough signal for a strategy)
 - You do not need to take into acocunt liquidity
 - Your strategy must create the following columns in a **single** pandas DataFrame:
   - position (for each instrument)
   - PnL (for each instrument)
 - You will be required to submit your code for review
 - Use jupyter notebook(s) for ideas - NB: you can submit multiple idea notebooks

# Marking Criteria
 - stability of strategy on the out of sample period (max dd, sharpe)
 - churn of strategy (lots of large position changes will cause high TCs in real life)
 - bugs in your code will clearly affect your score

# Tips
Focus on getting *something* together and improving upon it. We are not necessarily as bothered by positive PnL, rather a logical process.
The main thing about this is pretend we have just hired you and we have asked you to investigate this on the desk for a potential new strategy.

# Reading Data

You can read the file like follows

        In [120]: ls
        train.zip

        In [121]: data = pd.read_csv('train.zip')

        In [122]: data.head()
        Out[122]: 
                            datetime  instr_0  instr_1  instr_2  instr_3  instr_4  instr_5  instr_6  ...  instr_22  instr_23  instr_24  instr_25  instr_26  instr_27  instr_28  instr_29
        0  2017-11-29 09:57:00+00:00      NaN      NaN      NaN      NaN      NaN      NaN      NaN  ...       NaN       NaN       NaN  0.158771       NaN       NaN       NaN       NaN
        1  2017-11-29 10:57:00+00:00      NaN      NaN      NaN      NaN      NaN      NaN      NaN  ...       NaN       NaN       NaN  0.159026       NaN       NaN       NaN       NaN
        2  2017-11-29 11:57:00+00:00      NaN      NaN      NaN      NaN      NaN      NaN      NaN  ...       NaN       NaN       NaN  0.158855       NaN       NaN       NaN       NaN
        3  2017-11-29 12:57:00+00:00      NaN      NaN      NaN      NaN      NaN      NaN      NaN  ...       NaN       NaN       NaN  0.158781       NaN       NaN       NaN       NaN
        4  2017-11-29 13:57:00+00:00      NaN      NaN      NaN      NaN      NaN      NaN      NaN  ...       NaN       NaN       NaN  0.160082       NaN       NaN       NaN       NaN

        [5 rows x 31 columns]
