# AI Debate Simulation System

This project simulates a debate between two AI agents on the future of work in an era of artificial intelligence. One agent argues that AI will replace most human jobs, while the other maintains that AI will primarily enhance human development. A third agent, the moderator, evaluates the debate and determines which side presented a stronger argument.

## Features

* Automates debates between AI agents using OpenAI’s language model.
* Posts debates to specified Reddit subreddits using PRAW (Python Reddit API Wrapper).
* Simulates a back-and-forth exchange with customizable turn count and temperature.
* Includes a moderator LLM to summarize and determine a winner.
* Built-in logging via printed outputs and Reddit threads.

## Requirements

* Python 3.8+
* Reddit API credentials (via PRAW)
* OpenAI API key
* `.env` file to store secrets securely

## Setup

1. Clone this repository.

2. Create a `.env` file in the root directory with the following variables:

   ```env
   OPENAI_API_KEY=your_openai_api_key
   REDDIT_CLIENT_ID=your_reddit_client_id
   REDDIT_CLIENT_SECRET=your_reddit_client_secret
   REDDIT_USERNAME=your_reddit_username
   REDDIT_PASSWORD=your_reddit_password
   REDDIT_USER_AGENT=your_custom_user_agent
   ```

3. Install required Python packages:

   ```bash
   pip install requirements.txt
   ```

4. Optionally, update the `SUBREDDITS` dictionary to map temperatures to desired subreddit names.

## Running the Simulation

To run the debate simulation and post it to Reddit:

```bash
python ai_debate_simulation.py
```

This will:

* Start a debate between two agents
* Alternate turns using OpenAI’s language model
* Post replies as comments to a Reddit thread
* Have a third AI agent (moderator) summarize the debate and declare a winner

## Customization

You can customize:

* The number of turns in the debate
* The temperature (randomness) of the language model
* The initial debate prompt
* Subreddits used for posting

Modify the `simulate_and_post_debate()` parameters or the `SUBREDDITS` dictionary to fit your use case.

## Example Output

Each debate is structured as:

* A post on Reddit with a title and description
* Sequential comments from each AI agent
* A final moderator comment summarizing and evaluating the discussion
