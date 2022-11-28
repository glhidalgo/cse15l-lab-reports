# LAB REPORT 5 #
## Code ##
<pre><code> CPATH=.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar
set -e

rm -rf student-submission
git clone $1 student-submission

FILE=student-submission/ListExamples.java


if [[ -f "$FILE" ]]; then 
    echo "$FILE does exist."
    cp student-submission/ListExamples.java ListExample.java
    javac -cp $CPATH *.java
    if [[ $CPATH -eq 0 ]]; then
        echo "compiled successfully!"
    else
        echo "compiled unsuccessfully!"
        exit
    fi
else
    echo "$FILE does not exist."
    echo "Score: 0"
    exit
fi</code></pre>

## Examples ##

![image](https://user-images.githubusercontent.com/114626503/204302860-20296453-e37b-4849-8555-9b4868b13ef0.png)

In this example the code clones the repository checks to see if the ListExamples.java file exists, in this case it does not so the script tells the user that does not exist and gives the submission a score of 0.
