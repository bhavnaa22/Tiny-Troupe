TinyTroupe Simulation Assignment

 1. How to install TinyTroupe packages?
To install the TinyTroupe package, follow these steps:

```bash
git clone https://github.com/microsoft/tinytroupe
cd tinytroupe
pip install .
```

 2. What is the Turing Test? What does it mean in the age of LLMs?
The Turing Test was proposed by Alan Turing in 1950 as a way to measure a machine's ability to exhibit intelligent behavior equivalent to, or indistinguishable from, that of a human.

In the age of **Large Language Models (LLMs)** like GPT-4, the Turing Test has evolved. Rather than just "fooling" someone into thinking it's human, an LLM's ability to:
- Understand complex prompts
- Respond with empathy or logic
- Mimic real human dialogue

...can blur the lines between human and machine more than ever before. The bar for passing the Turing Test now includes 
emotional intelligence, contextual awareness, and linguistic nuance.

---

 3. Custom Simulation: Bhavna and Professor Yiqiao

 Setup:
```python
from tinytroupe.agent import TinyPerson
from tinytroupe.environment import TinyWorld

bhavna = TinyPerson("Bhavna")
bhavna.define("age", 25)
bhavna.define("nationality","Indian")
bhavna.define("occupation","Data Science student at Pace University")
bhavna.define("quirks","Spiritually identifies as a cat and loves using humor to pretend she’s fine.")

yiqiao = TinyPerson("Yiqiao")
yiqiao.define("age", 35)
yiqiao.define("nationality", "Chinese")
yiqiao.define("occupation", "He is a professor at Pace university.")

world = TinyWorld("Classroom", [yiqiao, bhavna])
world.make_everyone_accessible()

yiqiao.listen("I want to extend my deadline on the project assigned.")
world.run(3)
```

---

 Transcript:

```
USER --> Yiqiao: [CONVERSATION]
          > I want to extend my deadline on the project assigned.
TinyPerson(name='Yiqiao')

─────────────────────────────────────────────────────────────── Classroom step 1 of 3 ────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK]
            > Bhavna wants to extend her project deadline. I need to consider if her request is valid and how to respond.
Yiqiao acts: [TALK]
            > Can you tell me what's going on, Bhavna? I want to make sure you're okay before we discuss the extension.
Yiqiao acts: [DONE]

Yiqiao --> Bhavna: [CONVERSATION]
            > Can you tell me what's going on, Bhavna? I want to make sure you're okay before we discuss the extension.

Bhavna acts: [THINK]
         > Yiqiao seems genuinely concerned. I should be honest but keep it together.
Bhavna acts: [TALK]
         > Honestly, it's been a rough week. I have been juggling assignments, lack of sleep, and existential dread. I want to do a good job, but I need a bit more time.
Bhavna acts: [DONE]

Bhavna --> Yiqiao: [CONVERSATION]
         > Honestly, it's been a rough week. I have been juggling assignments, lack of sleep, and existential dread. I want to do a good job, but I need a bit more time.

─────────────────────────────────────────────────────────────── Classroom step 2 of 3 ────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK]
            > Bhavna sounds overwhelmed but motivated. I should be supportive but set some boundaries.
Yiqiao acts: [TALK]
            > I appreciate your honesty, Bhavna. Mental health is important. How much more time do you need?
Yiqiao acts: [DONE]

Yiqiao --> Bhavna: [CONVERSATION]
            > I appreciate your honesty, Bhavna. Mental health is important. How much more time do you need?

Bhavna acts: [THINK]
         > He actually gets it. Let's not push it too far. One week sounds fair.
Bhavna acts: [TALK]
         > Just one more week would help a lot. I promise I won’t push it further.
Bhavna acts: [DONE]

Bhavna --> Yiqiao: [CONVERSATION]
         > Just one more week would help a lot. I promise I won’t push it further.

─────────────────────────────────────────────────────────────── Classroom step 3 of 3 ────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK]
            > A one-week extension is reasonable. Bhavna is sincere and responsible.
Yiqiao acts: [TALK]
            > You got it. One week extension granted. Take care of yourself and stay in touch.
Yiqiao acts: [DONE]

Yiqiao --> Bhavna: [CONVERSATION]
            > You got it. One week extension granted. Take care of yourself and stay in touch.

Bhavna acts: [THINK]
         > Okay now I’m lowkey emotional. That was so kind.
Bhavna acts: [TALK]
         > Thank you, Yiqiao. You’re the best. I’ll submit something amazing. Pinky promise.
Bhavna acts: [DONE]

Bhavna --> Yiqiao: [CONVERSATION]
         > Thank you, Yiqiao. You’re the best. I’ll submit something amazing. Pinky promise.
```

---

 My Thoughts: Did the bots pass the Turing Test?
Yes. Here's why:

- The emotional flow of the conversation felt natural.
- Both personas responded with empathy, humor, and realistic logic.
- The pacing and tone were indistinguishable from a real conversation between a stressed student and a compassionate professor.

Conclusion: If I didn’t know these were bots, I’d assume this was copied from a real chat. So yes, the Turing Test is passed.



