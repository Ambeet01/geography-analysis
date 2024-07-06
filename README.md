
import pandas as pd

df = pd.read_csv(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv")

import sweetviz as sv

s = sv.analyze(df)
s.show_html()

from autoviz.AutoViz_Class import AutoViz_Class

av = AutoViz_Class()
a = av.AutoViz(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv".replace("\\", "/"), chart_format = 'html')

import os
os.getcwd()

a = av.AutoViz(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv".replace("\\", "/"), depVar = 'gmat') # depVar - target variable in your dataset


import dtale
import pandas as pd

df = pd.read_csv(r"C:\Users\Ambeet Mohapatra\Downloads\Dataset  (1).csv")

d = dtale.show(df)
d.open_browser()


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





