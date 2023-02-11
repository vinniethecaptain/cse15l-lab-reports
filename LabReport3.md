# Lab Report 3 #
## Using grep ##

### grep -r ###
Using the -r option allows the terminal to recursively search through all directories for text files that contain the specified pattern.
(Source: grep --help)

``` 
$ grep -r "Lucayans" written_2/
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and 
the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```
$ grep -r "pseudo-scientific" written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz1/IntroEgypt.txt:        fantasies. Today, “pseudo-scientific” theories about the origin and
```

### grep -c ###

Using the -c option allows the terminal return the number of times a certain specified pattern appears in a text file.
(Source: grep --help and ChatGPT)

```
$ grep -c "Lucayans" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Algarve-History.txt:0
written_2/travel_guides/berlitz2/Algarve-Intro.txt:0
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Amsterdam-History.txt:0
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt:0
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Athens-History.txt:0
written_2/travel_guides/berlitz2/Athens-Intro.txt:0
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bahamas-History.txt:2
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bali-History.txt:0
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Barcelona-History.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Beijing-History.txt:0
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Berlin-History.txt:0
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bermuda-history.txt:0
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Budapest-History.txt:0
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt:0
written_2/travel_guides/berlitz2/California-History.txt:0
written_2/travel_guides/berlitz2/California-WhatToDo.txt:0
written_2/travel_guides/berlitz2/California-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Canada-History.txt:0
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-History.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Cancun-History.txt:0
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:0
written_2/travel_guides/berlitz2/China-History.txt:0
written_2/travel_guides/berlitz2/China-WhatToDo.txt:0
written_2/travel_guides/berlitz2/China-WhereToGo.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Costa-History.txt:0
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Crete-History.txt:0
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt:0
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Cuba-History.txt:0
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Nepal-History.txt:0
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/NewOrleans-History.txt:0
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Poland-History.txt:0
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-History.txt:0
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/PuertoRico-History.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Vallarta-History.txt:0
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:0
```

```
$ grep -c "Kevin" written_2/non-fiction/OUP/Berk/*.txt
written_2/non-fiction/OUP/Berk/ch1.txt:0 
written_2/non-fiction/OUP/Berk/ch2.txt:0 
written_2/non-fiction/OUP/Berk/CH4.txt:14
written_2/non-fiction/OUP/Berk/ch7.txt:0 
```

### grep -n ###
Using the -n option allows the terminal return the specific lines that contain the specified pattern with their corresponding line numbers.
(Source: grep --help)

```
$ grep -n "Bond Stores" written_2/non-fiction/OUP/Abernathy/ch1.txt
5:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.
6:Fifty years later, it is hard to imagine a retailer—be it a high-end department store, mass merchandiser, or catalog service—limiting an individual customer’s clothing purchase. Retailers collect detailed point-of-sales information that reflects the real-time demand for goods by consumers. Through new computer systems, they share this information with suppliers who, in turn, can ship orders within days to automated distribution centers. The contemporary equivalent of 
Bond Stores now has a much better chance of avoiding stock-outs of popular items and the inventory gluts that lead to costly markdowns. By the same token, the overall risk associated with fickle consumers, numerous selling seasons, and segmented markets—along with fierce overseas competition—has currently made this a tough arena for American retailers and manufacturers.
7:The most surprising aspect of this story is that today’s U.S. apparel and textile industries—left for dead by business commentators and economic analysts in the 1980s—have begun to transform themselves, reaping new competitive advantages. Although Bond Stores’ customers were thrilled by a suit with two pairs of pants, contemporary customers want and expect a huge range of choices, and the consumer desire for limitless variety has kept the American apparel industry alive. In 1995, for instance, American consumers purchased 28.7 outerwear garments (all coats, jackets, shirts, dresses, blouses, sweaters, trousers, slacks, and shorts) per capita; in China the estimated number of such garments was only 2 
per capita.2
11:Supply channels are not new, of course; for centuries, fabric-makers have sold their wares to those who cut and sew garments. But, until recently, most channels in the textile and apparel industries have been characterized by arm’s-length relationships among relatively autonomous firms. It is only since the mid-1980s that a number of market and technological changes have encouraged companies to enhance the links among different stages of production and distribution. 
Indeed, retailers like Wal-Mart Stores, Kmart Corporation, and Dillard’s Inc. have been the driving forces behind changes in manufacturing and logistics systems in a way that was unheard of in Bond Stores’ time. For instance, entrepreneur Sam Walton built a retail juggernaut that began with thirty-nine Wal-Mart stores in 1971 and grew to almost three thousand by 1996. He did so by insisting that suppliers implement information technologies for exchanging sales data, adopt standards for product labeling, and use modern methods of material handling that assured customers a variety of products at low prices.
16:When Bond Stores had customers lining up around the block to buy suits, “casual wear,” as we know it today, did not exist. Even in the 1960s, men wore suits, ties, and hats to the ballpark, and women were clothed in dresses and millinery. As recently as 1969, the dress code at Harvard required undergraduate men to wear a collar, necktie, and jacket in the dining halls; women had to wear a dress or a skirt and blouse. It wasn’t until the 1970s that these vestiges of formality gave way to blue jeans and T-shirts—the casual wear uniform. The 1980s ushered in yuppie brands, and in the 1990s history repeated itself as baby boomers’ children adopted the bedraggled grunge look. Many business firms have “casual days” for office attire. Now six out of ten U.S. employers now have casual days in their workplaces, all but a few establishing this practice during the 1990s. About seven out of ten organizations with dress-down days permit employees to wear polo shirts, jeans, and sneakers.4
78:The information-integrated channel, with its emphasis on time and product perishability, is the basis for our cautiously optimistic—and unconventional—outlook. Even more important, the forces examined in this book provide a glimpse into processes reshaping a considerable portion of the economy. Consumers no longer line up for a special suit at a store like Bond Stores; they also expect an ever more “fashionable” array of cereal products, computers, and automobiles. As the next chapter shows, the changes now under way have their roots in new technologies, just as technical advances in transportation and communication shifted the industrial landscape at the end of the last century.
```

```
$ grep -n "el abuelo" written_2/non-fiction/OUP/Castro/chA.txt
6:An old-man figure called el abuelo (the grandfather) played the role of a bogeyman in Hispano folklore. In literature it is sometimes spelled aguelo, and some scholars speculate that it may be a borrowed word from the language of the Pueblo Indians. In Spanish it means “grandfather,” and has become synonymous with coco, cucui, and bogeyman. This folk character is more known in northern New Mexico than in other parts of the Southwest. He appeared at Christmastime to test and discipline children who did not know their catechism or prayers. He was a scary figure, dressed to terrify children with a black cape and a mask with large horns, and always carrying a whip. Children were terribly frightened because of his horrid appearance. Instead of a mask he sometimes had a tortilla plastered on his face, wore buffalo horns and a horsetail, and of course carried the whip. A few days before Christmas, he’d knock on the door of a home, give a bloodcurdling cry, crack his whip, and yell at the children, “Han sido buenos muchachos estos?” (Have these children been good?) The children would cringe and hide while the parents defended them. Then el abuelo would say, “Pues que recén y se acuestén” (Well, let them pray and go to bed). Sometimes he made the children dance Las Palomitas, loosely translated as “the little doves.” Espinosa describes this experience. “After making them pray, he makes them form a circle, 
and, taking each other’s hands, they dance around the room with him, singing,
13:A description of el abuelo making children “dance the little dove” is also available in Steele’s work (1992, 25). Throughout the year if children misbehaved, parents would threaten them, “Si no te sosiegas, llamo el abuelo” (If you don’t behave, I’ll call the bogeyman).
14:El abuelo is also a prominent figure in the dance of Los Matachines, and plays a comical role in which he makes jokes and shouts out instructions to the rest of the dancers. In some performances there is a female character, la abuela, who acts as el abuelo’s accomplice and plays a similar role. Although he is not heard of often in contemporary times, references to el abuelo can be found in the folktales and literature of New Mexico.
```

### grep -i ###
Using the -i option allows the terminal return all the lines that contains the specified pattern while ignoring lowercases and uppercases.
(Source: grep --help)

```
$ grep -i "el abuelo" written_2/non-fiction/OUP/Castro/chA.txt
El Abuelo (Grandfather)
An old-man figure called el abuelo (the grandfather) played the role of a bogeyman in Hispano folklore. In literature it is sometimes spelled aguelo, and some scholars speculate that it may be a borrowed word from the language of the Pueblo Indians. In Spanish it means “grandfather,” and has become synonymous with coco, cucui, and bogeyman. This folk character is more known in northern New Mexico than in other parts of the Southwest. He appeared at Christmastime to test and discipline children who did not know their catechism or prayers. He was a scary figure, dressed to terrify children with a black cape and a mask with large horns, and always carrying a whip. Children were terribly frightened because of his horrid appearance. Instead of a mask he sometimes had a tortilla plastered on his face, wore buffalo horns and a horsetail, and of course carried the whip. A few days before Christmas, he’d knock on the door of a home, give a bloodcurdling cry, crack his whip, and yell at the children, “Han sido buenos muchachos estos?” (Have these children been good?) The children would cringe and hide while the parents defended them. Then el abuelo would say, “Pues que recén y se acuestén” (Well, let them pray and go to bed). Sometimes he made the children dance Las Palomitas, loosely translated as “the little doves.” Espinosa describes this experience. “After making them pray, he makes them form a circle, and, taking each other’s hands, they dance around the room with him, singing,
A description of el abuelo making children “dance the little dove” is also available in Steele’s work (1992, 25). Throughout the year if children misbehaved, parents would threaten them, “Si no te sosiegas, llamo el abuelo” (If you don’t behave, I’ll call the bogeyman).
El abuelo is also a prominent figure in the dance of Los Matachines, and plays a comical role in which he makes jokes and shouts out instructions to the rest of the dancers. In some performances there is a female character, la abuela, who acts as el abuelo’s accomplice and plays a similar role. Although he is not heard of often in contemporary times, references to el abuelo can be found in the folktales and literature of New Mexico.
```

```
$ grep -i "german" written_2/non-fiction/OUP/Fletcher/ch1.txt
I write in this chapter of religious ideas and their value in understanding our legal experience. This, admittedly, is an unusual take in our rigorously secular academic world. The American university world has distanced itself from the 
sensibilities of ordinary Americans who take the Bible seriously as a source of wisdom and who live their lives with devotion to values of faith and redemption. In this interpretation of law as the path to national redemption, I seek to 
find a middle way between Jewish and Christian thinking. There is no doubt that the nations whose struggles I describe—France, Germany, and the United States—think of themselves as Christian nations. Yet, the very idea of redemption of the entire nation through law resonates more with the older tradition of the Jewish national mission under the Torah revealed at Mount Sinai. My account seeks to unite the divergent strains of all religions that trace their roots to the original idea in Exodus of a nation living under God and under law.
The idea that freedom exists only under law is often understood as a Central European or German approach to the individual in society. Americans tend to subscribe rather to the myth of a Lockian state of nature, where individuals exist prior to the organization of society under a social contract. The Declaration of Independence relies heavily on the principle that the “consent of the governed” is indispensable to the legitimacy of government. Yet, in actual American practice, the law—particularly constitutional law—serves the same function of sanctifying the social order as it does in the European experience. Before turning to the details of the American appeal to law after the surrender at Appomattox 
Courthouse in April 1865, let us examine first two significant European efforts to domesticate tendencies toward violence under the rule of law.
France and Germany
Legal cultures, too, must seek to perfect themselves. They cannot exist simply as the product of will. When legal cultures lose sight of their natural end of bringing a reign of justice and harmony to human affairs, they decline into corruption and the arbitrariness of power. The German philosopher Gustav Radbruch defined the ideal of Law as the practice of establishing rules in the pursuit of justice.4 Communal life seeks, through law, to perfect itself. This secular idea parallels the eschatological aim of perfecting the creation of the world under God’s reign.
It is not surprising that when the established authority’s respect for the political opposition is debased, the legal culture invariably suffers. This is most noticeably clear in dictatorial societies where legal debate is reduced to little more than efforts to placate the powers that be. Although the National Socialists purported to rely on legal forms and administrative regularity, their contempt for free and mutually respectful discourse led to a corruption of the legal culture. The Nazis’ conception of law fluctuated between two unpalatable extremes. Sometimes the slogan was that law was what Hitler wanted and commanded (Recht is das, was der Führer will). At other times, utility to the German people was the ultimate source of legitimacy (Recht is das, was dem Volke nutzt).5 The National Socialist Party’s manipulation of these slogans and their observance of legal forms served only to bring the culture to a deeper level of corruption.
It is an extraordinary feature of postwar German culture that a new generation of jurists managed to save, to redeem, their concept of law from its racist and Nazi associations. In the wake of their unforgettable crimes against humanity, the West Germans, too, sought redemption in the rule of law, in the Rechtsstaat that they have cultivated along with economic prosperity. Living by the law, and seeking justice within the law, redeems the humanistic side of German culture. It has suppressed the romantic will to break all restraints for the sake of glory in power.
The Germans, too, have a civil code that has united them, since 1900, through the transitions from Bismarck, to Weimar, to the Third Reich, to the present. Yet, under the National Socialists, the code, which contains the provisions on family law, became tainted with notions of racial purity. Jews and Aryans could not marry. Of course, this stain disappeared in the postwar reform, but the memory remains of a corrupted civil code. Not surprisingly, then, Germans have sought redemption by promoting both a new constitution, enacted in 1949, and the rule of law in a united Europe. More than any country seeking redemption under law, the Germans identified their new constitution, the Grundgesetz, as the focal point of state authority. The sanctity of the constitution—and not the personal head of state—became the interest protected under the reformed law of treason. When West Germans felt their infant postwar republic endangered by Communist 
subversion, they appointed an agency to protect the integrity of the government. The announced aim of the agency was to protect the constitution (Verfassungsschutz).
The preamble of this charter, called the Basic Law (Grundgesetz), repeatedly reminds Germans of the imperative to atone for the sins of the past:
Conscious of its responsibility before God and humanity, possessed of the will to serve the peace of the world as an equal member of a United Europe, the German nation [Volk] commits itself, by virtue of its inherent constitution-making 
authority, to the following Basic Law.6
No other constitution, so far as I know, stresses its sense of “responsibility” and declares as one of its primary purposes “to serve the peace of the world.” These gestures recall the descent of the German nation into the evils of aggressive war and crimes against humanity.
The first article of the Basic Law invokes the humanistic Kantian underpinnings of German culture: “Human dignity is inviolable. All state power is obligated to protect it and respect it.” This provision provides the backdrop for interpreting all the basic rights guaranteed under the constitution. The protection of human dignity is the fundamental value suffusing the entire legal order. The highest virtue of the postwar German constitutional order, then, was precisely the greatest casualty of the Nazi regime. The path to redemption lay in reclaiming the liberal and humanistic values most systematically violated in their darkest hour. The point is carried forward in the second article: “Everyone has the right to flourishing of his or her personality. . . . Everyone has the right to life.”
These are provisions that enabled Germans to redefine their identities. They would no longer be the people devoted to the Volk above all. They would become the nation of human dignity that served the cause of human flourishing and the sanctity of human life. For the postwar Germans, then, the law, and particularly the Basic Law became the means for suppressing evil impulses and returning to the promises of an earlier national self. This is what redemption means in a secular legal world.
The redemptive impulse leads national courts to place an emphasis on values that resonate against past sins. The German Constitutional Court has made a number of controversial decisions that make sense primarily as efforts to resolve the burden of memory. The court decided to uphold a law abolishing the twenty-year statute of limitations for concentration camp murders.7 It invoked the constitutional “right to life” to strike down a liberal abortion law that permitted abortion on demand in the first trimester.8 And, more recently, the court rejected an East German statutory justification for border guards who shot at their own citizens trying to flee the country for the West.9 All of these decisions brought to the fore fundamental values of protecting life and punishing those with contempt for life. Yet, the particular German emphasis on these values would probably not appeal in the same measure to other European courts.
The Germans themselves have coined a unique, hard-to-translate phrase to describe the controversies that have driven their system of justice for the last fifty years. They call it Bewältigung der Vergangenheit—“overcoming” or “coming to 
grips with” the past. Settling accounts with the past provides a critical perspective on the process of redemption from evil. We cannot avoid the past, for we are all prisoners of it. In real life, we cannot reenact the forty years of wandering in the desert that the Hebrews had to endure before they could shake off their ingrained ways and a new generation could seek redemption under the law. In the world of practical politics, we must act now, and criminal punishment 
often provides the mechanism for distancing ourselves from the past so that we can start anew.
As France and Germany had their experiences of seeking redemption after reigns of terror, Americans, too, indulged in the mammoth bloodletting on the killing fields of the Civil War. When Lincoln sought to resupply Fort Sumter in Charleston harbor, and General Beauregard chose in response to fire on the federal fort, the long-simmering feud between North and South bled into brothers’ killing each other at close range. They fired their canons on Fort Sumter, they fixed their bayonets at Little Round Top, they lobbed shells onto Vicksburg until troops could seize the forts reigning over the Mississippi, they burned down Atlanta, and under William Tecumseh Sherman they scorched the earth on their march to the sea. The blue and the gray fell everywhere. And they were not sure why. They only had abstract ideas in their heads—some died for the Union, others for their separate nation. Over six hundred thousand lives stained the ground, more 
than all the former and subsequent American wars put together.
In the ensuing chapters, we will look at these words and the entire address in greater detail. For now, I wish to make the unusual claim that these revered words serve as the preamble for the constitutional order that emerged from the unification of the nation. They are a preamble in much the same sense that the language beginning “Conscious of our responsibility before God and humanity” provides the organizing principle of the new German constitution or the following words echo in memory as the convening of the Philadelphia Constitution:
```
