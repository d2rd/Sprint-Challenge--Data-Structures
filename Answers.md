## Questions
1. What are the order of insertions/removals for the following data structures?
   - **Stack**
      Stack is LIFO (Last in First Out).  The common analogy is a stack of plates:
      - The first plate is on the bottom (sitting on the counter).
      - The second plate goes on top of the first.
      - The 'stack.push()' method is used to add a plate.
      - The last plate pushed in sits on the top of the stack.
      - The 'stack.pop()' method is used to remove each plate in succession from the top of the stack to the desired plate.
      - To access the first plate on the counter you must remove all the plates above it.  Therefore, if you push 10 plates onto the stack you must 'pop()' the stack 9 times to get to the first plate.
      - Popping the plate stack 10 times will result in an empty stack. Empty stacks return a value of 'null'.
      - The size of the stack can be determined using the 'stack.length()' method.
      - Using the above example:
        - 'stack.length()' will return a value of 10.
        - Running 'stack.pop()' for stack.length(-1) will navigate to the first plate sitting on the counter.

   - **Queue**
      Queue is FIFO (First in First Out).  The common analogy is a line at an airplane gate:
      - The first passenger is at the head of the line and will board first.
      - The second passenger boards behind the first.
      - The 'queue.enqueue()' method is used to add a passenger that passenger goes behind the last passenger already in line.
      - The last passenger enqueued in stands on the end of the queue.
      - The 'queue.dequeue()' method is used to remove each passenger in succession from the beginning of the queue.
      - To navigate to any given passenger in line you must use the queue.contains() to locate that passenger by its value (i.e. name on boarding pass).  
      - The size of the queue can be determined using the 'queue.length()' method.
      

2. What is the retrieval time complexity for the following data structures?
   - **Linked List** (Average) Source: http://bigocheatsheet.com/
      - Access: 0(1)
      - Search: 0(n)
   - **Hash Table** (Average) Source: http://bigocheatsheet.com/
      - Access: N/A
      - Search: 0(1)
   - **Binary Search Trees** (Average) Source: http://bigocheatsheet.com/
      - Access: 0(log(n)
      - Search: 0(log(n)

3. What are some advantages to using a Hash Tables over an array in JavaScript?
      - Arrays use an index to identify value locations.  Arrays require you to examine each element in order to find the desired item. On average, the amount of time it takes to find a value in an array is proportional to the number of items in your array. Therefore, the larger the array the more items that must be examined.  The more items, the longer it will take to find an item. If your target is in the middle of a huge array this will take a lot of time.   

      -  On the other hand a hash table uses a key to identify value locations (key|value pairs) the hashing function generates a location 'identifier' that references a particular bucket for each key.  Visualize a bookcase with multiple shelves.  The hash function creates a pointer that indicates the exact location of the target value.  The size of the hash is less important because each value has a specific location and the hash-table knows exactly where to go to retrieve the value.

      - Once the key|value pair has been hashed there is an additional performance game because the hash-table knows the location of that key whereas the array has to 'plod' along starting at the beginning and iterating through each element until the target is located.
      
