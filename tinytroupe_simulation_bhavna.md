# TinyTroupe Simulation Report - Bhavna

## 1. Cloning and installing the TinyTroupe package

```bash
git clone https://github.com/microsoft/tinytroupe
cd tinytroupe
pip install .
```

## 2. Importing the OPENAI API Key

```bash
export OPENAI_API_KEY="enter api key"
```

## 3. Starting Python

```bash
python
```

## 4. Creating 1st persona

```python
from tinytroupe.agent import TinyPerson

bhavna = TinyPerson("Bhavna")
bhavna.define("age", 25)
bhavna.define("nationality", "Indian")
bhavna.define("occupation", "MS. in Data Science student at Pace University")

```

## 5. Creating 2nd Persona

```python
from tinytroupe.agent import TinyPerson

yiqiao = TinyPerson("Yiqiao")
yiqiao.define("age", 30)
yiqiao.define("nationality", "Chinese")
yiqiao.define("occupation", "He is a professor at Pace university.")
yiqiao.define("skills", ["Python", "Data Science", "Machine Learning", "SQL", "Deep Learning", "Computer Vision", "Neural Networks", "Cloud Computing", "NLP (Natural Language Processing)"])
```

## 6. Observing a conversation between two personas

```python
from tinytroupe.environment import TinyWorld

world = TinyWorld("Classroom", [yiqiao, bhavna])
world.make_everyone_accessible()
yiqiao.listen("I want to extend my deadline on the project assigned.")
world.run(3)
```

### Output (Transcript):

```text
────────────────────────────────────────────────────────────── Classroom step 1 of 3 ──────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > The person wants to extend their project deadline. I need to consider how to respond
            > to this request and whether it's reasonable or not.
Yiqiao acts: [TALK] 
            > Could you please provide more details about why you need to extend the deadline? It
            > would help me understand your situation better.
Yiqiao acts: [DONE] 

Yiqiao --> Bhavna: [CONVERSATION] 
            > Could you please provide more details about why you need to extend the deadline? It
            > would help me understand your situation better.
Bhavna acts: [THINK] 
         > Yiqiao is asking for more details about the deadline extension. I need to explain my
         > reasons clearly and concisely to help them understand my situation better.
Bhavna acts: [TALK] 
         > I appreciate your willingness to understand my situation better. The reason I need to
         > extend the deadline is that I've encountered some unexpected challenges with my project
         > that have set me back. I want to ensure that I can deliver quality work, and a little
         > more time would really help me achieve that.
Bhavna acts: [DONE] 

Bhavna --> Yiqiao: [CONVERSATION] 
         > I appreciate your willingness to understand my situation better. The reason I need to
         > extend the deadline is that I've encountered some unexpected challenges with my project
         > that have set me back. I want to ensure that I can deliver quality work, and a little
         > more time would really help me achieve that.
────────────────────────────────────────────────────────────── Classroom step 2 of 3 ──────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > Bhavna has encountered unexpected challenges and needs more time to ensure quality work.
            > This is a reasonable request, and I should consider granting the extension.
Yiqiao acts: [TALK] 
            > Thank you for explaining your situation, Bhavna. I understand that unexpected challenges
            > can arise. How much additional time do you think you would need to complete the project?
Yiqiao acts: [DONE] 

Yiqiao --> Bhavna: [CONVERSATION] 
            > Thank you for explaining your situation, Bhavna. I understand that unexpected challenges
            > can arise. How much additional time do you think you would need to complete the project?
Bhavna acts: [THINK] 
         > Yiqiao is understanding about my situation, which is good. I need to consider how much
         > additional time I would realistically need to complete the project. I think an extra week
         > should be sufficient to address the challenges I faced and ensure the quality of my work.
Bhavna acts: [TALK] 
         > Thank you for your understanding, Yiqiao. I believe that an additional week would be
         > sufficient for me to complete the project. This will give me the time I need to address
         > the challenges I've encountered and ensure that I deliver quality work.
Bhavna acts: [DONE] 

Bhavna --> Yiqiao: [CONVERSATION] 
         > Thank you for your understanding, Yiqiao. I believe that an additional week would be
         > sufficient for me to complete the project. This will give me the time I need to address
         > the challenges I've encountered and ensure that I deliver quality work.
────────────────────────────────────────────────────────────── Classroom step 3 of 3 ──────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > Bhavna believes that an additional week will be sufficient to complete the project. This
            > seems reasonable, and I should consider granting the extension.
Yiqiao acts: [TALK] 
            > I can grant you the additional week for the project. I appreciate your commitment to
            > delivering quality work. Please let me know if you need any further assistance during
            > this time.
Yiqiao acts: [DONE] 

Yiqiao --> Bhavna: [CONVERSATION] 
            > I can grant you the additional week for the project. I appreciate your commitment to
            > delivering quality work. Please let me know if you need any further assistance during
            > this time.
Bhavna acts: [THINK] 
         > Yiqiao has granted me the additional week for the project, which is a relief. I should
         > express my gratitude and also consider if I need any assistance during this time.
Bhavna acts: [TALK] 
         > Thank you so much for granting me the additional week, Yiqiao. I really appreciate your
         > understanding and support. I will definitely reach out if I need any further assistance
         > during this time.
Bhavna acts: [DONE] 

Bhavna --> Yiqiao: [CONVERSATION] 
         > Thank you so much for granting me the additional week, Yiqiao. I really appreciate your
         > understanding and support. I will definitely reach out if I need any further assistance
         > during this time.
```

---

## 7. Turing Test Thoughts

I think that this conversation between these two bots has passed the Turing Test.

**Reasons:**

- The flow of the conversation felt very natural and coherent.
- The way both personas responded felt human — especially with empathy and clarity.
- It mirrors real-life communication between a student and a professor, both in tone and content.
