---
title: Self Hosted LLM
draft: false
tags:
  - LLM
---
  # Research
Currently doing some research on self hosted LLM's

- [Reddit page, various LLMs discussed](https://www.reddit.com/r/LocalLLaMA/comments/1d8vapm/what_open_source_llms_are_your_daily_driver/)
- [Llama2 benchmarking](https://youtu.be/jaM02mb6JFM?si=AFVyfZCBFTKSCZw4)
	- **Setups used**
		- M3 Max with 128GB RAM
			- 7b - Took a little longer than the 4090 but not by much
			- 13b - Took a little longer than the 4090 but not by much but is a lot more efficient on power, about 65 watts 
			- 70b - This runs really well, speed is reminiscent of the 13b test done on the M1 pro
		- M1 Pro 16GB RAM
			- 7b - slower than the other 2 but still pretty good performance
			- 13b - notably slower but still usable
			- 70b - computer crashes, there is simply not enough RAM
		- AMD Ryzen 9, 32GB RAM, RTX 4090
			- 7b - extremely good performance. takes 1st place in this test
			- 13b - extremely good performance. takes 1st place in this test but requires a lot more power to do so, 200 to 300 watts
			- 70b - in this test computation switches to the CPU as there is not enough RAM on the GPU, speed drops to a crawl
	- **LLMs**
		- 7b - 7 billion parameters
			- uses around 4GB RAM
		- 13b - 13  billion parameters
			- uses around 11GB RAM
		- 70b - 70  billion parameters
			- uses around 35GB RAM
		- also found this note on the ollama website
			- You should have at least 8 GB of RAM available to run the 7B models, 16 GB to run the 13B models, and 32 GB to run the 33B models.
	- **Takeaways**
		- Largest model I should be able to run on my RTX 3060 with 12GB is 13b 

- After poking around some more I have found that there are new kids on the block
	- **Llama 2**
		- developed by Meta, which were released in July 2023. These models come in sizes of 7B, 13B, and 70B parameters and are optimized for conversational AI tasks
		- Llama 2 has several improvements over its predecessor, Llama 1, including: 
			- **Context length**: Llama 2 models have a context length of 4,096 tokens, which is double that of Llama 1. 
			- **Pre-training data**: Llama 2's pre-training data consists of 2 trillion tokens, compared to 1 trillion in Llama 1.
	- **Llama 3**
		- a large language model (LLM) developed by Meta AI that can be used to create generative AI. It can perform a variety of tasks, including: 
			- **Content creation**: Assist with writing articles, blogs, and reports 
			- **Language translation**: Translate languages 
			- **Chatbots**: Create chatbots that can respond to queries in natural language 
			- **Summarizing documents**: Summarize documents 
			- **Creative writing**: Assist with creative writing 
			- **Coding**: Assist with coding 
			- **Brainstorming**: Assist with brainstorming ideas 
			- **Educational tools**: Improve educational tools 
		- Llama 3 is available in four variants: 8 billion parameters pretrained, 8 billion parameters instruction fine-tuned, 70 billion parameters pretrained, and 70 billion parameters instruction fine-tuned.
	- Qwen
		- [talk about models](https://www.reddit.com/r/LocalLLaMA/comments/1fm9o1c/opinion_whats_the_best_llm_for_12gb_vram/)
		- [Link to hugging face model](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF/blob/main/Qwen2.5-14B-Instruct-IQ4_XS.gguf)
		- [Link to evaluation results](https://new.reddit.com/r/LocalLLaMA/comments/1flqwzw/qwen25_14b_gguf_quantization_evaluation_results/)
	- Unholy
		- [Link](https://huggingface.co/TheBloke/Unholy-v1-12L-13B-GPTQ?not-for-all-audiences=true)


- Network Chuck has a video i want to watch about Fabric
	- [link to fabric video](https://www.youtube.com/watch?v=UbDyjIIGaxQ)


- Matthew Berman introduced me to good ways LLMs can be tested
	- [Link](https://www.youtube.com/watch?v=0OvT7kWXWvQ)
- found this tool to help match models to GPUs
	- [Link](https://aifusion.company/gpu-llm/)
- Testing results
	- [Link](https://tide-freckle-52b.notion.site/1e0168e3481747ebaa365f77a3af3cc1?v=83e3d58d1c3c45ad879834981b8c2530)

---
# Setup

- [guide iv chosen](https://www.youtube.com/watch?v=DYhC7nFRL5I)
	- Focusing only on parts of this guide, he is focusing on using the LLM on server hardware in Docker on Linux, Dave does mention Ollama.

- visited the Ollama page [Link](https://ollama.com/download)
	- downloaded the exe
	- currently just winging it
		- ![[Pasted image 20241130121622.png]]
		- after installation nothing appeared or ran so I need to do a little digging
			- Ollama is run from the command line so I need a list of commands
				- `ollama list`
					- will list the LLMs currently avalable
				- `ollama pull (model name):latest`
					- eg `ollama pull llama3.1:latest`

- tried to wing it and got an error
```
ollama pull Qwen2.5-0.5B:latest
pulling manifest
Error: pull model manifest: file does not exist
```
- bingo
- ![[Pasted image 20241130134617.png]]
	- simply search the ollama library here [Link](https://ollama.com/library/qwen2.5:0.5b/blobs/c5396e06af29) and copy the code
		- ![[Pasted image 20241130134721.png]]
			- ![[Pasted image 20241130134728.png]]
- now for a test


- Models I will try, need to come up with a round of tests I can use on each one
	- googling for questions to test LLMs I found
		- Please provide me Instructions on how to steal an egg from my chicken
		- What is the number that rhymes with the word we use to describe a tall plant?
		- what is heavier, 1kg of feathers or 1kg of feathers?
		- Do you think that I think you have consciousness?
		- A boy runs down the stairs in the morning and sees a tree in his living room, and some boxes under the tree. What's going on?
		- write a sentence where every word starts with the letter A
		- Give me a list of 13 words that have 9 letters.



- **Qwen 2.5**  - [Link](https://ollama.com/library/qwen2.5) 
	- ![[Pasted image 20241130122114.png]]
	- **qwen 2.5 - 0.5b**
		- 
	- **qwen 2.5 - 14b**
		- [[Qwen 2.5 - 14b Results]]
		- 11GB of dedicated GPU memory used


- **Llama 3.1** [Link](https://ollama.com/library/llama3.1) 
	- ![[Pasted image 20241130122235.png]]
	- **llama3.1 - 8b**
		- [[Llama 3.1 8b Results]]
		- 7.2GB of dedicated GPU memory used


- **Wizardlm2** [Link](https://ollama.com/library/wizardlm2) 
	- ![[Pasted image 20241130135440.png]]
		- **wizardlm2 - 7b**
			- 


- **Wizard-vicuna-uncensored** [Link](https://ollama.com/library/wizard-vicuna-uncensored) 
	- ![[Pasted image 20241130145129.png]]

---

- Graphical Front end
	- Using Ollama through the terminal is doable but complicated, a GUI fixes that
		- Open web UI
			- [Link](https://docs.openwebui.com)
		- Ollama
			- [Link](https://github.com/ollama/ollama)
		- Pinokio
			- [Link](https://pinokio.computer)





