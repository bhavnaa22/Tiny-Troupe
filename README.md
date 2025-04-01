# Tiny-Troupe
This project showcases a simulation using the tinytroupe package as part of an experiment exploring conversational agents and the Turing Test.
Setup Instructions

Step 1: Install Packages

git clone https://github.com/microsoft/tinytroupe
cd tinytroupe
pip install .

Step 2: Setup API Key

export OPENAI_API_KEY="your_openai_key_here"

Step 3: Run Simulation

Run a conversation between two personas (Bhavna and Yiqiao) by executing:

from tinytroupe.agent import TinyPerson
from tinytroupe.environment import TinyWorld

# Define personas
bhavna = TinyPerson("Bhavna")
bhavna.define("age", 25)
bhavna.define("nationality", "Indian")
bhavna.define("occupation", "Graduate student in Data Science")

yiqiao = TinyPerson("Yiqiao")
yiqiao.define("age", 35)
yiqiao.define("nationality", "Chinese")
yiqiao.define("occupation", "Professor at a university")

# Create world and run simulation
world = TinyWorld("Classroom", [yiqiao, bhavna])
world.make_everyone_accessible()
bhavna.listen("I want to extend my homework.")
world.run(3)

Simulation Transcript

See bhavna_simulation_output.md for the full transcript.

Turing Test Reflection

Based on the interactions in the transcript, the personas demonstrated realistic, context-aware behavior, which suggests a pass on the Turing Test from a qualitative perspective.
