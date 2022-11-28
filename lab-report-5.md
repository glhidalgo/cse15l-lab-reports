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
