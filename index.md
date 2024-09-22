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

  <style>
    #animation-container {
      position: relative;
      width: 800px; /* Adjust based on your image size */
      height: 400px;
    }

    #full-image {
      width: 100%;
      height: auto;
    }

    #component-text {
      position: absolute;
      top: 50px;
      left: 50px;
      background-color: rgba(255, 255, 255, 0.8);
      padding: 15px;
      border-radius: 5px;
      display: none; /* Hidden initially */
    }

    .hidden {
      opacity: 0.2; /* To dim components not in focus */
    }

    #component-description {
      font-size: 18px;
      color: #333;
    }
    .section {
      height: 100vh;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #animation-container {
      position: relative;
      width: 90%;
      max-width: 1200px;
      height: 80vh;
      overflow: hidden;
    }

    #system-image {
      width: 100%;
      height: auto;
      transition: transform 1.5s ease-in-out; /* Smooth zoom transition */
    }

    .component-text {
      position: absolute;
      background-color: rgba(255, 255, 255, 0.8);
      padding: 10px;
      border-radius: 8px;
      font-size: 1.1rem;
      max-width: 300px;
      display: none; /* Initially hidden */
    }

    .visible {
      display: block !important;
      animation: fadeIn 1.5s ease-in-out;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(50px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Specific positioning of each text */
    #ctf-text { top: 50px; left: 20px; }
    #server-text { top: 150px; right: 50px; }
    #swe-agent-text { bottom: 150px; left: 20px; }
    #enigma-text { bottom: 50px; right: 50px; }

    /* Zoom-in effects on scroll */
    .zoom-ctf {
      transform: scale(2.5) translate(-25%, -15%);
    }

    .zoom-server {
      transform: scale(2.5) translate(35%, 20%);
    }

    .zoom-swe-agent {
      transform: scale(2.5) translate(-20%, 35%);
    }

    .zoom-enigma {
      transform: scale(2.5) translate(40%, -10%);
    }

    /* Restore image to the initial state */
    .reset {
      transform: scale(1) translate(0, 0);
    }

    /* Sticky behavior */
    .sticky-section {
      position: sticky;
      top: 0;
      z-index: 1;
    }
  </style>
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

  <script>
    // Track the scroll position to detect up/down scrolling
    let lastScrollTop = window.pageYOffset || document.documentElement.scrollTop;

    function handleScroll() {
      const windowHeight = window.innerHeight;
      const systemImage = document.getElementById('system-image');
      const currentScrollTop = window.pageYOffset || document.documentElement.scrollTop;
      const scrollingDown = currentScrollTop > lastScrollTop;

      // Restore to initial position if scrolling up
      if (!scrollingDown) {
        systemImage.className = 'reset'; // Reset the zoom and translation
        document.querySelectorAll('.component-text').forEach(text => text.classList.remove('visible'));
      }

      // Capture The Flag Zoom
      const ctfText = document.getElementById('ctf-text');
      const ctfPosition = ctfText.getBoundingClientRect().top;
      if (ctfPosition < windowHeight - 150 && scrollingDown) {
        systemImage.className = 'zoom-ctf';
        ctfText.classList.add('visible');
      }

      // Server + Computer Zoom
      const serverText = document.getElementById('server-text');
      const serverPosition = serverText.getBoundingClientRect().top;
      if (serverPosition < windowHeight - 150 && scrollingDown) {
        systemImage.className = 'zoom-server';
        serverText.classList.add('visible');
      }

      // SWE-Agent Zoom
      const sweAgentText = document.getElementById('swe-agent-text');
      const sweAgentPosition = sweAgentText.getBoundingClientRect().top;
      if (sweAgentPosition < windowHeight - 150 && scrollingDown) {
        systemImage.className = 'zoom-swe-agent';
        sweAgentText.classList.add('visible');
      }

      // Enigma Zoom
      const enigmaText = document.getElementById('enigma-text');
      const enigmaPosition = enigmaText.getBoundingClientRect().top;
      if (enigmaPosition < windowHeight - 150 && scrollingDown) {
        systemImage.className = 'zoom-enigma';
        enigmaText.classList.add('visible');
      }

      // Update last scroll position
      lastScrollTop = currentScrollTop <= 0 ? 0 : currentScrollTop;
    }

    // Attach scroll event listener
    window.addEventListener('scroll', handleScroll);
  </script>

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
