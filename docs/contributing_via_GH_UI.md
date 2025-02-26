<h1>Contributing using the GitHub webpage UI</h1>
<p>There are a few ways you can create pull requests in an open source project: Locally using the git CLI tool in your terminal or using the GitHub webpage user interface. The following instructions show you how to create a PR using the GitHub webpage UI</p>
<h2>Prerequisites</h2>
<ul>
<li>You have a GitHub account</li>
<li>You have access to this repo</li>
</ul>
<h2>Make a copy of the taxonomy repo</h2>
<ol>
<li>
<p>Go to <a href="https://github.com/instructlab/taxonomy">github.com/instructlab/taxonomy</a>.</p>
</li>
<li>
<p>Click <strong>Fork</strong> to fork your own copy of the repo.</p>
</li>
<li>
<p>On the <strong>Create a new fork</strong> page, enter the information into the following fields:</p>
<ul>
<li><strong>Repository name:</strong> Name your fork the same as the repository, in this case <code>taxonomy</code> is the name of your fork.</li>
<li><strong>Description:</strong> Enter the description of <em>your fork</em>, not of the skills you will create. You can write something that makes sense to you or leave it blank.</li>
<li><strong>Copy the main branch only:</strong> The box is selected by default. You can choose to leave the box selected or clear it.</li>
</ul>
</li>
<li>
<p>Click <strong>Create Fork</strong>.</p>
</li>
</ol>
<p>You will get a copy of the taxonomy repo in your github account. This is your own copy, so don't worry about making mistakes. <em>If you do end up making a mistake and want to start over: you can delete the fork and create a new fork.</em></p>
<h2>Contributing a skill</h2>
<ol>
<li>
<p>IMPORTANT: Before you begin, create a working branch for your contribution and name it whatever you like. This allows you to have an up-to-date <code>main</code> branch in your fork as well as a working branch to add any changes.</p>
<p><img alt="add_branch" src="assets/add_skill_branch.png" /></p>
</li>
<li>
<p>Navigate to the directory where you want your knowledge or skill. The following image shows the compositional skills directory and its contents. Skills are contributed to this directory:</p>
<p><img alt="comp_skill" src="assets/comp_skill.png" /></p>
<p>The other top-level directory you can contribute to is the knowledge directory, which is used for knowlege contributions. You can read more about the difference between skills and knowledge in the <a href="https://github.com/instructlab/community/blob/main/docs/README.md">community documentation</a>.</p>
</li>
<li>
<p>Based on the directories that exist in the tree, make a best guess at where in the tree structure to add the skill that you want to contribute. If you get to a point where you've gone deep enough into the tree and you can't find any directories that match, create a new directory (and subdirectories, if needed) to best represent your skill.</p>
<p>For example, I want to train the model to learn how to create sentences using rhetorical devices, specifically similes. I started in the compositional_skills section, and navigated to linguistics.</p>
<p><img alt="linguistics_file" src="assets/linguistics.png" /></p>
<p>There is currently no rhetorical_devices folder in the linguistics section, so I can create one called "rhetorical_devices", then click <code>/</code> to create another folder called "simile"</p>
<p><img alt="new_file" src="assets/new_file.png" /></p>
<p><img alt="simile_folder" src="assets/simile_folder.png" /></p>
</li>
<li>
<p>It can be a little tricky mechanically to create directories in GitHub's web UI, but you can complete the process using the following steps:</p>
<p>a. In the GitHub repo, click the folder that you want to create the new directory inside of.</p>
<p>b. Click Add File and select Create new file from the menu.</p>
<p>c. Type the name of the first directory that you want to create. The  example image uses rhetorical_devices as the first directory, then metaphor as the next.</p>
<p>d. After you have entered the name of all of the directories that you want to add, type the file name. The file name should always be qna.yaml (qna stands for "Question aNd Answer.")</p>
<p><img alt="qna_example" src="assets/qna_ex.png" /></p>
<p>e. You can then click "commit changes" to your branch. The GitHub UI will prompt you to open a pull requestion. Select the "open pull request" button.</p>
</li>
<li>
<p>Verify that your YAML follows the proper structure. See <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#knowledge-yaml-examples">Knowledge: YAML examples</a> and <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#skills-yaml-examples">Skills: YAML examples</a> to help with formatting. The <a href="https://www.yamllint.com/">yamllint</a> tool is another great way to verify yaml.</p>
</li>
</ol>