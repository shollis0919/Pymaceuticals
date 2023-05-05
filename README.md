# Pymaceuticals
This repository contains the code for a Jupyter Notebook that goes through a data set of mice tumor treatment data and provides visualization of the data in the form of charts and graphs. The repository also contains the datasets used as CSV's and a Word Document of the written report as well as screeenshots of the figures produced in the jupyter notebook code and used in the Word document. 

The following code was devised from: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.duplicated.html
dupeMouse = study_data_complete[study_data_complete.duplicated()]
dupeMouse = study_data_complete[study_data_complete[['Mouse ID','Timepoint']].duplicated() == True]


The following code was devised from: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.bar.html & https://sparkbyexamples.com/pandas/pandas-series-sort-values/#:~:text=Sort%20the%20Series%20in%20Ascending,NaN%20values%20at%20the%20end & https://www.geeksforgeeks.org/python-pandas-series-to_frame/

regcount = regcount ["Mouse ID"]
regcount = regcount.sort_values(ascending=False)
regcount_frame=regcount.to_frame()
reg_Count_Plot = regcount.plot.bar()
reg_Count_Plot.set_xlabel("Drug Regimen")
reg_Count_Plot.set_ylabel("# of Observed Mouse Timepoints")

The following code was devised from https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html#pandas.DataFrame.plot
mouse_sum.plot.pie(y='Mouse ID',autopct="%1.1f%%")
plt.axis("equal")
plt.title("Mouse Sex Distribution")
plt.show()


The following code was devised from: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.agg.html

drug_sum2 = drug_sum2.groupby(["Drug Regimen"]).agg({'Tumor Volume (mm3)' : ['mean', 'median',"var","sem"]})


The code in section "Quartiles, Outliers and Boxplots" was produced with help from Tyler Aden during Office Hours.
