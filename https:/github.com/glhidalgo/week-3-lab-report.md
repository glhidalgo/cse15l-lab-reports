## PART 1
 
## PART 2
For the *ArrayExamples.java* I created a test for the *reversed(int[] arr)* method.

![image](https://user-images.githubusercontent.com/114626503/195946824-9e537e35-1e16-4f56-8450-949ee7cb48b7.png)

Here is the output I got from the test and we can see that the mthod is not reversing the array.

![image](https://user-images.githubusercontent.com/114626503/195946539-6cf73d9d-06c6-4c4d-abe8-5a1ca004ae09.png)

I saw that in the mothd that the mthod wass not returning the *newArray* that we created and was instead returning the input array (*arr*).
I also noticed that the mthod was not actually reversing the elements into the *newArray* and I had to switch *arr* and *newArray* on the fourth line of the method.
<pre><code>
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
 </code></pre>
