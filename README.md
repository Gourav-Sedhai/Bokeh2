# Bokeh2
#Interacting with bokeh
-
#Plotting Education Graph

#importing bokeh and pandas
from bokeh.plotting import figure
from bokeh.io import output_file, show
import pandas

#importing csv file
df = pandas.read_csv("bachelors.csv")

#storing in a variable
year = df["Year"]
engg = df["Engineering"]

#Creating output file
output_file("Education_Graph.html")

#Creationg object
f = figure()

#Creating line plot
f.line(year, engg)

#Output
show(f)

-
