<div class="_main--content-container--ILkoI"><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown ">
  
  <h1 id="the-environment">Deep Reinforcerment Learning Project: Continuous Control</h1>
  
  
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown ">
  
  <p>For this project, I worked with the <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher">Reacher</a> environment.  </p>
  
  
  
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div><a href="#" class="image-atom--image-atom--1XDdu"><div class="index--image-atom-content--YoZVu"><div class="index--image-and-annotations-container--1o6QP"><img src="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif" alt="Unity ML-Agents Reacher Environment" width="500px" class="index--image--1wh9w"></div><div class="index--caption--34paT"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Unity ML-Agents Reacher Environment</p>
  
  
</div></div></div></a></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown ">
  
<p>In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.</p>

<p>The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.</p>


<h2 id="distributed-training">Distributed Training</h2>
<hr>
<ul>
<li>The project contains 20 identical agents, each with its own copy of the environment.  </li>
</ul>
<p>I used DDPG-TD3 algorithm to solve the problem (Theory: https://spinningup.openai.com/en/latest/algorithms/td3.html,
    Reference Implementation: https://github.com/udacity/deep-reinforcement-learning/blob/master/ddpg-bipedal/DDPG.ipynb,
    Good implementation: https://github.com/henry32144/TD3-Pytorch)
    </p>
<h2 id="solving-the-environment">Solving the Environment</h2>
<hr>

<p>The barrier for solving  the environment is take into account the presence of many agents.  In particular, agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,</p>
<ul>
<li>After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent.  This yields 20 (potentially different) scores.  We then take the average of these 20 scores. </li>
<li>This yields an <strong>average score</strong> for each episode (where the average is over all 20 agents).</li>
</ul>
<p>As an example, consider the plot below, where we have plotted the <strong>average score</strong> (over all 20 agents) obtained with each episode.</p>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div><a href="#" class="image-atom--image-atom--1XDdu"><div class="index--image-atom-content--YoZVu"><div class="index--image-and-annotations-container--1o6QP"><img src="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/July/5b48f845_unknown/unknown.png" alt="Plot of average scores (over all agents) with each episode." width="386px" class="index--image--1wh9w"></div><div class="index--caption--34paT"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Plot of average scores (over all agents) with each episode.</p>
</div></div></div></a></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>The environment is considered solved, when the average (over 100 episodes) of those <strong>average scores</strong> is at least +30.  In the case of the plot above, the environment was solved at episode 63, since the average of the <strong>average scores</strong> from episodes 64 to 163 (inclusive) was greater than +30.</p>
</div></div><span></span></div></div></div></div>

<h2 id="step-1-activate-the-environment">Activate the Environment</h2>

<div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Follow the instructions below to explore the environment on your own machine!  You will also learn how to use the Python API to control your agent.</p>

<hr>
<p>If you haven't already, please follow the <a target="_blank" href="https://github.com/udacity/deep-reinforcement-learning#dependencies">instructions in the DRLND GitHub repository</a> to set up your Python environment.  These instructions can be found in <code>README.md</code> at the root of the repository.  By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.</p>
<p>(<em>For Windows users</em>) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.  </p>

<h2 id="step-2-download-the-unity-environment">Download the Unity Environment</h2>
<hr>
<p>For this project, you will <strong>not</strong> need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below.  You need only select the environment that matches your operating system:</p>
<h3 id="version-2-twenty-20-agents">Version: Twenty (20) Agents</h3>
<ul>
<li>Linux: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip">click here</a></li>
<li>Mac OSX: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip">click here</a></li>
<li>Windows (32-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip">click here</a></li>
<li>Windows (64-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip">click here</a></li>
</ul>
<p>Then, place the file in the <code>p2_continuous-control/</code> folder in the DRLND GitHub repository, and unzip (or decompress) the file.</p>
<p>(<em>For Windows users</em>) Check out <a target="_blank" href="https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64">this link</a> if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.</p>
<p>(<em>For AWS</em>) If you'd like to train the agent on AWS (and have not <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md">enabled a virtual screen</a>), then please use <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip">this link</a> to obtain the "headless" version of the environment.  You will <strong>not</strong> be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (<em>To watch the agent, you should follow the instructions to <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md">enable a virtual screen</a>, and then download the environment for the <strong>Linux</strong> operating system above.</em>)</p>

</div></div>

<h2 id="step-3-explore-the-environment">Train the agents</h2>
<hr>

Use requirement.txt file to install all libraries requires to the project, open the Notebook <code>Continuous_Control.ipynb</code> which is divided:


1. Start the enviroment
2. Examine the State and Action Spaces
3. Take Random Actions in the Environment
4. Model selected: DDPG - TD3
5. Training the agents
6. Testing the agents
7. Future improvement




