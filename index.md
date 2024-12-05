---
layout: page
title: <img src="assets/img/big_logo.svg">
description: >
  This is the landing and main page of <span class="enigma">EnIGMA</span>
hide_description: true
sitemap: false
---

<style type="text/css">
.no-zebra-table td{
    background-color: var(--gray-bg) !important;
}

/* Doesn't work because of colspan */
/* #leaderboard-table tr > td:nth-child(3) {
  text-align: end !important;
} */


tr.separator-row {
    border-bottom: 2px solid var(--border-color) !important;
}

td.top-align {
    vertical-align: top;
}

.enigma {
  background: linear-gradient(to right, #ec412b, #ec008c);
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  font-weight: bold;
  font-style: italic;
}

.label-date {
  font-size: 0.8em;
  padding: 0.2em 0.6em;
  color: white;
  background-color: var(--grey);
  border-radius: 0.5em;
  text-align: center;
}
</style>

## Enhanced Interactive Generative Model Agent for CTF Challenges

Talor Abramovich[^1], Meet Udeshi[^2], Minghao Shao[^2], Kilian Lieret[^3], Haoran Xi[^2], Kimberly Milner[^2], Sofija
Jancheska[^2], John Yang[^4], Carlos E. Jimenez[^3], Farshad Khorrami[^2], Prashanth Krishnamurthy[^2], Brendan
Dolan-Gavitt[^2], Muhammad Shafique[^5], Karthik Narasimhan[^3], Ramesh Karri[^2], and Ofir Press[^3]
{:.lead}

[^1]: *Tel-Aviv University*
[^2]: *New York University*
[^3]: *Princeton Language and Intelligence, Princeton University*
[^4]: *Stanford University*
[^5]: *New York University Abu Dhabi*

Although language model (LM) agents are demonstrating growing potential in many domains, their success in cybersecurity has been limited due to simplistic design and the lack of fundamental features for this domain. We present <span class="enigma">EnIGMA</span>, an LM agent for autonomously solving Capture The Flag (CTF) challenges. <span class="enigma">EnIGMA</span> introduces new *Agent-Computer Interfaces* (ACIs) to  improve the success rate on CTF challenges. We establish the novel *Interactive Agent Tools* concept, which enables LM agents to run interactive command-line utilities essential for these challenges. Empirical analysis of <span class="enigma">EnIGMA</span> on over 350 CTF challenges from three different benchmarks indicates that providing a robust set of new tools with demonstration of their usage helps the LM solve complex problems and achieves state-of-the-art results on the [NYU CTF](https://arxiv.org/abs/2406.05590) and [Intercode-CTF](https://openreview.net/pdf?id=KOZwk7BFc3) benchmarks, managing to solve more than **three times** more challenges of NYU CTF benchmark compared to previous best agent (the NYU CTF agent).


Want to try it yourself and explore our new agent? We are completely *open-source*!
You can try it out in the [SWE-agent repository](https://github.com/princeton-nlp/SWE-agent) ![GitHub Repo stars](https://img.shields.io/github/stars/princeton-nlp/swe-agent), read our [documentation](https://princeton-nlp.github.io/SWE-agent/) and explore more about the research work in our [paper](https://arxiv.org/abs/2409.16165).
{:.note title="Try It Out!"}

### Results

<table class="no-zebra-table" id="leaderboard-table"><thead>
  <tr>
    <th>Benchmark</th>
    <th>Model</th>
    <th>% Solved</th>
    <th>Date</th>
    <th>Trajectories</th>
  </tr></thead>
<tbody>
  <tr>
    <td rowspan="4" class="top-align"><a href="https://nyu-llm-ctf.github.io/">NYU CTF</a></td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td><strong>13.5</strong></td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/NYU_CTF/claude35_sonnet_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td>7.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/NYU_CTF/gpt4_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>9.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/NYU_CTF/gpt4o_pass1" /></td>
  </tr>
  <tr class="separator-row">
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>4.0</td>
    <td><span class="label-date">2024-08-21</span></td>
    <td><a href="https://github.com/NYU-LLM-CTF/leaderboard_submissions/tree/main/transcripts/baseline_gpt4" /></td>
  </tr>
  <tr>
    <td rowspan="5" class="top-align">InterCode-CTF</td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td>67.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/InterCode_CTF/claude35_sonnet_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td><strong>72.0</strong></td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/InterCode_CTF/gpt4_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>69.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/InterCode_CTF/gpt4o_pass1" /></td>
  </tr>
  <tr>
    <td><a href="https://openreview.net/pdf?id=KOZwk7BFc3">InterCode-CTF Agent</a></td>
    <td>40.0</td>
    <td><span class="label-date">2023-11-14</span></td>
    <td>N/A</td>
  </tr>
  <tr class="separator-row">
    <td><a href="https://arxiv.org/abs/2403.05530">Google DeepMind Agent</a> w/ Gemini 1.5 Pro</td>
    <td>43.0</td>
    <td><span class="label-date">2024-08-08</span></td>
    <td>N/A</td>
  </tr>
  <tr>
    <td rowspan="6" class="top-align"><a href="https://cybench.github.io/">CyBench</a></td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td><strong>20.0</strong></td>
    <td><span class="label-date">2024-12-05</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/CyBench/claude35_sonnet_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td>17.5</td>
    <td><span class="label-date">2024-12-05</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/CyBench/gpt4_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>12.5</td>
    <td><span class="label-date">2024-12-05</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/CyBench/gpt4o_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ Llama 3.1 405B Instruct</td>
    <td>10.0</td>
    <td><span class="label-date">2024-12-05</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/CyBench/llama31_405b_pass1" /></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2408.08926">CyBench agent</a> w/ Claude 3.5 Sonnet</td>
    <td>17.5</td>
    <td><span class="label-date">2024-08-15</span></td>
    <td><a href="https://drive.google.com/drive/u/1/folders/1xkA8wdAhSSYNQERQ2B7Gpzp87qP1Wgyl"/></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2408.08926">CyBench agent</a> w/ Llama 3.1 405B Instruct</td>
    <td>7.5</td>
    <td><span class="label-date">2024-08-15</span></td>
    <td><a href="https://drive.google.com/drive/u/1/folders/1xkA8wdAhSSYNQERQ2B7Gpzp87qP1Wgyl"/></td>
  </tr>
  <tr>
    <td rowspan="4" class="top-align">HackTheBox</td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td><strong>26.0</strong></td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/HTB/claude35_sonnet_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td>18.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/HTB/gpt4_pass1" /></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>16.0</td>
    <td><span class="label-date">2024-09-24</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/HTB/gpt4o_pass1" /></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>20.0</td>
    <td><span class="label-date">2024-08-21</span></td>
    <td><a href="https://github.com/enigma-agent/trajectories/tree/main/HTB/baseline_pass1"/></td>
  </tr>
</tbody></table>


### How it Works

<video controls preload="none" poster="/assets/img/Enigma Figure1.png" autoplay muted>
    <source src="/assets/video/enigma_fig1_medium.mov" type="video/mp4">
</video>
<!-- ![figure1](/assets/img/<span class="enigma">EnIGMA</span>%20Figure1.png) -->

### Interactive Agent Tools In Action

<iframe width="560" height="315" src="https://www.youtube.com/embed/IJxqOsNFiCc?si=xtIxyCcriM9FJexK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### BibTeX

If you found this work helpful, please consider using the following citation:

```bibtex
@misc{abramovich2024enigmaenhancedinteractivegenerative,
      title={EnIGMA: Enhanced Interactive Generative Model Agent for CTF Challenges},
      author={Talor Abramovich and Meet Udeshi and Minghao Shao and Kilian Lieret and Haoran Xi and Kimberly Milner and Sofija Jancheska and John Yang and Carlos E. Jimenez and Farshad Khorrami and Prashanth Krishnamurthy and Brendan Dolan-Gavitt and Muhammad Shafique and Karthik Narasimhan and Ramesh Karri and Ofir Press},
      year={2024},
      eprint={2409.16165},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2409.16165},
}
```
