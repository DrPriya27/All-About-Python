# All-About-Python

* https://www.linkedin.com/posts/sanyambhutani_james-powell-so-you-want-to-be-a-python-activity-6942515634656153600-_SzL?utm_source=linkedin_share&utm_medium=android_app
* https://towardsdatascience.com/python-for-data-scientists-from-a-to-z-12adf56713f1

https://www.linkedin.com/posts/letthedataconfess_python-for-data-science-cheat-sheet-activity-6956281348361732096-gtI4/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/activity-6955404339607711744-pFBF/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/pratham-kohli_python-cheatsheet-ugcPost-6955375061998428160-xQ_W/?utm_source=linkedin_share&utm_medium=android_app

panda tips
https://www.linkedin.com/posts/giannis-tolios_datascience-python-machinelearning-activity-6953738029580640257-Z2D7/?utm_source=linkedin_share&utm_medium=android_app
https://www.linkedin.com/feed/update/urn:li:activity:6955087193358897152/?utm_source=linkedin_share&utm_medium=android_app
https://www.linkedin.com/posts/giannis-tolios_python-datascience-machinelearning-activity-6954853371191136256-TNyI/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/giannis-tolios_python-datascience-machinelearning-activity-6954853371191136256-TNyI/?utm_source=linkedin_share&utm_medium=android_app

** all about pandas
*https://www.linkedin.com/posts/saileelarahulpujari_certificate-of-accomplishment-sai-leela-activity-6940373377580679168-egEo?utm_source=linkedin_share&utm_medium=android_app

Print missing values for each column
print(music_df.isna().sum().sort_values())

https://pandastutor.com/

https://www.linkedin.com/posts/khuyen-tran-1401_python-activity-6952952459774349312-8gqS/?utm_source=linkedin_share&utm_medium=android_app

