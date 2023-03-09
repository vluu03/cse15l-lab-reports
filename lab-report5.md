# Lab Report 5

For this lab report, I will be looking at Lab Report 3 again and this time, instead of exploring the different
options of the ```grep``` command, like I did last time, I will exploring the options for the ```find```
command. I will also be showcasing these different options on the ```/written_2``` data repository in bash

## Command-Line Options for ```find```

For this lab report, I will be shwoing the following command-line options:
* ```find -type``` //Finds files or directories of a specified type
* ```find -exec``` //Allows you to execute a command on a file or directory
* ```find -maxdepth``` //Lets you search a directory with a certain amount of depth
* ```find -and``` //Allows you to impose multiple conditions on the find command

I learned about all these commands on [this website](https://ss64.com/bash/find.html). To find this website I just
searched up "find command line options" in google and chose the top option


## Commands In Use

```find -type```: This command-line options is useful for cases in which you want to only find directories or files, in case there are directories and files that share names

I found this command [here](https://ss64.com/bash/find.html)

```
$ find . -type d
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

```
$ find . -type f -name "ch1.txt"
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Fletcher/ch1.txt
./non-fiction/OUP/Kauffman/ch1.txt
./non-fiction/OUP/Rybczynski/ch1.txt
```

```find -exec```: This command-line option is useful for situation where you want to execute a command on a file such as displaying the contents of the file, like what I did below.

I found this command [here](https://ss64.com/bash/find.html)

```
$ find ./travel_guides/berlitz1/ -name "HandRIbiza.txt" -exec cat {} \;

        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
        offfical government rating system.
        As a basic guide, the symbols we use indicate what you can
        expect to pay for a three-course meal for two, excluding wine, tax and
        tip. Drinks will add considerably to the final bill.
        ✪less than 5,000 ptas.
        ✪✪5,000–8,000 ptas.
        ✪✪✪more than 8,000 ptas.
```

```
$ find ./non-fiction/OUP/Abernathy/ -name "*.txt" -exec echo {} \;
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
```

```find -maxdepth```: This command-line option is useful for searching deeply within a directory and its subdirectories without having to know the exact paths.

I found this command [here](https://ss64.com/bash/find.html)

```
$ find . -maxdepth 4 -name "ch1.txt"
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Fletcher/ch1.txt
./non-fiction/OUP/Kauffman/ch1.txt
./non-fiction/OUP/Rybczynski/ch1.txt
```

```
$ find . -maxdepth 2 -name "travel_guides"
./travel_guides
```

```find -and```: This command-line option is useful for cases where you want to search for files that fufill mutiple conditions such as its name or depth.

I found this command [here](https://ss64.com/bash/find.html)

```
$ find ./non-fiction/OUP/Berk/ -maxdepth 4 -name "*.txt" -and  -name "ch1.txt"
./non-fiction/OUP/Berk/ch1.txt
```

```
$ find . -maxdepth 4 -name "Berk" -and -type d
./non-fiction/OUP/Berk
```

