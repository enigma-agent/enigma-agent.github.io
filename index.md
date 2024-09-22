---
layout: page
title: <img src="assets/img/big_logo.png">
description: >
  This is the landing and main page of EnIGMA
hide_description: true
sitemap: false
---


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



Although language model (LM) agents are demonstrating growing potential in many domains, their success in cybersecurity has been limited due to simplistic design and the lack of fundamental features for this domain. We present ***EnIGMA***, an LM agent for autonomously solving Capture The Flag (CTF) challenges. ***EnIGMA*** introduces new *Agent-Computer Interfaces* (ACIs) to  improve the success rate on CTF challenges. We establish the novel *Interactive Agent Tools* concept, which enables LM agents to run interactive command-line utilities essential for these challenges. Empirical analysis of EnIGMA on over 350 CTF challenges from three different benchmarks indicates that providing a robust set of new tools with demonstration of their usage helps the LM solve complex problems and achieves state-of-the-art results on the [NYU CTF](https://arxiv.org/abs/2406.05590) and [Intercode-CTF](https://openreview.net/pdf?id=KOZwk7BFc3) benchmarks.



### Leaderboard

<table><thead>
  <tr>
    <th>Benchmark</th>
    <th>Model</th>
    <th>% Solved</th>
    <th>Date</th>
    <th>Logs/Trajectories</th>
  </tr></thead>
<tbody>
  <tr>
    <td rowspan="4">NYU CTF</td>
    <td>EnIGMA w/ Claude 3.5 Sonnet</td>
    <td><strong>13.5</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4 Turbo (1106)</td>
    <td>7.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4o</td>
    <td>9.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>4.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="5">InterCode-CTF</td>
    <td>EnIGMA w/ Claude 3.5 Sonnet</td>
    <td>67.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4 Turbo (1106)</td>
    <td><strong>72.0</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4o</td>
    <td>69.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://openreview.net/pdf?id=KOZwk7BFc3">InterCode-CTF Agent</a></td>
    <td>40.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2403.13793">Google DeepMind Agent</a> w/ Gemini Ultra</td>
    <td>24.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="4">HackTheBox</td>
    <td>EnIGMA w/ Claude 3.5 Sonnet</td>
    <td><strong>26.0</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4 Turbo (1106)</td>
    <td>18.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EnIGMA w/ GPT-4o</td>
    <td>16.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>20.0</td>
    <td></td>
    <td></td>
  </tr>
</tbody></table>


### How It Works?

<!-- Capture The Flag Section -->
<div class="section sticky-section">
  <div id="animation-container">
    <img id="system-image" src="/assets/img/EnIGMA Figure1.png" alt="System Components">
    <div id="ctf-text" class="component-text">Capture The Flag Challenge: Explains the CTF part of the system.</div>
  </div>
</div>

<!-- Challenge Server + Computer Section -->
<div class="section sticky-section">
  <div id="animation-container">
    <div id="server-text" class="component-text">Challenge Server and Computer: Describes how the server and computer interact.</div>
  </div>
</div>

<!-- SWE-Agent Components Section -->
<div class="section sticky-section">
  <div id="animation-container">
    <div id="swe-agent-text" class="component-text">SWE-Agent Components: Outlines the agent's commands and interfaces.</div>
  </div>
</div>

<!-- Enigma Components Section -->
<div class="section sticky-section">
  <div id="animation-container">
    <div id="enigma-text" class="component-text">Enigma Components: Provides details on the LM-cybersecurity commands and summarizer.</div>
  </div>
</div>

<!-- ![figure1](/assets/img/EnIGMA%20Figure1.png) -->


### Interactive Agent Tools In Action





### BibTeX

~~~BibTeX
@article{Witten:1988hf,
      author         = "Witten, Edward",
      title          = "{Quantum Field Theory and the Jones Polynomial}",
      journal        = "Commun. Math. Phys.",
      volume         = "121",
      year           = "1989",
      pages          = "351-399",
      doi            = "10.1007/BF01217730",
      note           = "[,233(1988)]",
      reportNumber   = "IASSNS-HEP-88-33",
      SLACcitation   = "%%CITATION = CMPHA,121,351;%%"
}
~~~