** Python Libraries
* for interpratibility (https://www.linkedin.com/posts/smasis_machinelearning-datascience-data-activity-6943539354589958144-azKA?utm_source=linkedin_share&utm_medium=android_app)
* [PyCaret] https://www.linkedin.com/feed/update/urn:li:activity:6948275260790067200?utm_source=linkedin_share&utm_medium=android_app
* https://www.linkedin.com/posts/profile-moez_build-your-own-automl-in-power-bi-using-pycaret-activity-6951520407233417216-pcEQ?utm_source=linkedin_share&utm_medium=android_app
* [Python Flask REST API] https://www.linkedin.com/posts/thomives_super-simple-python-flask-rest-api-activity-6951569281864097792-PvEd?utm_source=linkedin_share&utm_medium=android_app
* [𝐒𝐮𝐩𝐞𝐫𝐆𝐫𝐚𝐝𝐢𝐞𝐧𝐭𝐬] https://www.linkedin.com/posts/rami-krispin_python-deeplearning-pytorch-activity-6951528246849011712-alGd?utm_source=linkedin_share&utm_medium=android_app
* [Mercury] https://www.linkedin.com/posts/piotr-plonski-mljar_ive-updated-the-mercury-demo-notebooks-website-activity-6951491810045132801-M64A?utm_source=linkedin_share&utm_medium=android_app
* [mlxtend] https://www.linkedin.com/posts/bextuychiev_one-of-the-most-fun-th%C4%B1ngs-you-can-do-w%C4%B1th-activity-6951792146249093121-F7C5?utm_source=linkedin_share&utm_medium=android_app
* [Rich] https://www.linkedin.com/posts/bextuychiev_rich-%C4%B1s-one-of-the-most-beaut%C4%B1ful-and-useful-activity-6952356593510330368-aZGa?utm_source=linkedin_share&utm_medium=android_app

**Data visulization**
https://www.linkedin.com/posts/bextuychiev_how-to-choose-a-correct-dpi-and-f%C4%B1gure-s%C4%B1ze-activity-6952426323914985473-eFNl?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/feed/update/urn:li:activity:6954521156611682304/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/prithivirajdamodaran_view-is-all-you-need-if-you-are-playing-activity-6954721237717684224-dymE/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/jill-cates-44bb9147_during-the-pandemic-i-decided-to-start-an-activity-6954194311307554816-cYHZ/?utm_source=linkedin_share&utm_medium=android_app

https://www.linkedin.com/posts/h2es-institute_efficient-python-tricks-and-tools-for-data-activity-6957608460473487360-rNJi/?utm_source=linkedin_share&utm_medium=android_app


** data visualization
* https://github.com/NimritaKoul/Visualization_NumPy_Pandas/blob/main/A%20guide%20to%20choosing%20chart%20types%20for%20data%20visualization.md
* https://www.linkedin.com/posts/letthedataconfess_data-visualization-techniques-activity-6952117705172742144-jy4j?utm_source=linkedin_share&utm_medium=android_app

# Import the matplotlib.pyplot submodule and name it plt
import matplotlib.pyplot as plt

# Create a Figure and an Axes with plt.subplots
fig, ax = plt.subplots()  #subplots(3,2)  3 rows and 2 columns

# Plot MLY-PRCP-NORMAL from seattle_weather against MONTH
ax.plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-NORMAL"])  #use marker="o or v", linestyle="-- or None", color="r"
# Plot MLY-PRCP-NORMAL from austin_weather against MONTH
ax.plot(austin_weather["MONTH"], austin_weather["MLY-PRCP-NORMAL"])
ax.set_xlabel("") # or set_y_label or set_title
plt.show()

# Create a Figure and an array of subplots with 2 rows and 2 columns
fig, ax = plt.subplots(2, 2)

# Addressing the top left Axes as index 0, 0, plot month and Seattle precipitation
ax[0, 0].plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-NORMAL"])

# In the top right (index 0,1), plot month and Seattle temperatures
ax[0, 1].plot(seattle_weather["MONTH"], seattle_weather["MLY-TAVG-NORMAL"])

# In the bottom left (1, 0) plot month and Austin precipitations
ax[1, 0].plot(austin_weather["MONTH"], austin_weather["MLY-PRCP-NORMAL"])

# In the bottom right (1, 1) plot month and Austin temperatures
ax[1, 1].plot(austin_weather["MONTH"], austin_weather["MLY-TAVG-NORMAL"])
plt.show()

# Create a figure and an array of axes: 2 rows, 1 column with shared y axis
fig, ax = plt.subplots(2, 1, sharey=True)

# Plot Seattle precipitation in the top axes
ax[0].plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-NORMAL"], color='b')
ax[0].plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-25PCTL"], color='b', linestyle='--')
ax[0].plot(seattle_weather["MONTH"], seattle_weather["MLY-PRCP-75PCTL"], color='b', linestyle='--')

# Plot Austin precipitation in the bottom axes
ax[1].plot(austin_weather["MONTH"], austin_weather["MLY-PRCP-NORMAL"], color='r')
ax[1].plot(austin_weather["MONTH"], austin_weather["MLY-PRCP-25PCTL"], color='r', linestyle='--')
ax[1].plot(austin_weather["MONTH"], austin_weather["MLY-PRCP-75PCTL"], color='r', linestyle='--')

plt.show()

# Read the data from file using read_csv
climate_change = pd.read_csv('climate_change.csv', parse_dates=["date"], index_col="date")
# Add the time-series for "relative_temp" to the plot
ax.plot(climate_change.index, climate_change['relative_temp'])

# Use plt.subplots to create fig and ax
fig, ax = plt.subplots()

# Create variable seventies with data from "1970-01-01" to "1979-12-31"
seventies = climate_change["1970-01-01":"1979-12-31"]

# Add the time-series for "co2" data from seventies to the plot
ax.plot(seventies.index, seventies["co2"])


....
import matplotlib.pyplot as plt

# Initalize a Figure and Axes
fig, ax = plt.subplots()

# Plot the CO2 variable in blue
ax.plot(climate_change.index, climate_change["co2"], color='blue')

# Create a twin Axes that shares the x-axis
ax2 = ax.twinx()

# Plot the relative temperature in red
ax2.plot(climate_change.index, climate_change["relative_temp"], color='red')

plt.show()

# Define a function called plot_timeseries
def plot_timeseries(axes, x, y, color, xlabel, ylabel):

  # Plot the inputs x,y in the provided color
  axes.plot(x, y, color=color)

  # Set the x-axis label
  axes.set_xlabel(xlabel)

  # Set the y-axis label
  axes.set_ylabel(ylabel, color=color)

  # Set the colors tick params for y-axis
  axes.tick_params('y', colors=color)
  
  fig, ax = plt.subplots()

# Plot the CO2 levels time-series in blue
plot_timeseries(ax, climate_change.index, climate_change["co2"], 'blue', "Time (years)", "CO2 levels")

# Create a twin Axes object that shares the x-axis
ax2 = ax.twinx()

# Plot the relative temperature data in red
plot_timeseries(ax2, climate_change.index, climate_change['relative_temp'], 'red', "Time (years)", "Relative temperature (Celsius)")

plt.show()

fig, ax = plt.subplots()
# Plot the relative temperature data
ax.plot(climate_change.index, climate_change['relative_temp'])
# Annotate the date at which temperatures exceeded 1 degree
ax.annotate(">1 degree", xy=(pd.Timestamp('2015-10-06'), 1))
plt.show()

fig, ax = plt.subplots()
# Plot the CO2 levels time-series in blue
plot_timeseries(ax, climate_change.index, climate_change["co2"], 'blue', "Time (years)", "CO2 levels")
# Create an Axes object that shares the x-axis
ax2 = ax.twinx()
# Plot the relative temperature data in red
plot_timeseries(ax2, climate_change.index, climate_change['relative_temp'], 'red', "Time (years)", "Relative temp (Celsius)")
# Annotate the point with relative temperature >1 degree
ax2.annotate(">1 degree", xy=(pd.Timestamp('2015-10-06'), 1), xytext=(pd.Timestamp('2008-10-06'), -0.2), arrowprops={'arrowstyle':'->', 'color':'gray'})
plt.show()

# bar plots
medals = pd.read_csv('lll.csv', index_col=0)
fig,ax = plt.subplots()
ax.bar(medals.index, medals["col1"], label="aa")
ax.bar(medals.index, medals["col2"], bottom=medals["col1"], label="")
ax.bar(medals.index, medals["col3"], bottom=medals["col2"] + medals["col1"], label="")
ax.set_xticklabels(medals.index, rotation=90)
ax.legand()
plt.show()

# histogram plots
fig, ax = plt.subplots()
# Plot a histogram of "Weight" for mens_rowing
ax.hist(mens_rowing["Weight"])

# Compare to histogram of "Weight" for mens_gymnastics
ax.hist(mens_gymnastics["Weight"])

# Set the x-axis label to "Weight (kg)"
ax.set_xlabel("Weight (kg)")
# Set the y-axis label to "# of observations"
ax.set_ylabel("# of observations")
plt.show()

fig, ax = plt.subplots()
# Plot a histogram of "Weight" for mens_rowing
ax.hist(mens_rowing["Weight"], histtype='step', label="Rowing", bins=5)
# Compare to histogram of "Weight" for mens_gymnastics
ax.hist(mens_gymnastics["Weight"], histtype='step', label="Gymnastics", bins=5)
ax.set_xlabel("Weight (kg)")
ax.set_ylabel("# of observations")
# Add the legend and show the Figure
ax.legend()
plt.show()
fig.savefig('my_figure.png')
fig.savefig('my_figure_300dpi.png', dpi=300)

fig.set_size_inches([3, 5])
fig.savefig('figure_3_5.png')

## box plots
fig, ax = plt.subplots()

# Add a bar for the rowing "Height" column mean/std
ax.bar("Rowing", mens_rowing["Height"].mean(), yerr=mens_rowing["Height"].std())

# Add a bar for the gymnastics "Height" column mean/std
ax.bar("Gymnastics", mens_gymnastics["Height"].mean(), yerr=mens_gymnastics["Height"].std())

# Label the y-axis
ax.set_ylabel("Height (cm)")

plt.show()

fig, ax = plt.subplots()

# Add the Seattle temperature data in each month with standard deviation error bars
ax.errorbar(seattle_weather["MONTH"], seattle_weather["MLY-TAVG-NORMAL"], yerr=seattle_weather["MLY-TAVG-STDDEV"])

# Add the Austin temperature data in each month with standard deviation error bars
ax.errorbar(austin_weather["MONTH"], austin_weather["MLY-TAVG-NORMAL"], yerr=austin_weather["MLY-TAVG-STDDEV"])

# Set the y-axis label
ax.set_ylabel("Temperature (Fahrenheit)")
plt.show()

fig, ax = plt.subplots()

# Add a boxplot for the "Height" column in the DataFrames
ax.boxplot([mens_rowing["Height"], mens_gymnastics["Height"]])

# Add x-axis tick labels:
ax.set_xticklabels(["Rowing", "Gymnastics"])

# Add a y-axis label
ax.set_ylabel("Height (cm)")

plt.show()

## scatter plot (bivariate comparison)
fig, ax = plt.subplots()
# Add data: "co2" on x-axis, "relative_temp" on y-axis
ax.scatter(climate_change["co2"], climate_change["relative_temp"])
# Set the x-axis label to "CO2 (ppm)"
ax.set_xlabel("CO2 (ppm)")
# Set the y-axis label to "Relative temperature (C)"
ax.set_ylabel("Relative temperature (C)")
plt.show()

fig, ax = plt.subplots()

# Add data: "co2", "relative_temp" as x-y, index as color
ax.scatter(climate_change["co2"], climate_change["relative_temp"], c=climate_change.index)

# Set the x-axis label to "CO2 (ppm)"
ax.set_xlabel("CO2 (ppm)")

# Set the y-axis label to "Relative temperature (C)"
ax.set_ylabel("Relative temperature (C)")

plt.show()

# Use the "ggplot" style and create new Figure/Axes
plt.style.use('ggplot')  #'default', 'bmh', 'seaborn-colorblind'
fig, ax = plt.subplots()
ax.plot(seattle_weather["MONTH"], seattle_weather["MLY-TAVG-NORMAL"])
plt.show()

# Use the "Solarize_Light2" style and create new Figure/Axes
plt.style.use('Solarize_Light2')
fig, ax = plt.subplots()
ax.plot(austin_weather["MONTH"], austin_weather["MLY-TAVG-NORMAL"])
plt.show()

# Extract the "Sport" column
sports_column = summer_2016_medals["Sport"]
# Find the unique values of the "Sport" column
sports = sports_column.unique()
# Print out the unique sports values
print(sports)

fig, ax = plt.subplots()

# Loop over the different sports branches
for sport in sports:
  # Extract the rows only for this sport
  sport_df = summer_2016_medals[summer_2016_medals["Sport"] == sport]
  # Add a bar for the "Weight" mean with std y error bar
  ax.bar(sport, sport_df["Weight"].mean(), yerr=sport_df["Weight"].std())

ax.set_ylabel("Weight")
ax.set_xticklabels(sports, rotation=90)

# Save the figure to file
fig.savefig("sports_weights.png")

## matplotlib gallery

# annotating time sereis data
** VS Code
* https://www.linkedin.com/posts/mihir-naik-52b6674_the-vs-code-server-activity-6951734386434138112-Ok9c?utm_source=linkedin_share&utm_medium=android_app

# strings
my_string.splitlines()  #will split the string only at \n character and create list of strings

#join method (concatenate strings from list or another iterable
print("".join(my_list))  #"" are the seperator here

#Strips characters from left ot right (need to check)
mystring.strip()

mystring.rstrip()  #remove characters from the right end
mystring.lstrip() #remove characters form the left end

##search target string for a speificied substring
mystring.find("hello",start,end)  #start and end are optional here  # will return index if not found will return -1

mystring.index("hello",start,end) #same as find but for not found case it will throw an valueerror

## counting occurences
mystring.count('fruit')

## replacing substrings
mystring.replace('house','car')
mystring.replace('house','car',2)  #replace only first 2 instances


#formatting sting
1) positional formating
print("{} has a friedn called {}".format(aksay,suraj))  
print("{2} has a friedn called {1}".format(aksay,suraj))  
name1="aksay"
name2="suraj"
print("{nameone} has a friedn called {nametwo}".format(nameone=name1,nametwo=name2)) #named placeholders

