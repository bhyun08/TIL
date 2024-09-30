Time Complexity is a measure of an algorithm's performance, which indicates how long it takes an algorithm to run, depending on its input size (e.g., the number of data). It is mainly expressed as `Big-O notation`, which indicates how many computational steps the algorithm goes through. Another measure of an algorithm's performance way are `Big-Omega`, `Big-Theta` etc.
# Big-O notation
The Big-O notation is a notation used to measure the performance of an algorithm, It is a mathematical representation of how the worst-case run time increases with the size of the input data. 

Big-O notation is the simple way that show how many operate algorithm when is increased input data(`n`)'s size. In Big-O notation, Constant and low orders are ignored because higher orders have the greatest impact on performance. For example, `5n^2 + 3n + 2` is represented by `O(n^2)` in the Big-O notation.
## Representative Big-O notations
![](https://miro.medium.com/v2/resize:fit:1024/1*WXfVqSBSsQBLKnPMM4rRKA.png)
1. **O(1)** - An algorithm that always takes the same amount of time regardless of the input size.
2. **O(log n)** - An algorithm which execution time increases slowly as the input size increases.
3. **O(n)** - An algorithm which execution time increases as the input size increases.
4. **O(n log n)** - The method of processing `n` entries in each step for the input size `n` and repeating them `log n` times.
5. **O(n^2)** - Time proportional to the square of the input size. Mostly in algorithms using double loops.

---
Reference link 🙂     
https://en.wikipedia.org/wiki/Time_complexity          
https://medium.com/@verdi/understanding-big-o-notation-for-the-newbie-dev-720c6f3446fd

Reference Book 📕
**C로 배우는 쉬운 자료구조(Easy data structure to learn with C) - 이지영**