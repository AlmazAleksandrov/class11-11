### Task 6kyu:

The Pell sequence is the sequence of integers defined by the initial values.
Your task is to write a method that returns nth Pell number

[Task link](https://www.codewars.com/kata/5818d00a559ff57a2f000082/train/java)

#### Solution:
```
import java.math.BigInteger;

public class Solution {
public static BigInteger pell(int n) {

  BigInteger p0 = BigInteger.valueOf(0);
  BigInteger p1 = BigInteger.valueOf(1);
  BigInteger pn = BigInteger.valueOf(0);

  if (n==0){return BigInteger.valueOf(0);}
  if (n==1){return BigInteger.valueOf(1);}

      for(int i = 2; i <= n; i++){
      pn = p1.multiply(BigInteger.valueOf(2));
      pn = pn.add(p0);
      p0 = p1;
      p1 = pn;
    }

  return pn;

  }
}
```

#### Fav solution:
```
import java.math.BigInteger;

public class Solution {
  public static BigInteger pell(int n) {
    BigInteger a = BigInteger.ZERO, b = BigInteger.ONE;
    for (int i = 0; i < n; i++) {
      BigInteger c = b.shiftLeft(1).add(a);
      a = b;
      b = c;
    }
    return a;
  }
}
```

#### Comment:
More optimal code, cost one cycle.


### Task 8kyu:

We need a function that can transform a string into a number.

[Task link](https://www.codewars.com/kata/544675c6f971f7399a000e79/train/java)

#### Solution:
```
public class StringToNumber {
    public static int stringToNumber(String str) {
        int number = Integer.parseInt(str);
        return number;
    }
}
```

#### Fav solution:
```
public class StringToNumber {
    public static int stringToNumber(String str) {
        int number = Integer.parseInt(str);
        return number;
    }
}
```

#### Comment:
I like my solution, others are not impressed.
