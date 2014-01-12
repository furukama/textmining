# -*- coding: utf-8 -*-
"""
Transforms the output of the Hive/MapReduce n-gram analysis
into a human readable Excel file
"""

import pandas as pd
import xlrd

data = pd.read_csv("./export_file.txt", sep="", header=None, index_col=False)
data.columns = ["Word", "Decade", "Ratio", "Increase"]
data.Decade = [d * 10 for d in data.Decade]

writer = pd.ExcelWriter("./German_ngrams.xlsx")
data.to_excel(writer, "German_ngrams", index=False)
writer.save()
