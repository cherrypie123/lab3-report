## Part 2
Failure inducing input
![image](https://user-images.githubusercontent.com/114331111/195963695-2ff18788-b6cb-47e4-a1a7-df5a9385c41f.png)

Symptom:
![image](https://user-images.githubusercontent.com/114331111/195963711-0e88c71f-8920-4b33-b6d2-f386bb915ab6.png)

The bug
![image](https://user-images.githubusercontent.com/114331111/195963812-00c4d44d-902a-4e07-92f9-a504473c0cf5.png)

Connection between symptom and bug. Basically the bug reverses everything from the array but the last element, so the last array will be the first element of the new inversed array. So the error says that the code returns {3,2,3} instead of {3,2,1}



In ListExamples.java, the filter method has a bug
if input is List<String> a = [true, false, false, true], it will only returns [true] instead of [true, true]

The problem is that the code keeps on updating the result in index 0 instead of adding the another right result to the new arraylist. 
```
static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(0, s);
      }
    }
    return result;
  }
```

