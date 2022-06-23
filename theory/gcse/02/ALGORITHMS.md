# 2.1 Algorithms

## 2.1.1 Computational thinking

There are three key principles to computational thinking at GCSE:
 - [decomposition](#decomposition)
 - [abstraction](#abstraction)
 - [algorithmic thinking](#algorithmic-thinking)

### Decomposition

**Decomposition** is the dissolution of a **complex problem** into more manageable parts.

A **complex problem** refers to any problem that does not have an immediate solution at first glance. Computational thinking involves taking the problem and breaking it down into a series of more manageable problems, which can be looked at individually. The simple solutions to the smaller problems can be used to write the solution to the complex problem.

### Abstraction

**Abstraction** is the process of filtering out (ignoring) out the unnecessary characteristics of problems that are not needed so that those that are needed can be concentrated on. It allows us to create a general idea of what the problem is and how to solve it - this idea is called a **model.**

As stated by the BBC:
 > An example of abstraction is the London Underground map. It details tube and rail lines and the stations that are on them. That is all that is required for a passenger to be able to plan a journey from one station to another. Other details, such as real geographical location, distance between stations, depth underground and number of platforms are not included as they are irrelevant to journey planning on the Underground.
 >
 > <img src="https://ichef.bbci.co.uk/images/ic/1008xn/p06rm6k4.jpg" height=200px>

## 2.1.2 Evaluating common search algorithms

### Linear search

A **linear search** is a simple way of searching a data set:
 1. get the length of the data set.
 2. set an counter (`i`) to 0.
 3. check if the value at index `i` is the desired value.
 4. if it matches, the value is found and the search is concluded.
 5. if not, increment `i` and go back to step 3 until:
    1. the desired value is found, or...
    2. ...there are no remaining values.

A linear search algorithm can be seen in pseudocode:
```js
// 'list' is the data set we are analysing
// 'value' is the value we are searching for
function linearSearch(list, value):
  for (i in range(list.length - 1)):
    if (list[i] == value):
      // the list value at index i is equal to the desired value, so we output a message to stdout.
      print("Found at position " + i);
      return; // 'return' exits the function, therefore concluding the search.
    endif
  endfor

  // if the function reaches this point, the value was not found in the data set.
  print("Value was not found.");
endfunction
```

Linear searches can be very inefficient. If the desired value happens to be last in the list, **all list items have to be checked** before the value is found.

However, linear searches *do* work on both **ordered and unordered** lists.

### Binary search

A **binary search** is a more efficient way of searching a data set:
 1. set a counter `i` to the middle position in the data set. This is the **midpoint.**
 2. if the value held there is a match, the search ends.
 3. if the value at the midpoint is **less** than the desired value, the list is divided in half. The lower half of the list is **ignored** (including the midpoint) and the search keeps to the upper half.
 4. if the value at the midpoint is **more** than the desired value, the list is divided in half. The upper half of the list is **ignored** (including the midpoint) and the search keeps to the lower half.
 5. the search moves to the midpoint of the remaining items. Steps 2-4 then continue until a match is made or there are no more items.

A binary search algorithm can be seen in pseudocode:
```js
// 'list' is the data set we are analysing
// 'value' is the value we are searching for
function binarySearch(list, value):
  var lowerBound = 0;
  var upperBound = list.length - 1; // the last index in the list

  while (lowerBound <= upperBound)
    var midpoint = roundUp((upperBound + lowerBound) / 2);

    if (list[midpoint] == value)
      // the list value at the midpoint is equal to the desired value, so we output a message to stdout.
      print("Found at position " + i);
      return; // 'return' exits the function, therefore concluding the search.
    endif

    if (list[midpoint] > value)
      // the midpoint is more than the value - the upper bound is lowered so that the upper half is ignored.
      upperBound = midpoint - 1;
    else
      // the midpoint is less than the value - the lower bound is raised so that the lower half is ignored.
      upperBound = midpoint + 1;
    endif
  endwhile

  // if the function reaches this point, the value was not found in the data set.
  print("Value was not found.");
endfunction
```

A binary search **only works if the list is ordered.**

## 2.1.3 Evaluating common sorting algorithms

### Bubble sort

Bubble sort works like this:
 1. start at the beginning of the list.
 2. compare the first value in the list with the next one up. If the first value is bigger, swap the two values' positions.
 3. move to the second value in the list. Again, compare this value with the next and swap if necessary.
 4. keep going until the last item is reached.
 5. go back to the start of the list.

Each run through the list is known as a **pass.** Bubble sort continues until a pass is made in which no values are swapped - here, the list has been sorted and the program is concluded.

```js
function bubbleSort(list)
  var sorted = false;

  // do this for as long as the list is not sorted; each iteration of this loop is one pass.
  while (sorted == false)
    var swaps = 0;

    for (i in range(list.length - 1)):
      // loop through the list; if the current value is greater than the one after...
      if (list[i] > list[i + 1]):
        // ...swap the positions of the two values.
        var temp = list[i];
        list[i] = list[i + 1];
        list[i + 1] = temp;
        swaps += 1;
      endif
    endfor

    if (swaps == 0)
      // if no swaps were made, we know the list has been sorted so the while loop ends
      sorted = true;
    endif
  endwhile
endfunction
```

### Insertion sort

 1. start with the **second value in the list.**
 2. if this value is greater than the value to the **left** of it, make no changes.
 3. otherwise, this value is repeatedly moved left until it meets a value that is less than it.
 4. the sort process than starts again with the next value - this continues until the end of the list.

Although more efficient than a bubble sort, insertion sorts work best with smaller data sets. Large data sets are more efficiently handled by **merge sorts**.

For more information, see [BBC Bitesize](https://www.bbc.co.uk/bitesize/guides/zjdkw6f/revision/6).

### Merge sort

Merge sorts are more complex than insertion sort, and far more complex than bubble sort. However, merge sort is *far* more optimised.

See [BBC Bitesize](https://www.bbc.co.uk/bitesize/guides/zjdkw6f/revision/5).

## 2.1.4 The production of algorithms

### Algorithmic thinking
**Algorithmic thinking** is focusing on how a desired solution can be reached by identifying the necessary steps to get there - a key part of [computational thinking](#211-computational-thinking), this process includes **algorithm** production.

An **algorithm** refers to any process to solving a problem. Algorithms are typically written as **[pseudocode](#pseudocode)** or a **[flowchart](#flowcharts)**.

Before an algorithm can be designed, the problem should be fully [decomposed](#decomposition). The following points should be considered:
 1. What are the inputs to the problem?
 2. What will be the outputs to the problem?
 3. In what order should instructions be carried out?
 4. What decisions need to be made in the problem?
 5. Are any areas of the problem repeated?

Then, the design process of the algorithm can be carried out.

### Pseudocode

Pseudocode is not a programming language, but rather a way of describing a set of instructions in a way that *resembles* source code. There is a standardised syntax for pseudocode:
```js
while (answer != "computer science")
  var answer = input("What is your favourite subject? ");
  if (answer == "computer science"):
    print("Correct");
  else
    print("Incorrect, try again");
  endif
endwhile
```

For the purposes of this documentation, pseudocode is highlighted with JavaScript syntax highlighting.

### Flowcharts

See [2.8 Flowcharts](FLOWCHARTS.md).

## References

### Sections
 - [2.1.1 Computational thinking](https://www.bbc.co.uk/bitesize/guides/z4rbcj6/revision/1)
 - [2.1.2 Evaluating common search algorithms](https://www.bbc.co.uk/bitesize/guides/zjdkw6f/revision/2)
 - [2.1.3 Evaluating common sorting algorithms](https://www.bbc.co.uk/bitesize/guides/zjdkw6f/revision/4)
 - [2.1.4 The production of algorithms](https://www.bbc.co.uk/bitesize/guides/z6m7xfr/revision/1)
