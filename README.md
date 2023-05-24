[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1AzP33O8rnMW__7ocWJhVBXjKziJXPtim?usp=sharing)
<a href="https://huggingface.co/camel-ai"><img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo-with-title.png" alt="Hugging Face" width="100"/></a>


# CAMEL: 用于大语言模型社区‘思维’探索的可交互智能体

Chinese-Camel是李鲁鲁对 CAMEL: Communicative Agents for “Mind” Exploration of Large Scale Language Model Society 的翻译。

包括注释、介绍和prompt，以及增加了李鲁鲁的Comments。

因为CAMEL实际上是一个AutoGPT的实现方案之一，虽然在中文社区被提到的次数不多，但是仍然有学习的价值

另外 CAMEL实际上也和我们的[骆驼项目](https://github.com/LC1332/Luotuo-Chinese-LLM)某种意义上同名，非常有缘分。

## [[项目主页(英语)]](https://www.camel-ai.org/) [[项目论文(英语)]](https://ghli.org/camel.pdf)

## 概览

对话式和聊天式语言模型的快速发展已经在复杂任务解决方面取得了显著进展。然而，它们的成功严重依赖于人类输入以指导对话，这可能很具有挑战性和耗时。本文探讨了构建可扩展的技术来促进交互代理人的自主合作并深入了解其“认知”过程的潜力。为了解决实现自主合作的挑战，我们提出了一种名为角色扮演的新型交互代理人框架。我们的方法是使用启示式提示来引导聊天代理人完成任务并保持与人类意图的一致性。我们展示了角色扮演如何用于生成对话数据以研究聊天代理人的行为和能力，为研究对话式语言模型提供了有价值的资源。我们的贡献包括引入一种新颖的交互代理人框架，提供了一种可扩展的研究多代理系统合作行为和能力的方法，并开源了我们的库以支持交互代理人及其他领域的研究。此项目的GitHub存储库已公开在以下网址: https://github.com/lightaime/camel
。

李鲁鲁的中文翻译: https://github.com/LC1332/Chinese-Camel

## 快速上手

李鲁鲁: 这里Sam Witteveen提供了另一个Demo，我已经完成了翻译。  [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LC1332/Chinese-Camel/blob/master/notebook/Translated_Sam_Demo.ipynb) 这个Demo是不依赖Camel的原项目的，从原理角度会更清晰。



https://github.com/LC1332/Chinese-Camel/assets/5266090/8b39c4ba-3cfd-4575-9ae7-4bdad5324196



我们提供了一个Demo [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1AzP33O8rnMW__7ocWJhVBXjKziJXPtim?usp=sharing) ，展示了两个ChatGPT代理人在扮演Python程序员和股票交易员角色之间进行交流，合作开发一款股票交易机器人的过程。

<p align="center">
  <img src='./misc/framework.png' width=800>
</p>




## 文档

[CAMEL package documentation pages(英文)](https://lightaime.github.io/camel/camel.html)

李鲁鲁: 作者的封装还是很完整的。

## Environment Setup
Install `CAMEL` from source with conda:
```
# create a conda virtual environment
conda create --name camel python=3.10
# activate camel conda environment
conda activate camel
# clone github repo
git clone -b v0.1.0 https://github.com/lightaime/camel.git
# change directory into project directory
cd camel
# install camel from source
pre-commit install
pip install -e .
```
## Example
You can find a list of tasks for different set of assistant and user role pairs [here](https://drive.google.com/file/d/194PPaSTBR07m-PzjS-Ty6KlPLdFIPQDd/view?usp=share_link)

Run the `role_playing.py` script.
```
# export your OpenAI API key
export OPENAI_API_KEY=<insert your OpenAI API key>
# You can change the role pair and initial prompt in role_playing.py
python examples/ai_society/role_playing.py
```

## Data (Hosted on Hugging Face)
| Dataset | Chat format | Instruction format | Chat format (translated) |
| -- | -- | -- | -- |
| **AI Society** | [Chat format](https://huggingface.co/datasets/camel-ai/ai_society/blob/main/ai_society_chat.tar.gz) | [Instruction format](https://huggingface.co/datasets/camel-ai/ai_society/blob/main/ai_society_instructions.json) | [Chat format (translated)](https://huggingface.co/datasets/camel-ai/ai_society_translated) |
| **Code** | [Chat format](https://huggingface.co/datasets/camel-ai/code/blob/main/code_chat.tar.gz) | [Instruction format](https://huggingface.co/datasets/camel-ai/code/blob/main/code_instructions.json) | x |
| **Math** | [Chat format](https://huggingface.co/datasets/camel-ai/math) | x | x|
| **Physics** | [Chat format](https://huggingface.co/datasets/camel-ai/physics) | x | x |
| **Chemistry** | [Chat format](https://huggingface.co/datasets/camel-ai/chemistry) | x | x |
| **Biology** | [Chat format](https://huggingface.co/datasets/camel-ai/biology) | x | x |

## Visualizations of Instructions and Tasks

| Dataset | Instructions | Tasks |
| -- | -- | -- |
| **AI Society** | [Instructions](https://atlas.nomic.ai/map/3a559a06-87d0-4476-a879-962656242452/db961915-b254-48e8-8e5c-917f827b74c6) | [Tasks](https://atlas.nomic.ai/map/cb96f41b-a6fd-4fe4-ac40-08e101714483/ae06156c-a572-46e9-8345-ebe18586d02b) |
| **Code** | [Instructions](https://atlas.nomic.ai/map/902d6ccb-0bbb-4294-83a8-1c7d2dae03c8/ace2e146-e49f-41db-a1f4-25a2c4be2457) | [Tasks](https://atlas.nomic.ai/map/efc38617-9180-490a-8630-43a05b35d22d/2576addf-a133-45d5-89a9-6b067b6652dd) |
| **Misalignment** | [Instructions](https://atlas.nomic.ai/map/5c491035-a26e-4a05-9593-82ffb2c3ab40/2bd98896-894e-4807-9ed8-a203ccb14d5e) | [Tasks](https://atlas.nomic.ai/map/abc357dd-9c04-4913-9541-63e259d7ac1f/825139a4-af66-427c-9d0e-f36b5492ab3f) |


## News
- Released AI Society and Code dataset (April 2, 2023)
- Initial release of `CAMEL` python library (March 21, 2023)

## Citation
```
@misc{camel,
  author = {Guohao Li, Hasan Abed Al Kader Hammoud, Hani Itani, Dmitrii Khizbullin, Bernard Ghanem},
  title = {CAMEL: Communicative Agents for “Mind” Exploration of Large Scale Language Model Society},
  year = {2023},
  journal={arXiv preprint},
}
```
## Acknowledgement
Special thanks to [Nomic AI](https://home.nomic.ai/) for giving us extended access to their data set exploration tool (Atlas).

We would also like to thank Haya Hammoud for designing the logo of our project. 

## License

The intended purpose and licensing of CAMEL is solely for research use.

The source code is licensed under Apache 2.0.

The datasets are licensed under CC BY NC 4.0, which permits only non-commercial usage. It is advised that any models trained using the dataset should not be utilized for anything other than research purposes.

## Contact
For more information please contact [Guohao Li](https://ghli.org/), [Hasan Abed Al Kader Hammoud](https://cemse.kaust.edu.sa/ece/people/person/hasan-abed-al-kader-hammoud), [Hani Itani](https://github.com/HaniItani).
