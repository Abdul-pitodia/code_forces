

Petya and Vasya are playing a game. Petya's got n non-transparent glasses, standing in a row. The glasses' positions are indexed with integers from 1 to n from left to right. Note that the positions are indexed but the glasses are not.

First Petya puts a marble under the glass in position s. Then he performs some (possibly zero) shuffling operations. One shuffling operation means moving the glass from the first position to position p 1, the glass from the second position to position p 2 and so on. That is, a glass goes from position i to position p i. Consider all glasses are moving simultaneously during one shuffling operation. When the glasses are shuffled, the marble doesn't travel from one glass to another: it moves together with the glass it was initially been put in.

After all shuffling operations Petya shows Vasya that the ball has moved to position t. Vasya's task is to say what minimum number of shuffling operations Petya has performed or determine that Petya has made a mistake and the marble could not have got from position s to position t.
Input

The first line contains three integers: n, s, t (1 ≤ n ≤ 105; 1 ≤ s, t ≤ n) — the number of glasses, the ball's initial and final position. The second line contains n space-separated integers: p 1, p 2, ..., p n (1 ≤ p i ≤ n) — the shuffling operation parameters. It is guaranteed that all p i's are distinct.

Note that s can equal t.
Output

If the marble can move from position s to position t, then print on a single line a non-negative integer — the minimum number of shuffling operations, needed to get the marble to position t. If it is impossible, print number -1.
Examples

Input
4 2 1
2 3 4 1

Output
3

Input
4 3 3
4 1 3 2

Output
0

Input
4 3 4
1 2 3 4

Output
-1

Input
3 1 3
2 1 3

Output
-1



```
enter = input().split()
n = int(enter[0]) - 1
s = int(enter[1]) - 1 
t = int(enter[2]) - 1
fix = s
arr_b = [int(i) - 1 for i in input().split()]
arr_a = [i for i in range(1,n+2)]
target = arr_a[s]
flag = 0
#print(arr_a)
#print(arr_b)


i = 0
while (arr_a[t] != target):
  
  correct_pos = arr_b[s] 
  arr_a[correct_pos],arr_a[s] = arr_a[s],arr_a[correct_pos]
  s = correct_pos
  i = i + 1
  if (target == arr_a[fix]):
    flag = 1
    break
#print(arr_a)
if (flag==0):
  print(i)
else:
  print(-1)
  
  
```


