# WEEK 3 LAB REPORT
### PART 1

 
### PART 2
For the *ArrayExamples.java* I created a test for the *reversed(int[] arr)* method.
<pre><code>
  @Test
  public void ttest() {
    int[] input1 = { 0, 0, 1 };
    assertArrayEquals(new int[]{ 1, 0, 0 }, ArrayExamples.reversed(input1));
 </code></pre>
 
Here is the output I got from the test and we can see that the mthod is not reversing the array.
<pre><code>
PS C:\Users\ghida\OneDrive\Documents\GitHub\lab3> javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java
PS C:\Users\ghida\OneDrive\Documents\GitHub\lab3> java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ArrayTests
JUnit version 4.13.2
..E.
Time: 0.007
There was 1 failure:
1) ttest(ArrayTests)
arrays first differed at element [0]; expected:<1> but was:<0>       
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)     
        at org.junit.Assert.assertArrayEquals(Assert.java:418)       
        at org.junit.Assert.assertArrayEquals(Assert.java:429)       
        at ArrayTests.ttest(ArrayTests.java:22)
        ... 32 trimmed
Caused by: java.lang.AssertionError: expected:<1> but was:<0>        
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
qual(ExactComparisonCriteria.java:8)
        at org.junit.internal.ComparisonCriteria.arrayEquals(Comparis        ... 38 more

FAILURES!!!
Tests run: 3,  Failures: 1
 </code></pre>

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
