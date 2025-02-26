<h1>Knowledge contribution guidelines</h1>
<p>You can create a Git repository to host your knowledge contributions anywhere (GitLab, Gerrit, etc.) but it may be favorable to create one on GitHub. The following instructions show you how to create a knowledge repository in GitHub and contribute to the taxonomy.</p>
<h2>Prerequisites</h2>
<ul>
<li>You have a GitHub account</li>
<li>You have a forked copy of the <a href="https://github.com/instructlab/taxonomy/tree/main">taxonomy</a> repository</li>
<li>Verify that the model does not already know the knowledge you want to submit</li>
</ul>
<h2>Creating your own knowledge repository</h2>
<p>To create a new GitHub repository, follow the GitHub documentation in <a href="https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository">Creating a new repository</a>.</p>
<p>The specific steps are listed as follows:</p>
<ol>
<li>In your GitHub profile page, navigate to the repositories tab. You will see a search bar where you can search your repositories, or create a new one.</li>
<li>This takes you to a page titled “Create a new repository”. Create a custom name for your repository and add a README.md file. For example, “knowlege_contributions” could be a good name for your repository.</li>
<li>Click “Create” when you are all set.</li>
</ol>
<h2>Convert your knowledge documentation to markdown</h2>
<p>There are many online tools that can help you convert your documents to markdown. If you are using a wiki page for your contributions, you can use <a href="https://pandoc.org/try/">pandocs</a> to convert the documents. For wikipedia sources on pandoc, use <code>from: mediawiki</code> and convert <code>to: markdown_strict</code> to access the proper markdown format.</p>
<h2>Add the markdown file to your repository</h2>
<p>To add a file to your GitHub repository, follow the GitHub documentation in <a href="https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository">Adding a file to a repository</a>.</p>
<p>The specific steps are listed as follows:</p>
<ol>
<li>Navigate to “Add files”. Click “Create new file” if you want to manually add your markdown content. Click “Upload files” if you have a file locally to add.</li>
<li>Add a description and commit your changes.</li>
</ol>
<p>Since this is your own repository, you can commit directly to the <code>main</code> branch.
3. You can then see your new content in your repository.</p>
<blockquote>
<p>[!IMPORTANT]
Make a note of your commit SHA; you need it for your <code>qna.yaml</code>.</p>
</blockquote>
<h2>Create a pull request in the taxonomy repository</h2>
<p>Navigate to your forked taxonomy repository and ensure it is up-to-date.</p>
<p>There are a few ways you can create a pull request:</p>
<ul>
<li>For details on the local process, check out <a href="https://github.com/kubernetes/community/blob/master/contributors/guide/github-workflow.md">The GitHub Workflow Guide</a> in the kubernetes documentation and the <a href="https://docs.github.com/en/get-started/using-github/github-flow">GitHub flow</a> in the GitHub documentation.</li>
<li>For details on contributing using the GitHub webpage UI, see <a href="https://github.com/instructlab/taxonomy/docs/contributing_via_GH_UI.md">Contributing using the GH UI</a> or <a href="https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request?tool=webui">Creating a pull request</a> in the GitHub documentation.</li>
</ul>
<h2>Verification</h2>
<p>Here are a few things to check before seeking reviews for your contribution:</p>
<ul>
<li>Your <code>qna.yaml</code> follows the proper formatting. See examples in <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#knowledge-yaml-examples">Knowledge: YAML examples</a></li>
<li>Ensure all parameters are set. Especially the <code>document</code>, <code>repo</code>, <code>commit</code> and <code>pattern</code> keys; these parameters are specific to knowledge contributions and require more analysis.</li>
<li>Include an <code>attribution.txt</code> file for citing your sources. see <a href="https://github.com/instructlab/taxonomy/blob/main/CONTRIBUTING.md#for-your-attributiontxt-file">For your attribution.txt file</a> for more information.</li>
</ul>
<h2>PR Upstream Workflow</h2>
<p>The following table outlines the expected timing for the PR(s) you have put in. The PRs go through a few steps, and checks, but you should be able to map your <code>label</code> to
the place that it is in.</p>
<table>
<thead>
<tr>
<th>Label</th>
<th>Actor</th>
<th>Action</th>
<th>Duration</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td>Contributor</td>
<td>Submit PR</td>
<td>-</td>
</tr>
<tr>
<td></td>
<td>Contributor</td>
<td>Fix failed PR checks</td>
<td>-</td>
</tr>
<tr>
<td>https://github.com/instructlab/taxonomy/labels/triage-needed</td>
<td>Triager</td>
<td>Review PR, ask for changes</td>
<td>Days</td>
</tr>
<tr>
<td>https://github.com/instructlab/taxonomy/labels/triage-requested-changes</td>
<td>Contributor</td>
<td>Make requested changes</td>
<td>Days</td>
</tr>
<tr>
<td>https://github.com/instructlab/taxonomy/labels/precheck-generate-ready</td>
<td>Triager</td>
<td>Run prechecks and generate</td>
<td>Days</td>
</tr>
<tr>
<td>https://github.com/instructlab/taxonomy/labels/community-build-ready</td>
<td>Backend</td>
<td>Model gets retrained</td>
<td>Weeks</td>
</tr>
<tr>
<td></td>
<td>Triager</td>
<td>Check the numbers and PR merged or closed</td>
<td>-</td>
</tr>
</tbody>
</table>