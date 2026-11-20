What is Langchain?
Open Source Framework that simplifies the process of building LLM powered applications. provides tools and abstractions that allows us to create complex llm-powered applications

Lets say we want to build an app on top of a powerful LLM like claude and combine it with personal data and save history and change to another LLM and make an API call. It invovles many moving parts and thats where langchain comes in.

One way is that it abstracts the concept of interacting with teh LLM and through chat models we can switch them

ex: from langchain_anthropic import ChatAnthropic
    llm = ChatAnthropic(model="claude-3-opus-2...")

    result = llm.invoke("tell me a joke about programming")

prompts: helps with prompt management, optimization and prompt serialization. you can create a template from the prompt and dynamucally inject your user into your template

ex:
from langchain_core.prompt import PromptTemplate
prompt_template = PromptTemplate.from_template("tell me a joke about {topic}")

prompt_template.invoke({"Topic": "cats"})

document loader as well.



UV is a very fast python package manager built on RUST


Model are conversational so: System message -> 1. Humanmessage, AImessage, 2. Humanmessage, AImessage, toolmessage,.....