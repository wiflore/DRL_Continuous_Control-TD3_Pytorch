<div class="_main--content-container--ILkoI"><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h1 id="the-environment">The Environment</h1>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>For this project, you will work with the <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher">Reacher</a> environment.  </p>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div><a href="#" class="image-atom--image-atom--1XDdu"><div class="index--image-atom-content--YoZVu"><div class="index--image-and-annotations-container--1o6QP"><img src="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif" alt="Unity ML-Agents Reacher Environment" width="500px" class="index--image--1wh9w"></div><div class="index--caption--34paT"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Unity ML-Agents Reacher Environment</p>
</div></div></div></a></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.</p>
<p>The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.</p>
<h2 id="distributed-training">Distributed Training</h2>
<hr>
<p>For this project, we will provide you with two separate versions of the Unity environment:</p>
<ul>
<li>The first version contains a single agent.</li>
<li>The second version contains 20 identical agents, each with its own copy of the environment.  </li>
</ul>
<p>The second version is useful for algorithms like <a target="_blank" href="https://arxiv.org/pdf/1707.06347.pdf">PPO</a>, <a target="_blank" href="https://arxiv.org/pdf/1602.01783.pdf">A3C</a>, and <a target="_blank" href="https://openreview.net/pdf?id=SyZipzbCb">D4PG</a> that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience.  </p>
<h2 id="solving-the-environment">Solving the Environment</h2>
<hr>
<p>Note that your project submission need only solve one of the two versions of the environment. </p>
<h3 id="option-1-solve-the-first-version">Option 1: Solve the First Version</h3>
<p>The task is episodic, and in order to solve the environment,  your agent must get an average score of +30 over 100 consecutive episodes.</p>
<h3 id="option-2-solve-the-second-version">Option 2: Solve the Second Version</h3>
<p>The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents.  In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,</p>
<ul>
<li>After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent.  This yields 20 (potentially different) scores.  We then take the average of these 20 scores. </li>
<li>This yields an <strong>average score</strong> for each episode (where the average is over all 20 agents).</li>
</ul>
<p>As an example, consider the plot below, where we have plotted the <strong>average score</strong> (over all 20 agents) obtained with each episode.</p>
</div></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div><a href="#" class="image-atom--image-atom--1XDdu"><div class="index--image-atom-content--YoZVu"><div class="index--image-and-annotations-container--1o6QP"><img src="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/July/5b48f845_unknown/unknown.png" alt="Plot of average scores (over all agents) with each episode." width="386px" class="index--image--1wh9w"></div><div class="index--caption--34paT"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Plot of average scores (over all agents) with each episode.</p>
</div></div></div></a></div><span></span></div></div></div><div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>The environment is considered solved, when the average (over 100 episodes) of those <strong>average scores</strong> is at least +30.  In the case of the plot above, the environment was solved at episode 63, since the average of the <strong>average scores</strong> from episodes 64 to 163 (inclusive) was greater than +30.</p>
</div></div><span></span></div></div></div></div>
