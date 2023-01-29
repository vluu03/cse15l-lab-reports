# Lab Report 2 (Part 1)
Here is the code I used to make my webserver:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069037329555128432/image.png)

Here is the webserver in action:

First Use:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069038114594631780/image.png)

For this use, the called methods are:
```
//Checks if "/add-message" is in the path of the url
url.getPath().contains("/add-message");
//Separtes the query in the url using "="
url.getQuery().split("=");
//Checks if there is an "s" located before the "=" in the url
parameter[0].equals("s");
//Adds the string put in after "=" and stores it in an ArrayList called stringList
stringList.add(string_num,parameters[1]);
//Joins together the elements in the ArrayList as strings and adds a new line after every //element
String.join("\n",stringList);
```
The arguments in these methods are:
* url (URL of the webserver)
* "/add-message" (string of path)
* "=" (part of query)
* "s" (part of query)
* string_num (keeps track of index of stringList)
* parameters[1] (string that gets added to stringList)
* "\n" (Delimiter to put a new line between each string)
* stringList (ArrayList of strings from the query)

From this first use, the stringList gets changed by adding the string from the query "Penguins" and string_num gets incremented. The rest of the values stay the same because they are fixed parts of the url for this request.

Second Use:

![Image](https://cdn.discordapp.com/attachments/1063006870299758622/1069038233368936499/image.png)

For this second use, similar methods were called:
```
//Checks if "/add-message" is in the path of the url
url.getPath().contains("/add-message");
//Separtes the query in the url using "="
url.getQuery().split("=");
//Checks if there is an "s" located before the "=" in the url
parameter[0].equals("s");
//Adds the string put in after "=" and stores it in an ArrayList called stringList
stringList.add(string_num,parameters[1]);
//Joins together the elements in the ArrayList as strings and adds a new line after every //element
String.join("\n",stringList);
```
And similarly, the arguments in these methods are:
* url (URL of the webserver)
* "/add-message" (string of path)
* "=" (part of query)
* "s" (part of query)
* string_num (keeps track of index of stringList)
* parameters[1] (string that gets added to stringList)
* "\n" (Delimiter to put a new line between each string)
* stringList (ArrayList of strings from the query)

In this second run of the request, stringList is changed again to add "are_cool" to the 2nd index and string_num gets incremented again. And like before, the rest of the arguments remain the same for this request.

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
This change addresses the issue because ```arr``` now gets assigned the values of a copy of the array
which means that the changed values of ```arr``` won't be included when taking the elements in reverse order. The reason ```int[] input1 = { 3 }; ``` 
did not cause a fail in the test is because there is only one elements which means that it is essentially assigning ```arr[0] = arr[0]; ``` 
which would end up passing the test since the reverse of an array with one element is the same array.

# Lab Report 2 (Part 3)

I learned a lot of new things from lab, specfically from lab 2. For example, I learned about the structure of URL's and the code that goes behind these URLs. I also learned about how the path affects where the user goes within the website and how query of the URL can alter the website in many different ways. In lab 3, I learned more about how debugging works, and how simply passing a methed test doesn't mean that it behaves as intended.
