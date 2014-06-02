First of all, here is a [book](http://eloquentjavascript.net/).

Secondly, here is program that adds the numbers one through ten and prints them out, written a few different ways.

```
00110001 00000000 00000000
00110001 00000001 00000001
00110011 00000001 00000010
01010001 00001011 00000010
00100010 00000010 00001000
01000011 00000001 00000000
01000001 00000001 00000001
00010000 00000010 00000000
01100010 00000000 00000000
```

```
1. Store the number 0 in memory location 0
2. Store the number 1 in memory location 1
3. Store the value of memory location 1 in memory location 2
4. Decrement the value in memory location 2 by the number 11
5. If the value in memory location 2 is the number 0, continue with instruction 9
6. Increment the value in memory location 0 by the value in memory location 1
7. Increment the value in memory location 1 by the number 1
8. Continue with instruction 3
9. Output the value of memory location 0
```

```
 Set 'total' to 0
 Set 'count' to 1
[loop]
 Set 'compare' to 'count'
 Subtract 11 from 'compare'
 If 'compare' is zero, continue at [end]
 Add 'count' to 'total'
 Add 1 to 'count'
 Continue at [loop]
[end]
 Output 'total'
```

```javascript
var total = 0, count = 1;
while (count <= 10) {
  total += count;
  count += 1;
}
print(total);
```

```javascript
print(sum(range(1, 10)));
```