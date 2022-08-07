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

* https://github.com/NimritaKoul/Visualization_NumPy_Pandas/blob/main/A%20guide%20to%20choosing%20chart%20types%20for%20data%20visualization.md
* https://www.linkedin.com/posts/letthedataconfess_data-visualization-techniques-activity-6952117705172742144-jy4j?utm_source=linkedin_share&utm_medium=android_app


# annotating time sereis data
** VS Code
* https://www.linkedin.com/posts/mihir-naik-52b6674_the-vs-code-server-activity-6951734386434138112-Ok9c?utm_source=linkedin_share&utm_medium=android_app



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

