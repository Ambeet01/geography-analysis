
import pandas as pd

df = pd.read_csv(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv")

# Auto EDA
# ---------
# Sweetviz
# Autoviz
# Dtale
#Pandas Profiling
# Dataprep


# Sweetviz
###########
#pip install sweetviz
import sweetviz as sv

s = sv.analyze(df)
s.show_html()

from autoviz.AutoViz_Class import AutoViz_Class

av = AutoViz_Class()
a = av.AutoViz(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv".replace("\\", "/"), chart_format = 'html')

import os
os.getcwd()

# If the dependent variable is known:
a = av.AutoViz(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv".replace("\\", "/"), depVar = 'gmat') # depVar - target variable in your dataset



# D-Tale
########

# pip install dtale   # In case of any error then please install werkzeug appropriate version (pip install werkzeug==2.0.3)
import dtale
import pandas as pd

df = pd.read_csv(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv")

d = dtale.show(df)
d.open_browser()


# Pandas Profiling


from pandas_profiling import ProfileReport 

p = ProfileReport(df)
p
p.to_file("output.html")

import os
os.getcwd()

# Dataprep
##########

from  dataprep.eda import create_report

report = create_report(df, title = 'My Report')


report.show_browser()





