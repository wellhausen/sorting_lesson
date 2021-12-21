<!-- >>>>>>>>>>>>>>>>>>>>>> BEGIN CHALLENGE >>>>>>>>>>>>>>>>>>>>>> -->
<!-- Replace everything in square brackets [] and remove brackets  -->

### !challenge

* type: code-snippet
* language: python3.6
* id: d6cd968a-7b7f-495e-b747-49243531f309
* title: Python Snippet incorporated
<!-- * points: [1] (optional, the number of points for scoring as a checkpoint) -->
<!-- * topics: [python, pandas] (optional the topics for analyzing points) -->

##### !question

Given the following Quick Sort Algorithm, fill in the three missing variables within the angled brackets <>.

##### !end-question

##### !placeholder

```py
def quick_sort(arr):

    elements = len(arr)
    
    #Base case
    if elements < 2:
        return arr
    
    current_position = 0 #Position of the partitioning element

    for i in range(1, elements): #Partitioning loop
         if arr[i] <= arr[0]:
              current_position += 1
              temp = arr[i]
              arr[i] = arr[current_position]
              arr[< 1) What variable goes here? >] = temp

    temp = arr[0]
    arr[0] = arr[< 2) And here? >] 
    arr[current_position] = temp #Brings pivot to it's appropriate position
    
    left = quick_sort(arr[0:current_position]) #Sorts the elements to the left of pivot
    right = quick_sort(arr[current_position+1:elements]) #sorts the elements to the right of pivot

    arr = left + [arr[< 3) And here? >]] + right #Merging everything together
    
    return arr



array_to_be_sorted = [4,2,7,3,1,6]
print("Original Array: ",array_to_be_sorted)
print("Sorted Array: ",quick_sort(array_to_be_sorted))
```

##### !end-placeholder

##### !tests

```py
import unittest
import main as p
import numpy as np

class TestPython1(unittest.TestCase):
  def test_one(self):
    self.assertEqual([1, 2, 3, 4, 6, 7], p.quick_sort())
```

##### !end-tests

<!-- other optional sections -->
<!-- !hint - !end-hint (markdown, hidden, students click to view) -->
<!-- !rubric - !end-rubric (markdown, instructors can see while scoring a checkpoint) -->
<!-- !explanation - !end-explanation (markdown, students can see after answering correctly) -->

### !end-challenge

<!-- ======================= END CHALLENGE ======================= -->