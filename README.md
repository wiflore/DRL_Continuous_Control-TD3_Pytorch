# DRL_Continuous-Control
20 robotic arms that reach target locations. 


<div id="main-layout-content" aria-labelledby="header-title" class="_body-module--body--UXv_5"><div><div><div class="index--image--15qrG index-module--loaded--3wgql index-module--_container--2jdEh"><div class="index-module--thumb--3ud4h index-module--_image--3QmIX" style="background-image: url(&quot;https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5af79360_reacher/reacher_thumb_w32_h.png&quot;);"></div><div class="index-module--full--3vMOI index-module--_image--3QmIX" style="background-image: url(&quot;https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5af79360_reacher/reacher.png&quot;);"></div><div class="index--title--1BHso">Continuous Control</div></div><div class="index--project-container--2b9U1"><div><div class="container-fluid index--container--1H1L7"><div class="index--body--2gqet layout--content--3Smmq layout--body--3U2qN"><div><div class="index--due-at--2NaON"><div class="due-at--due-at--2ujLU"><div class="tooltip--tooltip-container--2mGjh" aria-describedby="tooltip-due-at"><span><div class="due-at--label--hKnHP">Due</div> <div class="due-at--value--VPabf">Jul 31</div></span><div class="tooltip--tooltip-hover-center--ks0Gb tooltip--hidden--1YyX5" id="tooltip-due-at">Suggested Deadline</div></div></div></div><h2 class="index--title--3eIzO">Project Submission</h2></div><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.</p>
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
<p>The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. </p>
<h2 id="evaluation">Evaluation</h2>
<hr>
<p>Your project will be reviewed by a Udacity reviewer against the <a target="_blank" href="https://review.udacity.com/#!/rubrics/1890/view">project rubric</a>. Review this rubric thoroughly, and self-evaluate your project before submission. All criteria found in the rubric must meet specifications for you to pass.</p>
<h2 id="ready-to-submit-your-project-">Ready to submit your project?</h2>
<hr>
<p>Click on the "Submit Project" button and follow the instructions to submit!</p>
</div></div></div></div><div><div><div class="_footer--footer--31z6y layout--content--3Smmq"><span class="_footer--status--2vs9S">You have not submitted the project yet</span><span><button class="vds-button vds-button--primary" type="button"><span class="vds-button__content">Submit Project</span></button></span></div></div></div></div></div></div></div></div>
