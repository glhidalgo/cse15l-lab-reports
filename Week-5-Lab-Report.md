# LAB REPORT 3
## Less command
### Adding line numbers when opening file
To add number lines when opening the contents ofa file using the less command us the -N option
<pre><code> less -N [file] </code></pre>
![image](https://user-images.githubusercontent.com/114626503/199123389-2a78ff91-54bc-43fe-9f52-339f3b7acfe8.png)


###

###


## Find command
### Finding files created/modified before a file
Use the -newer option to find a file created/modified before the file you choose:

<pre><code> find -newer [file] </code></pre>

![image](https://user-images.githubusercontent.com/114626503/199087244-e8b99b44-8127-49da-b19a-d23ebdbc5205.png)
### Find a file by name
use the -name option to search for a file by name:

<pre><code> find -name [file] </code></pre>

### Use find to print full directory of file
Using -name will print the directory from the directory you are finding from so to get the full directory use "~+" as the search directory:
<pre><code> ~+ -name [file] </code></pre>

![image](https://user-images.githubusercontent.com/114626503/199096927-8299661c-f656-4621-9b86-0946d02e9d4c.png)


## Grep command
### Counting the text
When you want to find just the count of the text in a file, use the -c option:
<pre><code> grep -c [text] [file] </code></pre>
![image](https://user-images.githubusercontent.com/114626503/199080094-b7271d57-a065-4f67-8f20-d9dacce303ff.png)                                                  
As you can see in the first command we ask it to find "how" and it shows us the three parts but when we use the -c we get a clean count.

### Searching through all files in a directory
When you want to search all files in a directory at once, instead of typing out all the file names you can just type * at the end:
<pre><code> grep [text] * </code></pre>
![image](https://user-images.githubusercontent.com/114626503/199082226-a8b118a2-5706-44ce-88a5-59e515fab617.png)

Here it gives us the file name and where the text is found. If you only need to know just the files that contain the text you can just use the -l option to make things cleaner:

![image](https://user-images.githubusercontent.com/114626503/199082513-31a54fd4-0aca-450f-aa50-2f9d4e81017f.png)
### Searching for a specific word
In the first image for Searching through all files in a directory most of the words dont completely match the text that we searched, this is because grep only searches for the exact characters we chose throughout the files. We can search for specific words by using the -w option:

<pre><code> grep -w [text] [file] </code></pre>

![image](https://user-images.githubusercontent.com/114626503/199083718-e0c2093b-33d7-412d-92b7-f7e747ec931e.png)

