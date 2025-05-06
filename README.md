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

### Test with UI

You can simply run the gradio example:

```
uv pip install gradio
```

```bash
python examples/ui/gradio_demo.py
```

# Vision

Tell your computer what to do, and it gets it done.

## Roadmap

- [ ] Improve memory management
- [ ] Enhance planning capabilities
- [ ] Improve self-correction
- [ ] Fine-tune the model for better performance
- [ ] Create datasets for complex tasks
- [ ] Sandbox browser-use for specific websites
- [ ] Implement deterministic script rerun with LLM fallback
- [ ] Cloud-hosted version
- [ ] Add stop/pause functionality
- [ ] Improve authentication handling
- [ ] Reduce token consumption
- [ ] Implement long-term memory
- [ ] Handle repetitive tasks reliably
- [ ] Third-party integrations (Slack, etc.)
- [ ] Include more interactive elements
- [ ] Human-in-the-loop execution
- [ ] Benchmark various models against each other
- [ ] Let the user record a workflow and browser-use will execute it
- [ ] Improve the generated GIF quality
- [ ] Create various demos for tutorial execution, job application, QA testing, social media, etc.


<div align="center">
Made with ❤️ by the Nuvio Team
 </div> 