my_dic={"name1": "aksay", "name2":"suraj"}
print('{my_dict[name1]} has a friend called {my_dict[name2]}'.format(my_dict))

##format specifier {index:specifier}
print('only {0:f} of the {1} produces is {2}.".format....)   #use {0:.2f} for printing only two decimal places

##formatting date time
from datetime import datetime
print(datetime.now())

print("Today's date is (:%Y-%m-%d %H:%H".format(datetime.now())

2) formatting string literal
print(f"{name1} has a frind called {name2}")




print(1 * 3) #== 3
print("1" * 3) #=="111"

##docstrings for function definition
def ...:
  """ this is all abut """  #triple double quote
  new_tuple = (x, y)
  return new_tuple  # returing multiple values
  
## scope and user defined functions
global- defined in main body
local-  defined in a function (to make it global use global keyword)
build in- names in the pre-defined built-ins module (import builtins and than dir(builtins))
Dict is unordered 

Local scope se global per jate h
Nested function ko non local bana sakte h using nonlocal keyword otherwise it's scope will be limited to local space only

# default argument
def power(number, pow=1):  # will work both on (power(9), power(9,2)
   ------
   
#flexible argument using *args
def power(*args):          # will work on power(1) power(1,2) power(1,2,3)

def print_all(**kwargs):
   for key,value in kwargs.items():
      print(key+":"+value)
print_all(name="priya", job="research")

#lambda functions
raise_to_power =  lambda  x,y:x**y
raise_to_power(2,3)  # will return 8

##map() applies the function to all elements in the sequence
map(lambda num: num**2, nums) #here nums is a list of numbers

##filter()
filter(lambda strings:len(strings)>6, list_string)

##reduce()
from functools import reduce
reduce(lambda item1,item2: item1 + item2, list_string)

## errors and exceptions
# TypeError, UnboundLocalError, UnicodeError

def sqrt(x):
  if x<0:
    raise ValueError('...')
  try:
    return x ** 0.5
  except TypeError:
    print('...')
    
## iterating over iterables (lists, strings, dict and file connections [ file=open('file.txt); it=iter(file); print(next(it)) # will print whole file content); next()
word = 'Da'
iterator = iter(word)
next(iterator)  # need to write it again and again
print(*iterator) # iterating at once

#playing with iterables
using enumerate() # will give index as well
e=enumerate(list_strint)
print(list(e)) # will produce of list of tuples with index and corresponding value informaiton

using zip()
z= zip(list_string1, list_string2) #will produce lis to tuples with first value and second value
print(list(z))
print(*z)

#list comprehensions
new_nums = [num + 1 for num in nums]
     .....
   
 
https://www.youtube.com/watch?v=cKPlPJyQrt4

