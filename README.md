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

--------------------------------------------
#Plot Properties
import pandas
from bokeh.plotting import figure, output_file, show

p=figure(plot_width=500,plot_height=400, tools='pan')

p.title.text="Cool Data"
p.title.text_color="Gray"
p.title.text_font="times"
p.title.text_font_style="bold"
p.xaxis.minor_tick_line_color=None
p.yaxis.minor_tick_line_color=None
p.xaxis.axis_label="Date"
p.yaxis.axis_label="Intensity"    

p.line([1,2,3],[4,5,6])
output_file("graph.html")
show(p)

-----------------------------------------
#Weather Plotting
from bokeh.plotting import figure
from bokeh.io import output_file, show
import pandas

df = pandas.read_excel("some.xlsx")

Temp = df["Temperature"]
Pres = df["Pressure"]

f = figure(plot_width = 500, plot_height = 500, tools = 'pan')

f.title.text = "Temperature And Air Pressure"
f.title.text_color = "Gray"
f.title.text_font = "Times"
f.title.text_font_style = "bold"
f.title.text_font_size = '16pt'
f.xaxis.minor_tick_line_color = "Blue"
f.yaxis.minor_tick_line_color = "Blue"
f.xaxis.axis_label = "Temperature(°C)"
f.yaxis.axis_label = "Pressure(hPa)"


f.circle(Temp/10, Pres/10, size = 0.5)

output_file("graph.html")
show(f)

------------------------------------------
