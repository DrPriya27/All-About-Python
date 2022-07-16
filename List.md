### Aliasing

a = [81,82,83]
b = [81,82,83]

print(a is b) #False
b = a
print(a == b) #True
print(a is b) #True
b[0] = 5
print(a) #[5,82,83]

### Cloning lists
a = [81,82,83]
b = a[:]
print(a == b) #True
print(a is b) #False

b[0] = 5
print(a) #[81,82,83]
print(b) #[5,82,83]

### Making reference diagrams
x = [1,2,3]
y = x
x += [4,5]
y = y + [6]
print(x) #[1,2,3,4,5]
print(y) #[1,2,3,4,5,6]

### Non-mutating methods on Strings
#Example 1
ss="     Hello, World    "
els = ss.count("l")
print(els)  #3

print("**"+ss.strip()+"**") #**Hello, World**
news = ss.replace("o","**")
print(news) #      Hell**, W**rld  

#Example 2
ss = "Hello, World"
print(ss.upper()) #HELLO, WORLD

tt = ss.lower()
print(tt) #hello,world
print(ss) #Hello, World

#Example 3
s ="python rocks"
print(s[1] * s.index("n")) #yyyyy

#Example 4
print('{:.2f} is discounted by {}% is ${:.2f}.'.format(a,b,c)) #will print upto two decimals





