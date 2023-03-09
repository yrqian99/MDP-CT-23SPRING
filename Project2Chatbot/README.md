## Project2 Documentation

https://yrqian99.github.io/MDP-CT-23SPRING/Project2Chatbot/



My chatbot is a **Shakespearean Compliment Battle Bot**. As indicated by its name, it hosts a Shakespearean compliment battle. After calling the start of the battle, it selects a random member in the channel, and the rest of the members are free to throw compliments to the selected one. For now, the participants are limited to the first three people responding in the channel. The compliments should try to be phrased to in the Shakespearean style, and the most Shakespearean one will win the game. 

I used **Word Vector algorithm** to perform a sentence similarity that checks its similarity with Shakespeare’s Sonnets. It will calculate a cosine similarity score between the sentence and the sonnets. The lower the score is, the more Shakespearean the compliment is. And the winner will be awarded to the most Shakespearean compliment and its author. Lastly, it will pulling out the line from the sonnets that each compliment is most similar to, and combine them into one.

![](images\diagram.png)

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

<img src="images\randomly_pick_one.png" alt="randomly_pick_one" style="zoom:50%;" />
