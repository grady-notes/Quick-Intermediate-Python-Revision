# Multithreading

Multithreading in programming, means that the program is able to carry out multiple tasks simultaneously. Multithreading is a very powerful feature of Python. It comes into pitch when you have a large number of tasks to carry out and you want to be able to do them all at the same time. This is done when the number of tasks is greater than the number of cores on your computer. In short, whenever the CPU is left idle, it will be used to carry out other tasks. Multithreading can be achieved by using the `threading` module.

A direct consequence of multithreading is that the program will be able to run faster. This is because the program will be able to carry out multiple tasks at the same time.

A direct comparision of normal execution and multithreaded execution is shown below

The program will be taking an array as an input to two different functions. The program will call the functions two times, first time noramlly, and the second time, the program will be multithreaded. The time taken by the program to execute the two functions will be different.

```python
import time
import threading

def foo() :
    def square (arr):
        print("Calculating squares")
        for i in arr :
            time.sleep(0.2)
            i ** 2
    def cube (arr):
        print("Calculating cubes")
        for i in arr :
            time.sleep(0.2)
            i ** 3

    arr = [1,2,3,4]

    def normal() :
        print("Normal Execution")
        total = time.time()
        square(arr)
        cube(arr)
        print("Time taken in normal execution : ", time.time() - total)
    def multi() :
        print("\nMultithreaded Execution")
        total = time.time()
        t1 = threading.Thread(target=square, args=(arr,))
        t2 = threading.Thread(target=cube, args=(arr,))
        t1.start()
        t2.start()
        t1.join()
        t2.join()
        print("Time taken in multithreaded execution : ", time.time() - total)

    normal()
    multi()

foo()
```

Notice how the time taken by the program to execute the two functions is different. This is because the program is multithreaded.
