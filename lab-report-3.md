# Lab Report 3

For this lab report, I will be finding and showcasing some command-line options for the ```grep``` command in bash, and it will be used on the ```./written_2``` data repository.

## Command-Line Options for ```grep```

For this lab report I will be showing the following command-line options:

* ```grep -i //Makes the string or pattern case-insensitive```
* ```grep -c //Shows only the count the lines with the string or pattern```
* ```grep -r //Recursivly search for the string or pattern in all the subdirectories of the current directory```
* ```grep -n //Shows the line number of the string or pattern within the file```

I learned about these commands on [this website](https://man7.org/linux/man-pages/man1/grep.1.html)

## Commands In Use

```grep -i```:
This command-line option is useful for situations where you want to search for a string or pattern and don't know or care about whether there are any capital letters.

```
$ grep -i "lucayans" skill-demo1-data/written_2/*/*/*.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```
$ grep "count floris" -i  skill-demo1-data/written_2/*/*/*.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Amsterdam-History.txt:In 1275 the settlement of Amstelredamme, as it was known, received permission from Count Floris of Holland to transport goods along the river Amstel without incurring tolls, giving the city a monopoly on trade along the river. In 1323 Amstelredamme became a toll-free port for beer, and once a method of preserving herring had been perfected in the late 14th century, the town also had a product with a high profit margin and began exporting fish around Europe.
```


```grep -c```
This command-line option is useful when you want to see which files have a string or pattern and how many times it is used. It also presents that information without printing the contents of the files, making it much easier and faster to see the information compared to a normal ```grep```.

```
$ grep "Talia" -c  skill-demo1-data/written_2/non-fiction/OUP/Berk/*.txt
skill-demo1-data/written_2/non-fiction/OUP/Berk/ch1.txt:2
skill-demo1-data/written_2/non-fiction/OUP/Berk/ch2.txt:3
skill-demo1-data/written_2/non-fiction/OUP/Berk/CH4.txt:0
skill-demo1-data/written_2/non-fiction/OUP/Berk/ch7.txt:0
```

```
$ grep "Lincoln" -c skill-demo1-data/written_2/non-fiction/OUP/Fletcher/*.txt
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch1.txt:10
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch10.txt:1
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch2.txt:41
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch5.txt:11
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch6.txt:12
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch9.txt:2
```

```grep -r```
This command-line option is useful for situations where you want to search for all the files within a directory, but don't want to constantly type out the path of the file. This makes searching for a string or pattern within a directory much faster than typing out a full path.

```
$ grep "Lucayans" -r
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```
$ grep "Butchers" -r
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch6.txt:New Orleans Butchers
```

```grep -n```
This command-line option is useful for finding the exact location of a string or pattern within a file by showing you the line number of that string.

```
$ grep "Nationhood" -n skill-demo1-data/written_2/non-fiction/OUP/*/*.txt
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch6.txt:48:Nationhood and Citizenship
skill-demo1-data/written_2/non-fiction/OUP/Fletcher/ch6.txt:53:Nationhood rings of romance. It appeals not to the analytic mind but to the sentimental heart. As between thought and emotion, lawyers have a bias for the linear creations of mind. The appeals of nationhood are left to poets. Lawyers opt for its analytic counterpart: citizenship. As used in the Fourteenth Amendment, citizenship is a purely formal idea, dependent solely on one’s place of birth. In the debates about the rights of New Orleans butchers before the Supreme Court, the notion of citizenship and its privileges became the stakeholder for any residual yearnings to express the rights of the nation.
```

```
$ grep "Ihilani" -n skill-demo1-data/written_2/*/*/*.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HandRHawaii.txt:34:        Ihilani Resort & Spa $$$$ Ka Olina Resort & Marina,
skill-demo1-data/written_2/travel_guides/berlitz1/HandRHawaii.txt:37:        on the west side of Oahu, expertly managed by JW Marriott, Ihilani is
```


