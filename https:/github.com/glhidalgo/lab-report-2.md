# LAB REPORT 2
### PART 1
Simplest search engine code:
<pre><code>import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handlerr implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    ArrayList<String> searches = new ArrayList<String>(10);

    public String handleRequest(URI url) {
        int userNum = 0;
        if (url.getPath().equals("/")) {
            userNum++;
            return String.format("Welcome to our search engine! You are our ", userNum, "th user!");
        } 
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("search")) {
                    int indexOfSearch = 0;
                    int isInList = 0;
                    for (int i = 0; i > searches.size(); i++) {
                        if (searches.get(i) == parameters[1]){
                            isInList++;
                            indexOfSearch = i;
                        }
                    }
                    if (isInList > 0) {
                        return String.format("What you are trying to search has already been searched: ", searches.get(indexOfSearch));
                    }
                    else {
                        searches.add(parameters[1]);
                        return String.format( "Your search has been added to our engine: ", parameters[1]);
                    }
                }
            }
            return "404 Not Found!";
        }
    }
}

class SearchEngine {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}</code></pre>

***Did not finish.***
 
### PART 2
For the *ArrayExamples.java* I created a test for the *reversed(int[] arr)* method.
<pre><code>  @Test
  public void ttest() {
    int[] input1 = { 0, 0, 1 };
    assertArrayEquals(new int[]{ 1, 0, 0 }, ArrayExamples.reversed(input1)); </code></pre>
 
Here is the output I got from the test and we can see that the mthod is not reversing the array.
<pre><code>PS C:\Users\ghida\OneDrive\Documents\GitHub\lab3> javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java
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
Tests run: 3,  Failures: 1 </code></pre>

I saw that in the mothd that the mthod wass not returning the *newArray* that we created and was instead returning the input array (*arr*).
I also noticed that the mthod was not actually reversing the elements into the *newArray* and I had to switch *arr* and *newArray* on the fourth line of the method.
<pre><code>  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }</code></pre>
