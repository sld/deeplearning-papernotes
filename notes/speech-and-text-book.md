- Ссылка на книгу: https://web.stanford.edu/~jurafsky/slp3/
главы Dialog Systems and Chatbots и Advanced Dialog Systems


# Интересные моменты

**PARRY - первый чатбот прошедший Тест Тьюринга:**

- Psychiatrists couldn’t distinguish text transcripts of interviews
with PARRY from transcripts of interviews with real paranoids (Colby et al., 1972).


**Commercial implementations of the IR-based approach** include Cleverbot (Carpenter, 2017)
and Microsoft’s ’XioaIce’ (Little Bing 小冰) system (Microsoft, ).

**Another paradigm is adversarial evaluation** (Bowman et al. 2016, Kannan and Vinyals 2016,
Li et al. 2017), inspired by the Turing test. The idea is to train a
“Turing-like” evaluator classifier to distinguish between human-generated
responses and machine-generated responses. The more successful a response
generation system is at fooling this evaluator, the better the system.

- frame-based skill (semantic parsing, slot filling), iob-разметка, example: voiceXML lib.
- Iteratively test the design on users

Asking questions, giving orders, or making informational statements are things
that people do in conversation, yet dealing with these kind of actions in
dialogue—what we will call **dialog acts**— is something that the GUS-style frame-
based dialog systems of Chapter 29 are completely incapable of.

The system needs a **dialog policy** to decide what to say
(when to answer the user’s questions, when to instead ask the user a
clarification question, make a suggestion, and so on).

**Principle of closure.** Agents performing an action require evidence, sufficient
for current purposes, that they have succeeded in performing it. Grounding is
also important when the hearer needs to indicate that the speaker has not
succeeded. If the hearer has problems in understanding, she must indicate these
problems to the speaker, again so that mutual understanding can eventually be
achieved.


The ideas of speech acts and grounding are combined in a single kind of action
called a dialog act, a tag which represents the interactive function of the
sentence being tagged. **Different types of dialog systems require labeling different kinds of acts**,
and so the tagset—defining what a dialog act is
exactly— tends to be designed for particular tasks.

Dialog acts don’t just appear discretely and independently; conversations have
structure, and dialogue acts reflect some of that structure. One aspect of this
structure comes from the field of **conversational analysis or CA** (Sacks et al.,
1974) which focuses on interactional properties of human conversation. CA
defines ad- jacency pairs (Schegloff, 1968) as a pairing of two dialog acts,
like QUESTIONS and ANSWERS, PROPOSAL and ACCEPTANCE (or REJECTION), COMPLIMENTS
and DOWNPLAYERS, GREETING and GREETING.

**The goal of the dialog policy** at turn i in the conversation is to predict which
action Ai to take, based on the entire dialog state. The state could mean the
entire sequence of dialog acts from the system (A) and from the user (U), in
which case the task would be to compute

Once a dialog act has been decided, we need to generate the text of the response
to the user. The task of **natural language generation (NLG)** in the information-
state architecture is often modeled in two stages, **content planning (what to say), and sentence realization (how to say it).**

The policy we described in Section 30.4, deciding what actions the system should
take based just on the current filled slots and the users last utterance, has a
problem: it looks only at the past of the dialog, completely ignoring whether
the action we take is likely to lead to a successful outcome (a correctly booked
flight or filled-in calendar). But we can’t know whether the outcome is
successful until long after the current utterance we are trying to plan.
**Reinforcement learning is the branch of machine learning that deals with models that learn to maximize future rewards.** This is an extremely active area of
research, so we give here just the simplest intuition for this direction, based
on an oversimplified model of dialog as a **Markov decision process.**

The MDP is only useful in small toy examples and is not used in practical dialog
systems. A more powerful model, the partially observable Markov decision
process, or **POMDP**, adds extra latent variables to represent our uncertainty
about the true state of the dialog. **Both MDPs and POMDPs, however, have problems**
due to computational complexity and due to **their reliance on simulations** that
don’t reflect true user behavior.

