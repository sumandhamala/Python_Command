**Basic methods and functions in Python**
1. **Difference between sequence (list, tuple, string) and collection (dictionary, set, frozenset)**.
 	* Numeric_List or python array = [2, 8, 1, 4, 6, 3, 7] 
	* List = ['q', 'w', 'r', 'e', 't', 'y'] 
	* Tuple = ('q', 'w', 'e', 'r', 't', 'y') 
	* Dictionary = {'q':1, 'w':2, 'e':3, 'r':4, 't':5, 'y':6} 
        * set = {'q', 'w', 'e', 'r', 't', 'y'} 
        * Frozenset = frozenset(('q', 'w', 'e', 'r', 't', 'y')) 
	        
2. **To find index of a particular element in an array, tuple and dictionary.**
   Index = Variable.index(value of which index needs to be find)
   Example1: A=[1,2,3] # an array 
            Index=A.index(2) # command to find index of the element 2
            print(Index)      # print the index 
            
Example2:  # Python tuple index() Method  
          val = ('a','b','c','d')   # Creating a dictionary 
          print(val)  
          # Calling Method  
          index = val.index('d')  # Finds index  
          print("Index of k is: ",index)  
          
          
3) **Difference between sort() and sorted() function:**
 Syntax : sorted(iterable, key=optional, reverse=optional) # takes three parameters of which key and reverse are optional.
 	iterable means the list, tuple, dictionary or array to be sorted
 If you want to sort a list but still have the original unsorted version, then you would use the sorted() function. 
 If maintaining the original order of the list is unimportant, then you can call the sort() function on the list.
 Example: 	List = [3,2,1,4]
	new_list = sorted(List, Reverse=False) % gives sorted new list without changing order of List means original variable is preserved
	print(new_list)
	print(List) #Original list not modified 
	new_list = sorted(List, Reverse=True) % The argumnt Reverse will sort in descending order
            new_List = List.sort()
	    
(4) **function filter()**	    
	numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
	# Will return true if input number is even
	def even(x):
    		return x % 2 == 0
	# non-pythonic approach
	even_nums = []
	for num in numbers:
    		if even(num):
        	even_nums.append(num) 
	print('Non-Pythonic Approach: ', even_nums)
	# pythonic approach
	even_n = filter(even, numbers)
	print('Pythonic Approach: ', list(even_n))
	
(5) **function zip()**
       first = [1, 3, 8, 4, 9]
	second = [2, 2, 7, 5, 8]
	# Iterate over two or more list at the same time
	for x, y in zip(first, second):
    	print(x + y)
	
(6) **function map()**
     nums = [1, 2, 3, 4, 5]
	# this function will calculate square
	def square_num(x): 
   		 return x**2
	# non-pythonic approach
	squares = []
	for num in nums:
    	squares.append(square_num(num))
 
	print('Non-Pythonic Approach: ', squares)
	# pythonic approach
	x = map(square_num, nums)
	print('Pythonic Approach: ', list(x))


