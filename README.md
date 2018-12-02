# I am a Hacker
s4Lab - I am a hacker

1. I have summarized two papers. You can find the summaries in [summaries/](https://github.com/Javad-Alipanah/i-am-a-hacker/tree/master/summaries)

2. For the *1'st* question about git exposure by websites I have recorded a video which you can find in [videos/](https://github.com/Javad-Alipanah/i-am-a-hacker/tree/master/videos).  
I simply showed how to use directory listing along with git exposure to recover all website's source code.  
Although there is another situation where the directory listing is not enabled and you should be familiar with how a versioning system (here git) works. Briefly, also in this situation you can recover all source code through a recursive approach.

3. For *2'nd* question about duplicates finding my solution is:  
First we find the maximum file size through a simple iteration over all files; this maximum is represented by M.  
We know that counting sort algorithm is of O(N + K) processing order where N is number of instances and K is the range over which they are distributed. Here we have N = 2\*\*48 and K = M + 1 (0-M)  
We can assume that N >> K and that's a good assumption because 2\*\*48 in terms of size (in bytes) is equal to 256 Terabytes.  
Therefore we can sort the sizes associated with files using counting sort algorithm with O(N) processing order and O(M) memory order. The order of memory used is equal to maximum memory order of our files.  
Now we can iterate over the array of sorted sizes and compare the files which have the same size and discover duplicates.

4. With radare2 if you want to dump only binary file open the binary using  
```r2 helloworld```  
then run ```px```
If you want to disassemble instructions then instead of the ```px``` run ```pd```
And finally if you want radare to analyse code (function calls, flags, constraint types analysis, and etc) run  
```r2 -AA helloworld```
and then:  
```pdf```
