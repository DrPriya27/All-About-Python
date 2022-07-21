# All-About-Python

* https://www.linkedin.com/posts/sanyambhutani_james-powell-so-you-want-to-be-a-python-activity-6942515634656153600-_SzL?utm_source=linkedin_share&utm_medium=android_app
* https://towardsdatascience.com/python-for-data-scientists-from-a-to-z-12adf56713f1

** all about pandas
*https://www.linkedin.com/posts/saileelarahulpujari_certificate-of-accomplishment-sai-leela-activity-6940373377580679168-egEo?utm_source=linkedin_share&utm_medium=android_app

Print missing values for each column
print(music_df.isna().sum().sort_values())

https://pandastutor.com/

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

# annotating time sereis data
** VS Code
* https://www.linkedin.com/posts/mihir-naik-52b6674_the-vs-code-server-activity-6951734386434138112-Ok9c?utm_source=linkedin_share&utm_medium=android_app

https://www.youtube.com/watch?v=cKPlPJyQrt4

