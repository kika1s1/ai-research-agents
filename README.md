# AI Research Agents

## Overview

The **AI Research Agents** project is a research assistance tool designed to generate structured research outputs. The tool leverages multiple tools including web search (DuckDuckGo), Wikipedia querying, and text file storage. It is built using the LangChain framework and integrates with both OpenAI and Anthropic LLMs.

## Features

- **Web Search Integration:** Uses DuckDuckGo to search for relevant information.
- **Wikipedia Query:** Fetches summarized information from Wikipedia.
- **Structured Output:** Generates research outputs in a specified Pydantic format.
- **Data Storage:** Saves the generated research output to a text file with timestamps.
- **Environment Configurations:** Easily configurable via a `.env` file for API credentials.

## Project Structure

- **main.py:** The main entry point for the application. It sets up the LangChain agent using the provided tools and handles the research query.
- **tools.py:** Contains the definitions for various tools including the search, Wikipedia query, and file saving functions.
- **requirements.txt:** Lists all Python dependencies.
- **.env:** Used for storing sensitive API keys and configuration settings.
- **.vscode/settings.json:** VS Code specific settings to enable GitHub Copilot for the project.

## Setup

1. **Clone the Repository:**

   ```sh
   git clone https://github.com/kika1s1/ai-research-agents.git
   cd ai-research-agents
   ```

2. **Create a Virtual Environment and Activate:**

   ```sh
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install Dependencies:**

   ```sh
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables:**

   Update the `.env` file with your API keys. For example, set the `openai_api_key` and optionally the `anthropic_api_key`.

## Usage

Run the main application using:

```sh
python main.py
```

When prompted, enter a research query. The application will process your input, perform the required searches, and output a structured research response, as well as saving the output to a file named `research_output.txt`.

## Customization

- **LLM Models:** By default, the project uses the Anthropic LLM (Claude-3-5 Sonnet). You can customize or switch to an OpenAI model by modifying the initialization in `main.py`.
- **Tools:** Additional tools can be integrated by updating the `tools.py` file.
- **Output Format:** The research output is defined using the `ResearchResponse` Pydantic model in `main.py`. You can modify the structure as needed.

## Contribution

Feel free to fork the repository and submit pull requests with improvements and new features. Please adhere to the project's coding standards and ensure that all tests pass.

## License



Distributed under the MIT License. See [LICENSE](LICENSE) for more information.Distributed under the MIT License. See [LICENSE](LICENSE) for more information.
