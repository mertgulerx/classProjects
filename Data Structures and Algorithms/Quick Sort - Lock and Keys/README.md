# Lock and Keys

## ReflectionSort (Custom QuickSort)

Reflection Sort matchs uniquely sized keys and locks using the QuickSort algorithm.
Example data:

Keys: 1 6 4 3 5

Locks: 5 3 6 1 4

The main rule is that you cannot compare keys with keys or locks with locks. You must use a key to sort locks and a lock to sort keys

The pivot key is selected randomly.

### Pseudo Code: 

```pseudo
FUNCTION reflectionSort(keys, locks, low, high)
IF (low >= high) THEN
    RETURN
END IF
key = selectRandom(keys, low, high)
pivotIndex = divide(locks, low, high, key)
lock = locks[pivotIndex]
divide(keys, low, high, lock)
reflectionSort(keys, locks, low, pivotIndex - 1)
reflectionSort(keys, locks, pivotIndex + 1, high)
END FUNCTION
```

```
FUNCTION divide(array, low, high, pivot)
i = low - 1
FOR j = low TO high - 1 DO
    IF array[j] = pivot THEN
        swap(array[j], array[high])
    END IF
    IF array[j] < pivot THEN
        i = i + 1
        IF i != j THEN
            swap(array[i], array[j])
        END IF
    END IF
END FOR
IF i + 1 != high THEN
    swap(array[i + 1], array[high])
END IF
RETURN i + 1
END FUNCTION
```

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide1.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide2.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide3.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide4.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide5.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide6.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide7.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide8.SVG" width="80%">

<img src="https://github.com/mertgulerx/classProjects/blob/main/Data%20Structures%20and%20Algorithms/Quick%20Sort%20-%20Lock%20and%20Keys/images/Slide9.SVG" width="80%">

