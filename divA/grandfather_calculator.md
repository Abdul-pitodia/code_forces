https://codeforces.com/problemset/problem/620/B

```
digit_dict = {
    0:6,
    1:2,
    2:5,
    3:5,
    4:4,
    5:5,
    6:6,
    7:3,
    8:7,
    9:6
}

rng = input().split()


    rng_lst = [str(i) for i in range(int(rng[0]),int(rng[1])+1)]
    s = ''.join(rng_lst)
    sum_lst = []
    for alp in s:
        if int(alp) in digit_dict.keys():
            sum_lst.append(digit_dict[int(alp)])
    print(sum(sum_lst))


```



