# Assignment_3
Python assignment 3

1)Write a Python Program to implement your own myreduce() function which works exactly
like Python's built-in function reduce()

def my_reduce(func, seq):
   first = seq[0]
   for i in seq[1:]:
    first = func(first, i)
   return first
   
   
2 Write a Python program to implement your own myfilter() function which works exactly like
Python's built-in function filter()

def myfilter(anyfunc, sequence):
 # Initialize empty list
 result = []
 # iterate over sequence of items in sequence and apply filter function
 for item in sequence:
  if anyfunc(item):
   result.append(item)

 # return funal output
 return result

3 Implement List comprehensions to produce the following lists.
Write List comprehensions to produce the following Lists


['A', 'C', 'A', 'D', 'G', 'I', ’L’, ‘ D’]
word = "ACADGILD"
alphabet_list = [ alphabet for alphabet in word ]
print ("ACADGILD => " + str(alphabet_list))

['x', 'xx', 'xxx', 'xxxx', 'y', 'yy', 'yyy', 'yyyy', 'z', 'zz', 'zzz', 'zzzz']

input_list = ['x','y','z']
result = [ item*num for item in input_list for num in range(1,5)  ]
print("['x','y','z'] => " +   str(result))

'x', 'y', 'z', 'xx', 'yy', 'zz', 'xxx', 'yyy', 'zzz', 'xxxx', 'yyyy', 'zzzz']

input_list = ['x','y','z']
result = [ item*num for num in range(1,5) for item in input_list  ]
print("['x','y','z'] => " +   str(result))


[[2], [3], [4], [3], [4], [5], [4], [5], [6]]

input_list = [2,3,4]
result = [ [item+num] for item in input_list for num in range(0,3)]
print("[2,3,4] =>" +  str(result))

[[2, 3, 4, 5], [3, 4, 5, 6], [4, 5, 6, 7], [5, 6, 7, 8]]

input_list = [2,3,4,5]
result = [ [item+num for item in input_list] for num in range(0,4)  ]
print("[2,3,4,5] =>" +  str(result))

[(1, 1), (2, 1), (3, 1), (1, 2), (2, 2), (3, 2), (1, 3), (2, 3), (3, 3)]

input_list=[1,2,3]
result = [ (b,a) for a in input_list for b in input_list]
print("[1,2,3] =>" +  str(result))

4 Implement a function longestWord() that takes a list of words and returns the longest one.

def find_longest_word(words_list):
    word_len = []
    for n in words_list:
        word_len.append((len(n), n))
    word_len.sort()
    return word_len[-1][1]
