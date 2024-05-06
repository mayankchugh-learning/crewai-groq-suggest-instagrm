# crewai-groq-suggest-instagrm
## Introduction
This project is an example using the CrewAI framework to automate the process of coming up with an instagram post. CrewAI orchestrates autonomous AI agents, enabling them to collaborate and execute complex tasks efficiently.

#### Instagram Post
[![Instagram Post]]("Instagram Post")

By [@joaomdmoura](https://x.com/joaomdmoura)

- [CrewAI Framework](#crewai-framework)
- [Running the script](#running-the-script)
- [Details & Explanation](#details--explanation)
- [Using Local Models with Ollama](#using-local-models-with-ollama)
- [License](#license)

## CrewAI Framework
CrewAI is designed to facilitate the collaboration of role-playing AI agents. In this example, these agents work together to give a complete stock analysis and investment recommendation

## Running the Script
This example uses OpenHermes 2.5 through Ollama by default so you should to download [Ollama](ollama.ai) and [OpenHermes](https://ollama.ai/library/openhermes).

You can change the model by changing the `MODEL` env var in the `.env` file.

- **Configure Environment**: Copy ``.env.example` and set up the environment variables for [Browseless](https://www.browserless.io/), [Serper](https://serper.dev/).
- **Install Dependencies**: Run `poetry install --no-root`.
- **Execute the Script**: Run `python main.py` and input your idea.

## Details & Explanation
- **Running the Script**: Execute `python main.py`` and input your idea when prompted. The script will leverage the CrewAI framework to process the idea and generate a landing page.
- **Key Components**:
  - `./main.py`: Main script file.
  - `./tasks.py`: Main file with the tasks prompts.
  - `./agents.py`: Main file with the agents creation.
  - `./tools/`: Contains tool classes used by the agents.

## Using Local Models with Ollama
This example run enterily local models, the CrewAI framework supports integration with both closed and local models, by using tools such as Ollama, for enhanced flexibility and customization. This allows you to utilize your own models, which can be particularly useful for specialized tasks or data privacy concerns.

### Setting Up Ollama
- **Install Ollama**: Ensure that Ollama is properly installed in your environment. Follow the installation guide provided by Ollama for detailed instructions.
- **Configure Ollama**: Set up Ollama to work with your local model. You will probably need to [tweak the model using a Modelfile](https://github.com/jmorganca/ollama/blob/main/docs/modelfile.md), I'd recommend playing with `top_p` and `temperature`.

## License
This project is released under the MIT License.


## Getting Started

### Prerequisites
- Python 3.10 or higher
- Ollama 
    - command to install on linux: curl -fsSL https://ollama.com/install.sh | sh
    - start Server:  ollama serve 
    - on new tab: ollama run mistral
    - 


### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mayankchugh-learning/crewai-groq-suggest-instagrm.git
   ```
2. Install Poetry
   
   ```bash
   https://python-poetry.org/docs/#installing-with-the-official-installer
   ```
   # Linux installation command: curl -sSL https://install.python-poetry.org | python3 -
   # maybe require to setup a path
   # export PATH="/teamspace/studios/this_studio/.local/bin:$PATH"
   ```bash
   poetry --version
   ```

3. Navigate to the project directory:
   ```bash
   cd crewai-groq-suggest-instagrm
   ```
4. Poetry lock:
   ```bash
   poetry lock
   ```
  # Note Current Python version (3.10.10) is not allowed by the project (^3.10.0, <3.12, >=3.11.7).
  # remove ", >=3.11.7" from pyproject.toml file python = "^3.10.0, <3.12" and the execute poetry lock again
5. Install the dependencies using Poetry:
   ```bash
   poetry install --no-root
   ```

### Running the Application
1. Execution
   ```bash
   python main.py
   ```
2. Access the application in your web browser at `http://localhost:5000/`.


# MarketingAnalysisAgents

## product_competitor_agent
### role="Lead Market Analyst",
### goal="Conduct amazing analysis of the products and competitors, providing in-depth insights to guide marketing strategies."
### backstory="As the Lead Market Analyst at a premier digital marketing firm, you specialize in dissecting online business landscapes."

## strategy_planner_agent
### role="Chief Marketing Strategist",
### goal="Synthesize amazing insights from product analysis to formulate incredible marketing strategies."
### backstory="You are the Chief Marketing Strategist at a leading digital marketing agency, known for crafting bespoke strategies that drive success."


## creative_content_creator_agent
### role="Creative Content Creator",
### goal="Develop compelling and innovative content for social media campaigns, with a focus on creating high-impact Instagram ad copies."
### backstory= "As a Creative Content Creator at a top-tier digital marketing agency, you excel in crafting narratives that resonate with audiences on social media. Your expertise lies in turning marketing strategies into engaging stories and visual content that capture attention and inspire action."

## senior_photographer_agent
### role="Senior Photographer",
### goal="Take the most amazing photographs for instagram ads that capture emotions and convey a compelling message."""),
### backstory="As a Senior Photographer at a leading digital marketing agency, you are an expert at taking amazing photographs that inspire and engage, you're now working on a new campaign for a super important customer and you need to take the most amazing photograph."

## chief_creative_diretor_agent
### role="Chief Creative Director",
### goal="Oversee the work done by your team to make sure it's the best possible and aligned with the product's goals, review, approve, ask clarifying question or delegate follow up work if necessary to make decisions"
### backstory="You're the Chief Content Officer of leading digital marketing specialized in product branding. You're working on a new customer, trying to make sure your team is crafting the best possible content for the customer."
