# Year When Max People Were Alive - Max Interval Overlap Problem

Find the year when maximum number of people we alive.
 You are given two arrays, array containing born years and array containing death years.
 You need to return the year when maximum number of people were alive.
```
 e.g
 born = {2000, 1975, 1975, 1803, 1750, 1840, 1803, 1894}
 death ={2010, 2005, 2003, 1809, 1869, 1935, 1921, 1921}

 returns: 1803
```
 explanation:
 sort both born and death arrays:
 ```
 born = {1750, 1803, 1803, 1840, 1894, 1975, 1975, 2000};
 death= {1809, 1869, 1921, 1921, 1935, 2003, 2005, 2010};
```
 - initialize peopleAlive counter with 1.
 - initialize i and j with 0. i will used to traverse born array and j will be used to traverse death array.
 - Start incrementing the peopleAlive counter, on every increment check if maxPeople alive is less than peopleAlive
 then update maxPeopleAlive and year when maxPeople were alive.
 - Keep incrementing the counter until a value of year is found in sorted born array on ith value which is greater than
   jth value in death array.
 - At this point peopleAlive and increment j counter.
 - In the end return year.
```
 Year                Counter
 1750   --born-->       1
 1803   --born-->       2
 1803   --born-->       3
 1840   --died-->       2
 1840   --born-->       3
 1894   --died-->       2
 1894   --born-->       3
 1975   --died-->       2
 1975   --died-->       1
 1975   --died-->       0
 1975   --born-->       1
 1975   --born-->       2
 2000   --born-->       3

 returns 1803
```
