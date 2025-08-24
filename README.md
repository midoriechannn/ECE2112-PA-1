## ECE2112 PA #1 | DOCUMENTATION 

**1. ALPHABET SOUP PROBLEM: Create a function that takes a string and returns a string with its letters in alphabetical order.**

  **EXAMPLE:**
   
   alphabet_soup("hello") ➜ ehllo

   alphabet_soup("hacker") ➜ acehkr 

**CODE**
```
#Defining our function named "alphabet_soup"
def alphabet_soup(text):
```
▸ First, we need to define our function which have a specific work to do. It will accept an argument called "text". 

```
 #Convering the string into a list
    conv = list(text)  
```
▸ Since our input is a string, this code is for converting text entered, into a list.  

```
 #For removing whitespaces if present
    while ' ' in conv: 
        conv.remove(' ') 
```
▸ The while loop is used to remove any whitespaces. I include this since, there are some cases where a user might input a sentences and by doing this we can remove the whitespaces.  

```
#Sorting the list alphabetically 
    conv.sort() 
```
▸ This code is basically sorting the entered text alphabetically. 

```
#Return sorted list as string
    final = "".join(conv) 
    return print (final)  
```
▸ The text that we converted into a list is converted back to string by joining the individual elements using ".join() function. The last line also indicate that it is printed at the same time.  

```
#Function call 
alphabet_soup("hello")  
alphabet_soup("hacker") 
alphabet_soup("meow k") 
```
▸ Calling the function with different arguments to have a visible output. 

**OUTPUT**  
```
ehllo
acehkr
ekmow
```



**2. EMOTICON PROBLEM:Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon.**

**EXAMPLE:**

emotify(“Make me smile”) ➞ Make me :) 

emotify(“I am mad”) ➞ I am >:( 

**CODE** 

```
#Defining our function named "emotify"
def emotify(text): 
```
▸ Defining our function named "emotify" that accepts an argument called "text". 

```
#Initializing value each keys
    emoticon= {"smile": ":)", 
           "grin" : ":D", 
           "sad"  : ":((",
           "mad"  : ">:(",} 
```
▸ Initialized a dictionary named "emoticons". The keys are the words, while the values are  the respective emotes to each words.  

```
#Loop thru dictionary items 
    for key, value in emoticon.items(): 
        
        #For replacing the key with corresponding values(emoticons) 
        if key.lower() in text.lower(): 
            return print(text.replace(key,value))

    #If no match is found in the text, return the original text
    return print(text)
```
▸ A "for" loop goes through the dictionary items then it does the following condition wheter a key is present in the string "words".  If the condition is met, the words will automatically change. It is done by using ".replace()" function. 

▸The original statement is also returned if the condition is not met. 

```
#Function Call
emotify ("Make me smile")  
emotify ("I am mad")
``` 
▸ Calling the function with different arguments to have a visible output. 

**OUTPUT** 
```
Make me :)
I am >:(
```
**3.Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.** 

**EXAMPLE:** 

lst = [1,2,3,4,5,6] 

Output: 

first: 1  

middle: [2,3,4,5] 

last: 6 

**CODE** 

```
#Defining the list
lst = [1,2,3,4,5,6] 
```
▸ Defining the list named "lst" and have a values [1,2,3,4,5,6].

```
#Indexing to unpack the list 
first = lst[0] 
middle = lst[1:-1] 
last = lst[-1] 
```
▸ A variable "first" is initialized with the first ([0]) value in our list named "lst".

▸ A variable "middle" is initialized, the same as the first one but it holds the the values of our list named "lst".  
between the first and last index ([1:-1]).

▸ A variable "last" is initialized with the last value ([-1])in our list named "lst".
```
#Print the three values
print("first:", first) 
print("middle:", middle)  
print("last:", last)
```
▸ Calling the function with different arguments to have a visible output. 

**OUTPUT** 
```
first: 1
middle: [2, 3, 4, 5]
last: 6
```
