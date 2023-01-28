#Lab Report 2 (Part 1)

#Lab Report 2 (Part 2)

##Debugging
I will be testing and identifying the bugs from the method reverseInPlace method in ArrayExamples.java
For this method, the failure inducing input I used was:
```
@Test
public void testReverseInPlace2() {
  int[] input1 = { 1, 2, 3 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
}
```

And for an input that doesn't induce a failure, I used:
```
@Test
```
