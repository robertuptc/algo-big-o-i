# Big O Answers

## Snippet 1 -
### Big O: O(N) - linear time 
### Explanation: as the number of iterations grow, the time complexity grows linearly
```python
def largest(array, value):
  for item in array:
    if item > value:
      return False
  return True 
```


## Snippet 2 -
### Big O: O(n * m) - linear time
### Explanation: They loops are not nested loops. Each iteration occurs independently from each other and both run linearly in time. 

```python
def info_dump(customers):
  
  print('Customer Names:')
  for customer in customers: 
    print(customer['name'])
  
  print('Customer Locations:')
  for customer in customers: 
    print(customer['country'])
  
```

## Snippet 3 -
### Big O: O(1) - constant time
### Explanation: Even if more elements are added to the array, the function only accesses the first element, therefore the time complexity doesn't increase

```python
def first_element_is_red(array):
  return array[0] == 'red' 
```

## Snippet 4 -
### Big O: O(n^2) - quadratic time
### Explanation: time complexity increases as input size increases for both iterations since both depend of the the lenght of the same list. 


```python
def duplicates(array):
  for index1, item1 in enumerate(array):
    for index2, item2 in enumerate(array):
      if index1 == index2:
        continue
      if item1 == item2:
        return True
  return False
``` 

## Snippet 5 -
### Big O: 0(n * m) - linear time 
### Explanation: Each iteration runs independently based on their different list inputs. They do not depend on each other, but they both run linearly in time

```python
words = ['chocolate', 'coconut', 'rainbow']
endings = ['cookie', 'pie', 'waffle']

for word in words:
  for ending in endings:
    print(word + ending)

```

## Snippet 6 -
### Big O: O(n) - linear time
### Explanation: Runtime grows proportionally as the input size is increased.

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

def print_array(array):
  for item in array:
    print(item)

```

## Snippet 7 -
### Big O: O(n * m) - linear time
### Explanation: the while loop depends on the output of the for loop. Runtimes grows proportionally as the input size increases

```python
# this is insertion sort
def insertionSort(arr): 
  for i in range(1, len(arr)): 
    key = arr[i] 
    j = i-1
    while j >=0 and key < arr[j] : 
      arr[j+1] = arr[j] 
      j -= 1
    arr[j+1] = key 
```

## Snippet 8 -
### Big O: O(n * m)
### Explanation: Both loops depend on the same input elements. Both runtimes will grow proportionally

```python
for i in range(len(my_list)):
  min_idx = i
  for j in range(i+1, len(my_list)):
      if my_list[min_idx] > my_list[j]:
          min_idx = j

  my_list[i], my_list[min_idx] = my_list[min_idx], my_list[i]
```
