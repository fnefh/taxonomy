<h1>Contributing</h1>
<p>👍🎉 First off, thank you for taking the time to contribute! 🎉👍</p>
<p>The following is a set of guidelines for contributing. These are just guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request. Please read the <a href="https://github.com/instructlab/community/blob/main/CONTRIBUTING.md">Community Contribution Guide</a> first for general practices for the InstructLab community.</p>
<h2>What Should I Know Before I Get Started?</h2>
<h3>Code of Conduct</h3>
<p>This project adheres to the <a href="https://github.com/instructlab/community/blob/main/CODE_OF_CONDUCT.md">Contributor Covenant</a>. By participating, you are expected to uphold this code.</p>
<p>Please report unacceptable behavior to one of the <a href="https://github.com/instructlab/community/blob/main/MAINTAINERS.md">Maintainers</a>.</p>
<h3>Related repositories</h3>
<p>In addition to this repository, InstructLab has two related repositories:</p>
<ul>
<li><a href="https://github.com/instructlab/instructlab">CLI</a>. This repository is responsible for the the <code>ilab</code> command-line interface (CLI) tool.</li>
<li><a href="https://github.com/instructlab/community">Community</a>. This repository is responsible for showing collaboration details across the InstructLab community.</li>
</ul>
<p>The following sections provide a general overview for contributing to the Taxonomy repository.</p>
<h2>Ways of contributing to the taxonomy repository</h2>
<h3>Contributing skills and knowledge</h3>
<p>You can contribute to the taxonomy in the following two ways:</p>
<ol>
<li>
<p>Adding new examples to <strong>existing leaf nodes</strong>:</p>
</li>
<li>
<p>Go to the corresponding leaf node / end of the branch and modify the YAML</p>
</li>
<li>Add a new example to the <code>qna.yaml</code> files as a new entry to the list</li>
<li>
<p>Adding <strong>new branches/skills</strong> corresponding to the existing domain:</p>
</li>
<li>
<p>You can add new folders under the corresponding category (replace any spaces with underscores <code>_</code>)</p>
</li>
<li>Create a new <code>qna.yaml</code> file containing examples for the new skill</li>
</ol>
<p>A detailed contribution guide is documented in the <a href="#how-can-i-contribute">How can I contribute section</a> section.</p>
<h3>Contributing new features, enhancements or documentation</h3>
<p>Help on open source projects is always welcome and there is always something that can be improved. For example, documentation (like the text you are reading now) can always use improvement, code can always be clarified, variables or functions can always be renamed or commented on, and there is always a need for more test coverage. If you see something that you think should be fixed, take ownership! Here is how you get started:</p>
<p>To propose a new feature, it's best to raise an issue in the appropriate repository. This way, features can be discussed with the project maintainers, ensuring that your time is not wasted working on a feature that the project developers will not accept into the codebase.</p>
<p><em>How Do I Submit A (Good) Enhancement or Improvement item?:</em> Enhancements and improvement items suggestions are tracked as <a href="https://github.com/instructlab/taxonomy/issues/new?assignees=&amp;labels=&amp;projects=&amp;template=proposal.md&amp;title=">GitHub issues: Proposal</a>. Create an issue and provide the information suggested in the proposal template.</p>
<h2>How do I start contributing?</h2>
<p>The following workflow is designed to help you begin your first contribution journey. It will guide you through creating and picking up issues, working through them, having your work reviewed, and then merging.</p>
<h3>How Can I Contribute?</h3>
<p>The goal of InstructLab is to enable true collaborative development around common Large Language Models (LLMs) using a technology that enables collaboration following standard open source development practices. A general overview of making a contribution to this project consists of writing an extension to the existing taxonomy, making a pull request, and getting your work reviewed and merged so that it can benefit the whole community.</p>
<p>Before you start, review the <a href="https://github.com/instructlab/taxonomy/issues">open issues</a> and <a href="https://github.com/instructlab/taxonomy/pulls">opened pull requests</a> board to see if your contribution or enhancements are already proposed. You might instead be able to join forces with them by providing input to what they have started. If you are unsure about what kind of skill or knowledge to contribute, you can <a href="https://github.com/instructlab/taxonomy/issues/new?assignees=&amp;labels=&amp;template=proposal.md&amp;title=">open an issue</a> first to discuss your proposal idea with the maintainers.</p>
<p>To contribute to this repo, you'll use the <em>Fork and Pull</em> model common in many open source repositories. You can follow this process in a local terminal or in the GitHub web UI.</p>
<ul>
<li>For details on the local process, check out the <a href="https://docs.github.com/en/get-started/using-github/github-flow">GitHub flow</a> documentation from GitHub and <a href="https://github.com/kubernetes/community/blob/master/contributors/guide/github-workflow.md">The GitHub Workflow Guide</a> documentation from Kubernetes.</li>
<li>For details on contributing using the GitHub webpage UI, see <a href="docs/contributing_via_GH_UI.md">Contributing using the GH UI</a>.</li>
</ul>
<blockquote>
<p>[!IMPORTANT]
For all contributions to InstructLab 🐶, you want to become familiar with the workflow described in the <a href="https://github.com/instructlab/instructlab">InstructLab 🐶 CLI
<code>ilab</code></a> documentation. It would be best to understand how to test
your changes, generating new data, training and downloading the new model, and testing it to check that it gives you the desired results.</p>
</blockquote>
<p>When your contribution is ready, you can create a pull request (PR). In general, we follow the standard <a href="https://help.github.com/en/articles/about-pull-requests">GitHub pull request</a> process. Follow the template to provide details about your pull request to the maintainers. Before submitting pull requests, make sure your changes pass applicable formatting tests in the repository CI.</p>
<blockquote>
<p>[!NOTE]
Always refer to the <a href="https://github.com/instructlab/taxonomy/blob/main/README.md">README.md</a>
if you are unsure on how to format your contributions.</p>
</blockquote>
<h3>What can I contribute?</h3>
<p>You can contribute <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#getting-started-with-knowledge-contributions">Knowledge</a> or <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#getting-started-with-skill-contributions">Skills</a> to the taxonomy tree. Make sure to review the <a href="README.md">general documentation</a> for a detail explanation of these concepts and the differences between the two.</p>
<blockquote>
<p>[!IMPORTANT]
You can only contribute original material. <strong>DO NOT</strong> contribute copyrighted content or content coming from another system.</p>
</blockquote>
<h3>Submitting your contribution</h3>
<p>When submitting your PR, give it a title which is as explicit as possible. Include in the description of the PR on GitHub, both what the system gave you before your contribution and what it gives you with your contribution.</p>
<h3>Pull request review</h3>
<p>Once you've <a href="#how-can-i-contribute">created a pull request</a>, maintainers will review your proposed addition and may make suggestions to fix before merging. It will be easier for your pull request to receive reviews if you consider the criteria the reviewers follow while working. Remember to:</p>
<ul>
<li>Run tests locally and ensure that they pass</li>
<li>Ensure your contribution is in the proper format (<code>ilab generate</code> shouldn't report any warnings or errors)</li>
<li>Break large changes into a logical series of smaller patches, which are easy to understand individually and combine to solve a broader issue</li>
<li>Follow the project coding conventions</li>
<li>Include the DCO sign off; see <a href="#legal">Legal</a></li>
</ul>
<p>The project maintainers use <code>LGTM</code> (Looks Good To Me) in comments on the code review to indicate acceptance. You can see more information on the triaging process in the <a href="https://github.com/instructlab/taxonomy/blob/main/docs/triaging/triaging-contributions.md">Triaging skills</a> documentation.</p>
<p>For a list of the maintainers and triagers, see the <a href="https://github.com/instructlab/community/blob/main/MAINTAINERS.md">MAINTAINERS.md</a> page.</p>
<h2>Submitting bugs</h2>
<p>To submit a new bug, raise an issue in the appropriate repository before creating a pull request. This ensures that the issue is properly tracked. To fix an existing bug, assign yourself a bug from the issues page of the desired repository. Then, submit a pull request for review.</p>
<p>Bugs are tracked as <a href="https://github.com/instructlab/taxonomy/issues/new?assignees=&amp;labels=&amp;template=bug_report.md&amp;title=">GitHub issues using the Bug Report template</a>. Create an issue on that and provide the information suggested in the bug report issue template.</p>
<h2>Legal</h2>
<p>We have tried to make it as easy as possible to make contributions.
This applies to how we handle the legal aspects of contribution.
We use the same approach - the <a href="https://developercertificate.org/">Developer's Certificate of Origin 1.1 (DCO)</a> - that <a href="https://docs.kernel.org/process/submitting-patches.html#sign-your-work-the-developer-s-certificate-of-origin">the Linux Kernel community uses</a> to manage code contributions. All contributions that leverage third-party content should either come from the public domain or be licensed with an open data license that does not restrict commercial use or the creation of derivative works, including the following license types:</p>
<ul>
<li>CC0-1.0</li>
<li>CDLA-Permissive-2.0</li>
<li>CC-BY-4.0</li>
<li>CC-BY-SA-4.0</li>
<li>Apache-2.0</li>
<li>MIT</li>
</ul>
<p>Any third-party content contributed to this project undergoes modifications in order to formulate it in the templated format required for submission to this project.</p>
<p>We simply ask that when submitting a patch for review, the developer must include a sign-off statement in the commit message.</p>
<p>Here is an example <code>Signed-off-by</code> line, which indicates that the submitter accepts the DCO:</p>
<p><code>text
Signed-off-by: John Doe &lt;john.doe@example.com&gt;</code></p>
<p>You can include this automatically when you commit a change to your local Git repository using the following command:</p>
<p><code>shell
git commit -s</code></p>
<blockquote>
<p>[!TIP]
If you created a commit message that did not include the <code>-s</code> option, you can edit your original commit message by using the <code>git commit -s --amend</code> command. Ensure you force push the amended commit to your pull request (PR).</p>
</blockquote>
<h3>License</h3>
<p>Unless specifically stated, this project is
distributed under the <a href="http://www.apache.org/licenses/LICENSE-2.0">Apache License, Version 2.0</a>.</p>
<p>SPDX-License-Identifier: <a href="https://spdx.org/licenses/Apache-2.0">Apache-2.0</a></p>
<p>For more details, see the <LICENSE>.</p>
<h3>For your attribution.txt file</h3>
<p>An important part of contributing to the InstructLab project is citing your sources of information. This comes in the form of your <code>attribution.txt</code> that you add to the pull requests. Almost all instances of attribution can be covered by the parameters required for Creative Commons Attribution licenses. Some parameters are as follows:</p>
<ul>
<li>Title of work</li>
<li>Link to work</li>
<li>Include link to a specific revision where possible</li>
<li>License of the work</li>
<li>Include an SPDX identifier where possible</li>
<li>Creator names</li>
<li>Copyright information</li>
<li>Modification information</li>
<li>Indicate if work was itself derived from another openly licensed work</li>
</ul>
<p>You can also see this citation style in the <a href="https://github.com/instructlab/community/blob/main/docs/DataSources.md">Data sources documentation</a></p>
<h2>Development</h2>
<p>Please consult the <a href="https://github.com/instructlab/instructlab"><code>ilab</code> documentation</a> to set up your environment.</p>