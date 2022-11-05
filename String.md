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
print(f'pi is equal to {pi}') #use{pi:.3f} for printing three decimal places, use{pi:.3} for printing whole number as three digit long, use{pi:12.3f} for leaving 12 spaces before printing, use{pi:012.3f} for 12 padding but with leading zero, use{pi:+.3f} to have + in front, use{pi:<12.3f} will leave space in the right, use{pi:^12.3f} for centrally aligned

```

### Regular expressions
![Screenshot_20221105-143907_Samsung Internet](https://user-images.githubusercontent.com/54790008/200112668-4b7c2cfd-aa71-4cd2-a2d5-4106df318341.jpg)

![Screenshot_20221105-144044_Samsung Internet](https://user-images.githubusercontent.com/54790008/200112680-6bad9e87-042e-4e2c-92d8-f0bdec1a360c.jpg)

![Screenshot_20221105-144121_Samsung Internet](https://user-images.githubusercontent.com/54790008/200112685-22a7b0d6-6f21-431a-b129-7577b24e99a9.jpg)

![Screenshot_20221105-144134_Samsung Internet](https://user-images.githubusercontent.com/54790008/200112689-6af7e1e0-85cf-40df-b994-4a8e237ef54e.jpg)

![Screenshot_20221105-144158_Samsung Internet](https://user-images.githubusercontent.com/54790008/200112629-42d29aa8-6db8-4fcd-8f3f-848b54853b5e.jpg)




