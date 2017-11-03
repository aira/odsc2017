---
title: There's Hope for Chatbots
lang: en
revealjs-url: ''  # for absolute path to lib/ and css/ folders use '/'
theme: black
transition: fade  # none/fade/slide/convex/concave/zoom
center: false
---

## There's Hope for Chatbots

----------

* Chatbots are Everywhere
* Why?
* Stroll through the ChatBot Zoo (Pandorabot)
* Two Approaches
* Breakthroughs
* Python Chatbot Frameworks
* ChatterBot APIs
* Demo

----------

# Chatbots are Hidden in Plain Sight

- SlackBot
- Amazon Echo
- Google Now
- Zukerberg's Personal Assistant
- Siri

<aside data-markdown="" class="notes">
How do they work?
the innards of chatbots are hidden in a loAs I was researching chatbots
The software behind Siri is the same as for a chatbot
English in, English out
Wrap it in STT and TTS and you've got Siri
</aside>

----------

# ELIZA

* 1964
* Therapist Bot
* Used "reflection"

```text
Gorman: Whoa, conversations with an AI. Skynet is near.
ELIZA : I see. What makes you feel that way?
```

<aside data-markdown="" class="notes">
Joseph Weizenbaum  
14 years after Turing test
Reflection:  
1. Claim understanding  
2. Repeat what they said  
3. Replace "I" with "you"  
4. Ask for details, emotions  
</aside>

------------

# What about Tai?

* Why was Tai so cruel?
* It "reflected" it's audience
* Online learning is risky
* "Prime Objective": Popularity 

<aside data-markdown="" class="notes">
The core tech I'm going to show you is live  
And it's even less sophisticated than Tai  
So be careful  
</aside>

----------

# Gamergate

Chatbots that

* Coax users into being civil
* Enforce behavior rules
* Make harassers uncomfortable

<aside data-markdown="" class="notes">
* 40% of harassers ceased when confronted with a bot
* Most remaining "cured" with threats of penalty
* Very few kick-bans required
* Any gamers out there?
* Run into any "referee" chatbots?
</aside>

----------

# Micromoments

* Friendly, slick sales bots

> "You look great this morning."

> "Have a great day at work today."

<aside data-markdown="" class="notes">
Flattery will get you everywhere
As nice as it sounds, it's manipulative
</aside>

----------

## Bot Community

