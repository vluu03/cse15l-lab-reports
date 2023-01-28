# Lab Report 2 (Part 1)
Here is the code I used to make my webserver:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069037329555128432/image.png)

Here is the webserver in action:
First Use:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069038114594631780/image.png)

Second Use:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069038233368936499/image.png)

# Lab Report 2 (Part 2)

## Debugging
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
int[] input1 = { 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input1);
```
Here is the result of running the JUnit tests:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1068818968774721566/image.png)

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1068293992078381116/image.png)

```
//Before change
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  
//After change
static void reverseInPlace(int[] arr) {
    int[] copyArray = new int[arr.length];
    for (int i = 0; i < arr.length; i++) {
      copyArray[i] = arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = copyArray[arr.length - i - 1];
    }
  }
```
This change addresses the issue because arr now gets assigned the values of a copy of the array
which means that the changed values of arr won't be included when taking the elements in reverse order.
