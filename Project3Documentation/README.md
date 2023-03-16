## Project2 Documentation

https://yrqian99.github.io/MDP-CT-23SPRING/Project2Chatbot/



My chatbot is a **Shakespearean Compliment Battle Bot**. As indicated by its name, it hosts a Shakespearean compliment battle. After calling the start of the battle, it selects a random member in the channel, and the rest of the members are free to throw compliments to the selected one. For now, the participants are limited to the first three people responding in the channel. The compliments should try to be phrased to in the Shakespearean style, and the most Shakespearean one will win the game. 

I used **Word Vector algorithm** to perform a sentence similarity that checks its similarity with Shakespeare’s Sonnets. It will calculate a cosine similarity score between the sentence and the sonnets. The lower the score is, the more Shakespearean the compliment is. And the winner will be awarded to the most Shakespearean compliment and its author. Lastly, it will pulling out the line from the sonnets that each compliment is most similar to, and combine them into one.

![diagram](images\diagram.png)

------

I started by printing the list of members in a discord channel:

<img src="images\print_list_of_member_code.png" alt="print_list_of_member_code" style="zoom:50%;" />

<img src="images\print_list_of_member.png" alt="print_list_of_member" style="zoom:50%;" />

------

Before pivoting to the idea of throwing compliments to one member, I had the idea of pairing the members up into groups of two and let them compliment each other:

<img src="images\randomly_pair_up_code.png" alt="randomly_pair_up_code" style="zoom:50%;" />

<img src="images\randomly_pair_up.png" alt="randomly_pair_up" style="zoom:50%;" />

------

Next, I managed to make the bot randomly pick one of the members in the list:

<img src="images\randomly_pick_one_code.png" alt="randomly_pick_one_code" style="zoom:50%;" />

<img src="images\randomly_pick_one.png" alt="randomly_pick_one" style="zoom: 80%;" />

------

Then a major success appears. Following the [Word Vector algorithm tutorial](https://gist.github.com/aparrish/2f562e3737544cf29aaf1af30362f469), I managed to import numpy and spacy, which are the two libraries needed for the algorithm, and conducted a similarity test between two victors, an sentence analysis, and eventually managed to compare the similarity between two words.

<img src="images\sentencesimilaritystep1_importednumpy.PNG" alt="sentencesimilaritystep1_importednumpy" style="zoom:60%;" />

<img src="images\sentencesimilaritystep2_importedspacyforwordvector.PNG" alt="sentencesimilaritystep2_importedspacyforwordvector" style="zoom:60%;" />

<img src="images\sentencesimilaritystep2_wordcomparisonnailed.PNG" alt="sentencesimilaritystep2_wordcomparisonnailed" style="zoom:60%;" />

------

Then, I imported the Shakespeare's Sonnets, and managed to compare the first compliment with the text: 

<img src="images\complimentgamemodified_secondtry.PNG" alt="complimentgamemodified_secondtry" style="zoom:60%;" />

After making sure it's working as I wanted, I made it successful to compare the first three compliments with the text: 

<img src="C:\Users\Rue\Documents\GitHub\MDP-CT-23SPRING\Project2Chatbot\images\complimentgamemodifie_thridtry naileddiscord.PNG" alt="complimentgamemodifie_thridtry naileddiscord" style="zoom: 80%;" />

<img src="images\Inkedcomplimentgamemodifiedthridtrynailed2.jpg" alt="Inkedcomplimentgamemodifiedthridtrynailed2" style="zoom:60%;" />

------

Next, I made the bot compare the similarities between the three compliments, and announcing the one who has the highest similarity (lowest distance) as winner of this round of battle:

 <img src="images\complimentgamemodifiedthridtryinnerannouncing2.PNG" alt="complimentgamemodifiedthridtryinnerannouncing2" style="zoom:60%;" />

<img src="images\complimentgamemodifiedthridtrywinnerannouncing2discord.PNG" alt="complimentgamemodifiedthridtrywinnerannouncing2discord" style="zoom: 80%;" />

------

Last but not least, I combine the sonnet lines that the compliments are most similar to into one, and put an end to the battle:

<img src="images\finished_console.PNG" alt="finished_console" style="zoom:60%;" />

<img src="images\finished_discord.PNG" style="zoom:80%;" />
