<h1>Docs</h1>
<p>The purpose of these documents is to inform users and maintainers on the review/triaging process and different ways to contribute to the taxonomy repository. You can view the following:</p>
<ul>
<li>Full layout of taxonomy repository - <a href="taxonomy_diagram.md">Taxonomy diagram</a></li>
<li>Flowchart of the pull request review process - <a href="assets/review-process.png">Review process</a></li>
<li>Flowchart of how the backend works with reviewing PRS - <a href="assets/backend.png">Backend process</a></li>
</ul>
<h2>Overview of the Review Process</h2>
<p>The review process starts with contributor drafting the PR.</p>
<ol>
<li>At the PR stage, reviewers manually check its contents (e.g. making sure the examples are added to the correct path, inspecting the contents of examples).</li>
<li>If not valid, go back to the contributor and ask them to take actions.</li>
<li>If a PR passes step 1, the SDG will be triggered to generate synthetic data samples.</li>
<li>If not valid, go back to the contributor and ask them to take actions.</li>
<li>If step 2 passes, it will be used in the next model update.</li>
</ol>
<p>See the <a href="https://github.com/instructlab/instructlab/blob/main/docs/README.md">README.md in <code>instructlab/docs</code></a> on how to modify and render the flowcharts.</p>
<p>For more information on the review process, see <a href="https://github.com/instructlab/taxonomy/blob/main/CONTRIBUTING.md#pull-request-review">Pull request review in CONTRIBUTING.md</a></p>
<h2>Triaging documentation</h2>
<p>For more information on triaging contributions pull requests, see:</p>
<ul>
<li><a href="triaging/safe-responses.md">Safe responses for common PR mistakes</a></li>
<li><a href="triaging/triaging-contributions.md">Triaging guide</a></li>
</ul>
<h2>Contributing documentation</h2>
<p>For documentation contribution processes, see:</p>
<ul>
<li><a href="contributing_via_GH_UI.md">Contributing using the GitHub webpage UI</a></li>
<li><a href="knowledge-contribution-guide.md">Knowledge contribution guidelines</a></li>
<li><a href="../CONTRIBUTING.md">CONTRIBUTING.md</a></li>
</ul>