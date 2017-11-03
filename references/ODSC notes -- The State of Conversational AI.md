The State of Conversational AI
Mariya Yao
CTO and Head of Research & Design
TOPBOTS

5 approaches to chatbots

Most in production use first 2

1. retrieval
2. rule-based

Rule-based (DOS example)
Retrieval Based
Generative

Scan for keywords
Ranked words in the sentence. Guess what the sentence is about by the keyword and compose a reply based on that.

Mitsuku won the Loebner

Knowledge base of 3000 objects

Tree: color, size, rhymes with

AIML-based (but Mariya called it a Retrieval-based)

Watson was called retrieval-based but described a knowledge-base or ontology-based arch.
Though encoded as rules in AIML-like language.

Sequence to sequence (missed the order of words thing that came up in NLP tutorial)

LSTM (1997): Memory and Attention
Gated RNN (recent)

optimization function focuses on the most common/general/likely word coming next in a sentence.  Get caught in repetitive loops because of this, saying similar things.


seq2seq with reinforcement learning to encourage an engaging conversation.

Markhov decision process is based on the current state representation. So Reinforcement works well because state of board is all there is. POMDP - assumption is that process is MDP but AI can't know what the state is exactly.

Jointly train the user and the agent to create an "adversarial network"


4. Grounded Learning is what we're doing with Aira. Like recommendation about a restaurant that knows about you and the restaurant. Watson is a grounded system.

Requires structured data. Visual question and answering.

Humor comes from figuring out what a statement means, for a rare occurrence. The aha moment is. And they said poodle instead of Lassie or Collie or Black Lab.

5 Interactive Learning

Mitsuku bot took 12 years to develop.

Zootopia engagement rate of 10 minutes (just an advertising agent), 10 seconds

Hello Barbie (2 star rating on Amazon, plus), your users will be offended! suggested that Mariya become a clothing designer. 
