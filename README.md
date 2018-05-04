# Final Assignment
## "QWERTY be like dat"

Keyboard layout - who? what? and also, why? 
One of the most common ways of communication in the past 150 years of typing. We talk with it, we learn with it, we play on it.
Hell, we even let it drink coffee every once in a while. This image of a keyboard, is criminally trivial to us, and so weird and mysterious. Time to break the mystery - The QWERTY leyout was designed by Christpher Sholes. The design took the most common two letters combination in English and placed each letter as far as possible from each other. Why? so the type writer won't get jammed, since when typing two close characters they could get stuck... hmmmm.

Anyway, I dare you to stare at this and not freak-out:

![900px-kb_united_states_dvorak svg](https://user-images.githubusercontent.com/31703048/39634329-82fdd2c2-4f88-11e8-9954-2927c6249c5a.png)





For the final assignment I decided to try and show what does this bizzare phenomenon has to say through copmutational poetry.
What do our fingers and muscles have to say when they're banging on the QWERTY keyboard.

### The Process :

I wanted to create a corpus of gibberish that is made out of people going-berserk on a computer keyboard. So, I asked ITP students to give me their own gibberish, and I parsed it into one big corpus (lots of j's and f's there).

Then I took this corpus and trained the "textgenrnn" training model to create my own gibberish model. 
Now - in order to make the output interesting I decided to use another source text that I'll infuse into the gibberish model, thous turning it to a somewhat readable text. For this matter I was thinking, which piece can be Ironically merge into a giant pile of nonsense. I came up with King David's Psalms. As one of the oldest writen poetry, the Psalms has a distinct style, and an iteresting vocabulary. 

The algorythem:
The purpose here was to somehow create an arc to the output by starting with gibberish text and through time make the text more meaningful. The output is generated from the original gibberish that is made out of ITP's keyboard mess.

I'm creating a new "live" gibberish text, and clean it from all the numbers and punctuations, dividing it randomaly into words, then training the gibberish model with it. I then choose random lines from the Psalms, and gradually infuse the psalms text by training the gibberish model with it. I iterate that as much as the original live-gibberish text, thous making the model more Psalmy. Now, I have decided to make things a little more weird. Every iteration of training the model with the Psalms text, I'm also runing it through semantic vector replacement function. Each iteration I'm increasing the "nuttiness" and the "chance" and making the output lines more twisted and deformed. 
The output text was a bit weird, so I did some cleaning, such as removing any "bad word" (the, a, as, with, etc) from the ends of sentences, and tried to make the lines smaller.

When it comes to reading, I really wanted to make the performance a "here and now" and not choose the best lines or the ones theat makes most sense. I feel that this way, I can truly represent the live output of QWERTY "keyboard playing".

Here's an example of an output :

![screen shot 2018-05-02 at 15 57 05](https://user-images.githubusercontent.com/31703048/39634393-b2725dc0-4f88-11e8-9061-6a6030f644ad.png)




#  Assignment #6
## A hearing problem

For my final project I would like to investigate miscommunication, and take a dialogue to a spiralling chaos of meaning. 
I want to create a "Telephone" game. But instead of phonetic misundertanding I want to make it an exponential misinterperting chaos. I'm intrigued by the notion of how miscommunication is the cause of 90% of our conflicts and our discourse with our surrounding. Maybe there is a way I can take miscommunication to a more empowering and positive place.  

For this assignment I wanted to create a regular "Telephone" game with phonetic manipulation...

The Concept:

As part of my research for a different project I looked into the trancription of "Inconvenient Truth" - the famous environmental presentation of Al Gore. 
I imagined two senior citizens sitting in the audience (kind of like Statler and Waldorf from the Muppet Show), and constantly confusing each other by mishearing what the former senator says. 

The Process:

I used SpaCy to choose the verbs and the nouns (The important parts of speach) from the randomly-picked sentence.
for each verb/noun I randomly picked a rhyming word using "Pronouncing" and parsed them all back to the sentence.
So, the first sentence of each iteration is from Al's presentation and then comes the broken sentence. 

I still have some trouble with the code.

First, for some reason the rhymes that are beeing chosen are super weird and unusual.
Second, sometimes the cell of the for loop gives me an error that there are no rhymes for a word, and I don't know how to dubug it. I encountered some trouble with the SpaCy types (Tokens) that I couldn't figure out how to transform them to be able to do regular expressions with them. So I don't know if I need to do something to the text before I'm "SpaCy"ing it or maybe I'm using "Pronouncing" wrong. Like, I figured out that "pronoiuncing.rhymes" doesn't work on upper-case words. So, for some reason I was having trouble manipulatig the words to a lower case without changing the SpaCy tokens. Perhaps I need to go through SpaCy again...





example 1:

![screen shot 2018-04-13 at 11 45 39](https://user-images.githubusercontent.com/31703048/38744877-01897aa2-3f11-11e8-83b9-0f3b3432c709.png)

example 2:

![screen shot 2018-04-13 at 11 47 33](https://user-images.githubusercontent.com/31703048/38744876-01787194-3f11-11e8-9675-9218535ebf3f.png)

example 3:

![screen shot 2018-04-13 at 11 49 53](https://user-images.githubusercontent.com/31703048/38744875-016a55be-3f11-11e8-83c5-b786c1bd7693.png)

example 4:

![screen shot 2018-04-13 at 11 57 17](https://user-images.githubusercontent.com/31703048/38745200-e11f4cb4-3f11-11e8-9330-d877b28c8480.png)

#  Assignment #5
## RNNNGRAMS and spaCy

Source text = the script of "Star Wars - New Hope"...

To my perspective, this film represents an important form of new mythologies. 
So, I wanted to use the Hollywood-script-vibe of writing, to see if it could be manipulized to poetry.

To be honest, I'm not very happy with this work...

Seeing the wonderful things you can do with n-grams got me really excited. But, I felt like I had put myself (literally) inside the Millenium Falcon's cockpit and tried to jump into hyper-space. Like there are a lot of buttons, and flashing gizmos that I don't relly know how to approach.

Eventually I came up with two pieces -  n-gram sentences poem ,and a spaCy generated poem.
I started with simply copying the functions from the notebooks, and tried to play arround with the structure.

For the n-gram poem, I looked at what are the most common pairs of words, and then I had randomly selected out of the first 50.
Using those "pairs" I made two generated markov-chained and seperated them with a line. Well, It's not really a poem but I enjoy the subtle-but-not-subtle mess it does to the story.

For the SpaCy - I simply reached into the script and took nouns, verbs, adjectives and adaptors. Then I parsed them into a sentence form that creates a poetic vibe. The outcome surprised me how it sounded traditionally poetic. 
"Hooded under mechanical death" - beautiful!

The combination of space-battles, stupid dialogues, scenary descriptions, 70's jargon, and a whole lot of "DEATH" - creates a funny twisted poems and some crazy lines.

These are the n-gram :

![screen shot 2018-03-30 at 14 35 39](https://user-images.githubusercontent.com/31703048/38149737-c208ea8a-3429-11e8-9004-fb030172c06c.png)


![screen shot 2018-03-30 at 13 49 12](https://user-images.githubusercontent.com/31703048/38147842-f9700600-3421-11e8-8020-be5dee0deb2d.png)


And these are the spaCy :

![screen shot 2018-03-30 at 13 44 22](https://user-images.githubusercontent.com/31703048/38147843-f97df828-3421-11e8-831b-1aa28437c2cf.png)
![screen shot 2018-03-30 at 12 50 15](https://user-images.githubusercontent.com/31703048/38147844-f994af46-3421-11e8-9c1c-05620c2ad190.png)
![screen shot 2018-03-30 at 12 49 21](https://user-images.githubusercontent.com/31703048/38147845-f99ed408-3421-11e8-99b3-73f83493fa7c.png)

![screen shot 2018-03-30 at 14 19 05](https://user-images.githubusercontent.com/31703048/38148680-7a33a1d6-3425-11e8-9977-778c67de4662.png)


#  Assignment #4
## A new poetic form - Chain links

In this assignment we were asked to create a new poetic form using the tools we discussed in class (tracery, dictionaries,etc). The idea of a poetic form is a phenomenon I haven't really thought about in my few encounters with poetry. I realized that a structure of a poem is an additional face for a poetic or even a literature piece. A side that is no less important than the content or language. 

## Sateen Lemurs
Like the last assignments, I started by scribbling on a piece of paper what I would like to talk about. Then I wrote down "metallic rabbits". I liked the combination of living organisms with different materials and elements. I played around with the idea of somehow expressing the hard time we humans give the rest of the animal kingdom and maybe turn the animals against humans. But then I started thinking of the structure or the form I want to give the poem. Again, as the previous exrcise, I wanted to create a palindrome of some sort, but now I wanted to add more flow to the structure and create a chain of links that talk to each other. A repeatable or even a neverending cycle.
I have to be honest, I'm not sure that this is considered as a new poetic form, but I feel that there is a "body" here, with rules other than "which source text am I using" 
When I combined all these thoughts of the structure and the content, I decided to make a poem that expresses the notion of a never ending stereotype cycle of animal relations. Sometimes the relations has a fascist vibe, and sometimes it feels like love is the air.
Either way the relations depend on the material of the animal and not of the animal itself - kind of reverse racism I would say . I was happy and somewhat surprised with what was coming out.

I used a few JSON files from "corpora", and got a little lost inside the 'verb' file. Since I wanted to use pefect tense, i needed the big file which is pretty messy and contains a lot of junk.
I used 'tracery' to create the poem 'links' but then I got stuck in reusing the same animal and material twice, I turned to Kate Compton through Google and got over the obsticle (see assignment notebook). 
I wanted each 'link' or poem in the 'for loop' to use different verbs but inside the poem I needed to use the same verb twice- for that (and with the help of Allison) we duplicated the rules-dictionary and took the verbs outside to the for-loop.
The specific layout of each poem was decided in orde to look like a chain that is being linked with transitions and circular "buts".
What I haven't managed to do with "Tracery" is to make the "active" animals become th "passive" animals in the next poem or "link in the chain".
I have made another notbook that does not use "Tracery" and managed to make tha chain effect I was looking for.

Anyway - here are some examples:

The first one is using "Tracery" and the result is not satisfying since the animals don't repeat in the next "link" : 

![screen shot 2018-03-08 at 23 56 41](https://user-images.githubusercontent.com/31703048/37191414-5991e180-232d-11e8-9233-c6a3e4ae5fa7.png)

These ones are better - not using Tracery : 

![screen shot 2018-03-09 at 14 07 52](https://user-images.githubusercontent.com/31703048/37225179-c95892f4-23a3-11e8-8483-72bdefb31540.png)


![screen shot 2018-03-09 at 14 08 33](https://user-images.githubusercontent.com/31703048/37225082-7f08a342-23a3-11e8-8e47-1d521d370f4d.png)

![screen shot 2018-03-09 at 15 28 39](https://user-images.githubusercontent.com/31703048/37228446-ad5e8378-23ae-11e8-83be-119bfcf5bfee.png)


A good short : 

![screen shot 2018-03-08 at 23 58 13](https://user-images.githubusercontent.com/31703048/37191451-b53eba12-232d-11e8-9969-587056dfbd6d.png)


generally I feel that the form delivers what it promisses - a continoues stereotype mess in the animal kingdom (sort of).
My choice of source text definitely give the poem a comic vibe to it. I enjoy the playfulness and cynicism of the poem, but I also feel the message is being lightly noticed.


 


#  Assignment #3
## Poetry Masher
In this assignment we were asked to create a poem out of two text files, by using different list comprehension and other elements we learned in class.

The concept :

I wanted to create a piece that has a repeatable structure. A poem that will have a sense of rolling or rythem. So I decided to make a repetitive word after every line that will give the poem some movement and emphasis.


The process :

the main frame of manipulating a text file is to turn it into a list. In my example I started by creating a list of lines and then I drilled a little more and used single words.
I took two poems, and chose two random lines from each one.
Then I chose a random word from each line and repeated that word for three times. On the third time I added another phrase or adjective that gives an extra twist for the repeated word.
During the work, I played aruond a little with the order of the lines and mashed the chosen words a bit more. 
In the end I chose a chiastic frame. I repeated a word from the last line, after the first line. Then repeated a word from the third line, after the second line, and so on. 
I just love chiastic structure.

For the extra phrase I chose dark and negative adjectives. For some reason it seemed to give much more interesting results.

I had to deal with a lot of repeating words that weren't fitting the structure. Words like 'the', 'and' , 'of' etc. I guess I could of come-up with a way to leave them out when I choose the repeated words.  

Here it is :

![screen shot 2018-02-23 at 12 20 44](https://user-images.githubusercontent.com/31703048/36607255-12f3629c-1894-11e8-8a6c-c77b7c3d14de.png)



![verymashed1](https://user-images.githubusercontent.com/31703048/36570915-4fe41d32-1802-11e8-8108-952afbc1f49a.png)


A different structure that uses a word from the previous line (not chiastic):

![mashed2](https://user-images.githubusercontent.com/31703048/36571011-b7c0bd52-1802-11e8-9c90-a012560bb7ef.png)


A good short one :

![mashedshort1](https://user-images.githubusercontent.com/31703048/36571084-0e74de44-1803-11e8-8544-0e6935e03787.png)





# Reading response
## Randomness, Juxtaposition, Surprise

#### Juxtaposition
When I read the first example in "Start with poetry" and the comparison between the two pieces, I had a thought about an element we talked about in another class("Nothing-creating illusions"). In "Nothing" we talked about vision and how our brains are working to complete an outline of an object. We saw some examples of fragments of an image or an object, and we were able to materialize and figure what exactly are we looking at. The important idea of subtracting as much as possible without loosing the meaning realy spoke to me. I tend to think, that the less you present, the more interactive your piece can be.
"Shaving" the transitions and the perfectly-makes-sense elements, gives the reader more space to be immersed in the search for meaning. I didn't notice this method (or rather couldn't point it out) so far, and now that I do, I realize how powerful it is.

On the other hand, it's a dangerous tool. Like it is said in the book : "Eventually, though, the gap would get too big to cross". To my opinion, let's say in visual arts, the fine line between non-sense and sense is drawn by the viewer. Here I feel that linguistic art has more restrictions, has more visibility to define the border. The logic and the context have a preety clear threshold to the non-sense part. Well, of course that Lewis Carroll's poems are mind-blowing. I simply believe that the rules of linguistics are more clear and the emotions you feel when you encounter a "gap" you can't cross in a poem, are more intense. Probably in a bad way. Maybe it's only me.

#### Randomness
The question of randomness being a "juxtaposition-generator" brought up a small philosophical thought. I was thinking of order and disorder, and their relations. Is it a spectrum? is there such a thing a little disorder? Or maybe it's binary? 
0 for disorder, 1 for order? of course these questions are related to the point-of-view, related to the judgemental nature of the viewer/reader. I personally feel that disorder is a matter of scale. The small systems must be in chaos so the large picture would be of meaning and stable in a sort of way.  

Randomness is a catalist for curiosity. It's a very efficient way to let the listener/reader/viewer engage his deep thinking and emotions. When I see a random pattern of any kind, I'm just eager to draw lines between the dots and let my brain do the rest. I like the fact that I'm not carefully approaching a work of art that someone already made the thinking for me.
Here I feel I have a crucial role in the work. Knowing that even the author can be surprised from his work is a very powerful thought.  
I think that the awareness of randomness is is also playing a role in the game. If I was to read a poem, that crushed my soul into bits and pieces and made me cry, and then I realize that it was randomly made by a machine, I would ask some serious questions about the world.

I believe, that the procedural technique and the choice of source are the paint brush and the colors we are given as readers. For example - the resolution and the relations between the words in the text can determine the nature and the abstraction of the poem. The farther the connections are, the more mystery we get. The splising mechanism paves the layout of the poem.
It creates a path for us to walk through. To walk in the general places that the poet wanted us to walk.  

#  Assignment #2
## Poetry generator

I call it  "Last transmission".
I have a wild imagination, this time it involved Sci-Fi scenary.
The Idea behind this poem generator is to recreate the last communication sequences from a combat ship in distress.
I chose this subject, or this kind of text because it seems like it's very far from poetry. With calling this a poem, I make the readers see these transmissions in a poetic light. The concept came to me really fast and really intuitively, so it's a bit hard for me to write what I was thinking. Anyway...

I played around with the generators we were given, and I really wanted to make my own simple one.
The generator is very simple. I made a template of the message and then made 6 lists of the different components.
The different words are being chosen randomly, and give new details on the scene or the hero's actions. 
Then I used "print()" and constructed the poem. I decided to give the poem a shape that reminded me of a spaceship from the side. 

I wanted to see how each message delivers a different vibe, or situation. Each situation conjur a different vision of who is the pilot. Is he a hero? a coward? a wierd irrational person? an idealist, or a survivor? Whether he chooses to be able to communicate, use the weapons, come out alive and see the next day, etc.
At first I chose words that implied that the pilot is a man (by accident). Then I modify them to be also as if the pilot is a woman. 

I feel like there is nothing smart about my generator and I would very like to try and make it more interesting. Like making the pilot totally irrational and make the words correlate to each other.

After I did that I remembered a famous Holocaust poem I learned in Highschool, written by Hebrew writer Dan Pagis:

Here in this carload
I Eve
Am with my son Abel 
If you see my firstborn son
Cain son of Man
Tell him I am...

(an important anacdote - this poem is supoose to be read in a loop).

There is something very powerful in a "last message". It is very hard to imagine the last words of a person as a poem.
My poem, off course, has a Hollywood like feel to it which make it a little cyinical. I decided not to write stuff that will sound like a joke, but rather be more solemn.

![screen shot 2018-02-09 at 11 41 46](https://user-images.githubusercontent.com/31703048/36039238-e9ec16dc-0d8f-11e8-955b-efd3734d995d.png)



![screen shot 2018-02-09 at 11 40 35](https://user-images.githubusercontent.com/31703048/36039499-a831f648-0d90-11e8-9258-e2e2b61bb3d5.png)



![screen shot 2018-02-09 at 11 39 42](https://user-images.githubusercontent.com/31703048/36039575-e09dad4c-0d90-11e8-8372-51d9e593f836.png)



![screen shot 2018-02-09 at 11 38 47](https://user-images.githubusercontent.com/31703048/36039637-15a719ce-0d91-11e8-9c05-f3c67f7624b1.png)



![screen shot 2018-02-09 at 11 34 31](https://user-images.githubusercontent.com/31703048/36039676-36472fa2-0d91-11e8-87ea-8cc75db1daa8.png)



![screen shot 2018-02-09 at 11 33 51](https://user-images.githubusercontent.com/31703048/36039715-53046bdc-0d91-11e8-8d89-28459fad90a0.png)


# Week #2 Assignment
## Transcription

One of my favorite scenes in films is the scene from Stanley Kubrick's "Full Metal Jacket".
The film tells the story of soldiers being sent to Vietnam.
In this scene we see new recruits for the Marine Corps being brutally discipline by their drill-sergeat.
In one of the best rantings in film history, The drill sergeant just bombs them with violant, racist, foul mouth speach.
Since I really love this scene, I really wanted to try and transcribe it, by listening of course. 
Unfortunatelly, this is a little bit too offensive so I decided to try and transcribe something else.

I'm taking a class at cinema studies here at Tisch, and last week we saw the film "They shoot horses, don't they?".
At last minute, I decided to transcribe the dialogs between the two main charaters.
Here I decided to do the first dialouges as dry as I can, in order to emphasize the scenary in the last one.
It got me to think - Does describing scenary counts as transcribig? Is representing the settings and physical reactions a part of the transcriber's roll? I don't know. sometime it has no meaning and sometimes it's crucial. 
https://www.youtube.com/watch?v=Zmwu26X9vXk&t=418s

In the middle, I tried to transcribe an interview with George Harrison in 1971. I realized that transcribing
a real conversation is much harder then transcribing a scripted monolouge/dialogue. In the interview or in a more realistic conversation there are a lot of overlaping sentences, phonetic expressions, and unintelligable phrases. For this transcription task the denaturalization format would be more suitable, but is much harder to preform. In some cases when I was trying to figure out what George is saying, since his so quiet, I just filled in words that I thought he would say. That gives out his humbling cinical nature. That made me feel really powerfull.

This takes me to the reading about the politics of transcription. Some thoughts I had on that:
 - I understand that the roll of the transcriber is much more than simply write down what she/he feels. I understand that it's important to have responsbilty as a transcriber and as a reader. But there are places that I relly want to see just the words and not feel like I'm being manipulated by some one. I think that the only way to do that is with technology. After reading this article, I really see transcription as a form of art, as an expressiv medium of writing. But there are instences in which the importance of the dry words and the phonetic way they were pronounced is too critical. Like the police interrogation instance. 
 - I feel that today, these matters are getting less common since the better quality of recrodings and videos. People are less reading and more listening and watching. There's no fooling you there. Or perhaps there's more manipulation in videos and recordings. Is't a big question. 
 - Now that I understand my biases for the written word of interviews and speaches, I feel I have more ways to engage such a thing and widen my prespective.

