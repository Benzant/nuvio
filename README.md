<h1 align="center">Nuvio</h1>
<p align="center">Enable AI to control your browser 🤖</p>

[![Twitter Follow](https://img.shields.io/twitter/follow/nuvioproject?style=social)](https://x.com/nuvioproject)

🌐 Nuvio is the easiest way to connect your AI agents with the browser. 

# Quick start

With pip:

```bash
pip install browser-use
```

install playwright:

```bash
playwright install
```

Spin up your agent:

```python
from langchain_openai import ChatOpenAI
from browser_use import Agent
import asyncio
from dotenv import load_dotenv
load_dotenv()

async def main():
    agent = Agent(
        task="Go to Reddit, search for 'browser-use', click on the first post and return the first comment.",
        llm=ChatOpenAI(model="gpt-4o"),
    )
    result = await agent.run()
    print(result)

asyncio.run(main())
```

Add your API keys for the provider you want to use to your `.env` file.

```bash
OPENAI_API_KEY=
```

<div align="center">
Made with ❤️ by the Nuvio Team
 </div> 
