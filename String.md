```
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

print(1 * 3) #== 3
print("1" * 3) #=="111"
```

### Formatting sting
```
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
```



