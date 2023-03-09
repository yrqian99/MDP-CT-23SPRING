## Project2 Documentation

https://yrqian99.github.io/MDP-CT-23SPRING/Project2Chatbot/



My chatbot is a **Shakespearean Compliment Battle Bot**. As indicated by its name, it hosts a Shakespearean compliment battle. After calling the start of the battle, it selects a random member in the channel, and the rest of the members are free to throw compliments to the selected one. For now, the participants are limited to the first three people responding in the channel. The compliments should try to be phrased to in the Shakespearean style, and the most Shakespearean one will win the game. 

I used **Word Vector algorithm** to perform a sentence similarity that checks its similarity with Shakespeare’s Sonnets. It will calculate a cosine similarity score between the sentence and the sonnets. The lower the score is, the more Shakespearean the compliment is. And the winner will be awarded to the most Shakespearean compliment and its author. Lastly, it will pulling out the line from the sonnets that each compliment is most similar to, and combine them into one.

![](images\diagram.png)

------

I started by printing the list of members in a discord channel:

![print_list_of_member_code](images\print_list_of_member_code.png)

![print_list_of_member](images\print_list_of_member.png)

------

Before pivoting to the idea of throwing compliments to one member, I had the idea of pairing the members up into groups of two and let them compliment each other:

![randomly_pair_up_code](C:\Users\Rue\Dropbox\MDP\23SPRING\CT\Project2Bot\documentation\randomly_pair_up_code.png)

![randomly_pair_up](images\randomly_pair_up.png)
