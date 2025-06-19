# ChatGPT Clone

A simple command-line chatbot built with Python that uses OpenAI's GPT-3.5-turbo model to provide conversational AI responses.

## Features

- Interactive command-line interface
- Powered by OpenAI's GPT-3.5-turbo model
- Continuous conversation loop
- Simple and clean response formatting

## Prerequisites

- Python 3.11+
- OpenAI API key

## Setup

### 1. Get OpenAI API Key

1. Visit [OpenAI Platform](https://platform.openai.com/signup)
2. Create an account or sign in
3. Navigate to "View API Keys" from the top right menu
4. Click "Create new secret key"
5. Copy your API key

### 2. Configure Environment

1. In your Replit project, open the Secrets tool (lock icon in the sidebar)
2. Add a new secret:
   - Key: `OPENAI_API_KEY`
   - Value: Your OpenAI API key

### 3. Install Dependencies

The project uses Poetry for dependency management. Dependencies will be automatically installed when you run the project.

Required packages:
- `openai` - OpenAI Python client library
- `boltiotai` - Bolt IoT AI integration

## Usage

1. Click the "Run" button in Replit, or run:
   ```bash
   python main.py
   ```

2. When prompted, enter your question or instruction:
   ```
   Question: what is your question/instruction?
   ```

3. The AI will respond, and you can continue the conversation:
   ```
   Question: your next question/instruction?
   ```

4. The conversation continues indefinitely until you stop the program.

## Example Interaction

```
Question: what is your question/instruction?
Tell me about Python programming

Ans Python is a high-level, interpreted programming language known for its simplicity and readability. It's widely used for web development, data science, artificial intelligence, and automation.

Question: your next question/instruction?
What can I build with Python?

Ans With Python, you can build web applications, data analysis tools, machine learning models, automation scripts, desktop applications, games, and much more!
```

## Code Structure

- `main.py` - Main application file containing the chatbot logic
- `pyproject.toml` - Poetry configuration and dependencies
- `.replit` - Replit configuration file

## How It Works

1. The program initializes by requesting the first question from the user
2. It checks for the OpenAI API key in environment variables
3. Creates a chat completion request to OpenAI's GPT-3.5-turbo model
4. Displays the AI's response
5. Prompts for the next question and repeats the process

## Troubleshooting

### API Key Issues
If you see an error about the API key:
- Ensure you've added `OPENAI_API_KEY` to your Replit Secrets
- Verify your API key is valid and has available credits
- Check that the key is correctly copied without extra spaces

### Model Access
- Make sure your OpenAI account has access to GPT-3.5-turbo
- Verify you have sufficient API credits

## Customization

You can modify the system message in `main.py` to change the AI's behavior:

```python
"content": "You are a helpful assistant."
```

Change this to customize the AI's personality or expertise area.

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to fork this project and submit pull requests for improvements!
