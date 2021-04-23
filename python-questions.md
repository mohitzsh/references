- ```ENUM``` class in python:
  - ```
    from enum import Enum
    
    class A(Enum):
      AA = 1
      AB = 2
      AC = 3
     
    list(A) -> [<A.AA: 1>, <A.AB: 2>, <A.AC: 3>]
    
    for x in A:
      print(x)
    
    # A.AA
    # A.AB
    # A.AC
    ```
    See what's the difference between using ```A``` inside ```list()``` and ```A``` within a loop.