[PandoraBots](http://www.pandorabots.com/)

* Like SquareSpace for bots
* Grammar for Q&A (flash cards!)
* Statistical ML too
* Bots can talk to each other (APIs)

----------

## Example Grammar

Who built Siri?

<aside>
* Predicate: What the subject of a sentence does or is
* Interrogative Pronoun: asks a questions without identifying the noun
* Pronoun: He, she, it, then but without refernce to a known noun
* Who, what, where, when
* Extract the predicate
* Wiki the predicate and replace pronoun with the name of the page
</aside>

----------

## Problem with Word2Vec

> BFF  
> 4EVAH  
> XOXO  
> &h!t  

<aside data-markdown="" class="notes">
pretrained on WSJ formal english  
emoticons  
slang  
cursing  
obfuscation  
</aside> 

----------

## Grammar-Based

* subject: the "primary" noun active noun phrase of a sentence 
* predicate: verb phrase that says what happened to the subject

<div><aside data-markdown="" class="notes">
ELIZA used simple grammar rule called "reflection"  
PandoraBots uses similar predicate-processing rule to answer questions 
subject: Root of the AST In Parsey McParseface     
predicate: depends on the subject  and the object?
</aside></div>

----------

## Parsey McParseface](https://research.googleblog.com/2016/05/announcing-syntaxnet-worlds-most.html)

**[SyntaxNet](https://github.com/tensorflow/models/tree/master/syntaxnet)**

* Best Syntax-Tree tagger
* Best POS tagger

<div><aside data-markdown="" class="notes">
Statistical training of grammar tagger!
Used for grammar-based approaches
</aside></div>

----------

## Chomsky


> You: What's up?  
> Chomsky: I am chatting with my friends on the internet.  
> You: Cool! How do you do that?  
> Chomsky: Always stay cool whatever the weather. It is sometimes difficult, but I stick at it.

----------

## [Josh's Mom](https://chatbotsmagazine.com/what-if-mom-had-a-chatbot-that-could-live-on-after-shes-gone-video-b9e11dab1937#.788p5kw6m)

Hey Mom.  
> Hello.  
How are you?  
> I'm doin' pretty good.  
What are you doin'?  
> I'm reading a book.  
Hey, can you send me a photo of us?  
> [bot sends photo] Remember this?  
Yea... I do... I miss you.  
> I miss you too.  

<div><aside data-markdown class="notes">
* Josh Bocanegra basing bot on Mother
* CEO of Humai, a technology
* To reduce and maybe prolong grief
* Like Google maps, uses voice recordings, not TTS
* Logic engine is similar to ChatterBot
* We can use ChatterBot for "personality recording"
* Like a telephone conversation recording, but dynamic
</aside></div>

----------

## Smart, Useful bots

* Google Now ("OK Google")
* Siri
* Allo (Google Assistant)

<div><aside data-markdown class="notes">
You probably don't think of these as chat bots
But they are
They just have voice recognition layer on top
I'll show you how to add that to your bots too! (Sphinx)
</aside></div>

----------

## Sensitive Bots

* [Viv](https://techcrunch.com/2015/02/20/viv-built-by-siris-creators-scores-12-5-million-for-an-ai-technology-that-can-teach-itself/): Dag Kittlaus

Siri, but smarter

----------

* [The Chatbot Club](http://www.lifehacker.com.au/2016/05/meet-viv-the-future-of-chatbots-and-artificial-intelligence/): Linda Chang

Mimics your personality on FB (you're sensitive, aren't you?)

----------

## Koko (MIT)

Ground-up design for empathy

----------

## [Allo](https://research.googleblog.com/2016/05/chat-smarter-with-allo.html)

* LSTM
* TensorFlow

<div><aside data-markdown="" class="notes">
"Smarter" Chat by Google
</aside></div>

---

## Experiments

----------

## [Speakeasy](http://lauragelston.ghost.io/)

* Character-level LSTM NN
* Quickly goes "off the rails"

----------

## [Mitsuku](http://www.mitsuku.com/)

* 2013 Winner of the Loebnez Prize!
* [Chat with it]((http://www.square-bear.co.uk/mitsuku/nfchat.htm)) yourself
* Backend is [open sourced](https://github.com/pandorabots/pandorabots.github.io/blob/master/_modules/mitsuku.md)
* Ontology-based

<div><aside data-markdown="" class="notes">
Most human-like open chatbot in 2013
"Stands her ground" in an argument
Large ontology backend (knowledge base)
</aside></div>

----------

## How?

* regular expressions?
* statistical models (Markhov Chains)?
* logical grammar?

> * YES!

<div><aside data-markdown="" class="notes">
Chatterbot allows plugin of multiple LogicAdapters
So lets do them all!
</aside></div>

---

## Statistical Language Models

1. BOC (cryptography)
2. BOW (spam filters)
3. Bag of N-Grams
4. Sequence of Words
5. [Sequence of Characters](https://github.com/Lasagne/Recipes/blob/master/examples/lstm_text_generation.py)

<div><aside data-markdown="" class="notes">
More and more data required
More and more realism/fidelity/robustness
SOC RNN (LSTM) required for sophisticated/flexible chatbot (e.g. Tai, Siri, Google Assistant)
</aside></div>

----------

## Word Vectors

* LSI/PCA (Gensim)
* LDA (Gensim)
* Neural Nets (Word2Vec)

<div><aside data-markdown="" class="notes">
</aside></div>

----------

## Python Options

* Wil
* **Chatterbot**


----------

## Logic Adapter

----------

## DB Model Enhancements

----------

## Chat Age

* Flesch-Kincaid Grade level
* [Google NGram DB](https://books.google.com/ngrams) mean year

----------

## Sentiment 

* `NLTK`'s VADER by Hutto, C.J. & Gilbert
* 3-D "valence": positivitity, negativity, neutrality
* 1-D intensity

----------

## Sarcasm

* trained on #sarcasm in twitter
* need context to improve on 70% accuracy

----------

## Kindness

Positivity / Sarcasm - Intensity - Negativity / Sarcasm + Readability + Chat Age

* curse words?
* use of "you" as multiplier?

----------

## New Hope

- Grammar: [SyntaxNet](https://github.com/tensorflow/models/tree/master/syntaxnet)
- Statistics: [Word2Vec & Gensim](https://radimrehurek.com/gensim/models/word2vec.html)
- Text: [Gutenberg](https://en.wikipedia.org/wiki/Project_Gutenberg)
- N-Grams: [Google Books](http://storage.googleapis.com/books/ngrams/books/datasetsv2.html)
- Knowledge: [YAGO](https://en.wikipedia.org/wiki/YAGO_(database))

<div><aside data-markdown="" class="notes">

**SyntaxNet** Parsey McParseface
* POS tagging
* syntax/dependency tree  
  
**Word2Vec**  
* Pretrained High-Fi Vectors for WSJ language  
* Not good for informal slang  
* Easy to train on tweets and other "one-liner" sources  

**Gutenberg**
* Pre 1950's only
* Full text
* No tech terms

**N-Grams**
* 1-5-grams
* Occurr at least 40 times
* 15% of all books
* Lots of modern tech jargon!
* Great for word "age" tagging

**YAGO** yet another great ontology   
* 95% accurate  
* core to Watson  
* DBPedia, SUMO, WordNet  

</aside></div>

---------- 

## How Do I Make Hope Talk!

* Best Speech Synthesizer (TTS): [WaveNet](https://arxiv.org/pdf/1609.03499.pdf)

(and Listen)

* Best Speech Transcription (STT): [LSTM RNNs](https://research.googleblog.com/2015/08/the-neural-networks-behind-google-voice.html)

<div><aside data-markdown="" class="notes">
WaveNet is open source!
Best speech recognition packages are closed source
Google describes architecture (LSTM)
and Speech recognition are easily trained
and Kaldi, Sphinx are pretty good (Gaussian Mixture Models)
</aside></div>

----------

<div><aside markdown-data class="notes">
I'm going to show you how to build a prosocial chatbot, or at the very least least, a bot that  isn't antisocial. In the process you're going to get a peak into the technology used by most AI systems that interract in a natural way. But before all that I'd like to explain why I'm so passionate about chatbots. After all, most of them that we interract with are pretty annoying, almost infantile. They can be fun to play with, but aren't usualy all that helpful. And sometimes it's downright dehumanizing to be forced to deal with a machine when you know there's a human out there watching all the text stream by just waiting for you to say the magic word to step in and help you complete you get the information you need or complete your purchase. But for the call center personel who previously were treated like robots themselves, forced to click through a logic tree of questions and responses, all day long, it's probably a bit empowering. They finaly have a pet to keep them entertained while they work to help you solve your problem. 
</aside></div>

<div><aside markdown-data class="notes">
And if you need a bigger picture reason, consider the concerns of Gates, Musk, Bostrom, and Chace who title their concerns "Surviving AI" or talk about a "Superintelligence Explosion" that could destroy human civilization. That's what inspires me. In the back of my mind I've convinced myself I've fighting the good fight on behalf of the human race. The big robotic machines called Google, Apple, Microsoft, or even Canonical. These bots have a one-tracked mind. They want to sell you something. The can listen to you, and give you new and interesting information and fun things to do, but they are always just waiting to pounce with just the right product to manipulate you into wanting. That maniuplative employment of "influence techniques" is antisocial, not social. So if we let corporations build our bots, none of them will have a soul. And more and more, we are being left out of the conversation. Bots are talking to each other through web APIs. Even if we monitored the traffic, it wouldn't be much fun reading through all the log files to look for bot conspiracies. We humans have the good manners to use the language of those around us rather than having coded conversations behind our neighbors' back. Or bots should be so polite.
</aside></div>

<div><aside markdown-data class="notes">
There are two approaches to chatbots that are working pretty well right now. We're going to combine both.  There's Will with his good manners and rules for action. He can answer your questions and obey your commands, because under the hood he has a graph of logic rules encoded into regular expressions and python conditionals (if-then-else). But if you step just outside of the bounds of what he understands by saying something like "tank u", his logic might get befuddled and Will will be speechless, unable to respond with his oft-used but enthusiastic response "Your welcome!".
</aside></div>

<div><aside markdown-data class="notes">
So once you teach your bot manners you can expand its repertoire more quickly with Machine Learning. Like an authoritarian, over-protective parent you can discover the magic of letting a child learn from its own mistakes and successes. And eventually you can no longer tell them to "do what I say, not what I do." That's the approach of bots like "Salvius" (`ChatterBot`). Salvius imitates the conversations he sees his parents (the human race) to. So all you need to do is socialize him by giving him a homelessman disguise and he'll learn from the conversations of all the passersby around him. Or, if you want to give him a crash course, just feed him a bunch of "call and response" musical lyrics or Shakespeare dialog and he'll be speaking like a born thesbian in no time. You can culture your bot any way you like.
</aside></div>

<div><aside markdown-data class="notes">
When we first domesticated wolves and ungulates, we chose those that were most domesticatable. When we tried with foxes and bears and other animals, we quickly learned our lesson that some things are teachable and some things aren't. Those that could obey our rules, like sitting back away from the campfire and hearth and waiting us to finish our meal before cleaning up our scraps. But they weren't pups when we first encountered them. When we raise our own children we just use baby talk to get their mouths moving and try to have conversations around them so they know what conversations look like. So we're going to start with Salvius, the imitation bot by Gunther Cox (who started the Salvious project as a High School science experiment!).
</aside></div>

----------

## Algorithm Ideas

- Analogy/generalization mad libs:
  - find words that appear in both statement and response
  - replace these paired words with their part of speech or some other "word type" in a separate statement_template, resonse_template DB record
  - for matches on these madlibs sentences that happen to be off on this filler word then transfer the missing word from the statement to the response
  - hack: surround all such words with -<{}>- to make them match levenshtein distance even when paired words don't match
- 4-D GIS index on LDA topic vectors for statements and responses

----------

<aside>
## Plan

[*] draft slides
[ ] styled revealjs slides

[-] train ChatterBot on tweets and other dialog DBs in data/
[-] script to convert lines of text (with empty lines to break) into Chatterbot Conversations json
[ ] train ChatterBot on Shakespear and copy sqlite DB to separate file
[ ] matched text (response_to: ) along side the response in small text.
[ ] add sentiment analysis within ChatterBot framework
[*] install ChatterBot in `hope` django project/apps
[=] convert to postgres on `hope` django app
[-] implement madlibs hack
[ ] add twip predictor to ChatterBot logic
[-] add tests and get them passing
[-] add datetime extractor to logic
</aside>