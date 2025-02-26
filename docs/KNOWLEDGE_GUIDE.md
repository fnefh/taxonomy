<h1>Knowledge Guide</h1>
<h2>What is "Knowledge"?</h2>
<p>Knowledge consists of data and facts and is backed by documents. When you create knowledge for a model, you're giving it additional data to more accurately answer questions.</p>
<p>Knowledge contributions in this project contain a few things.</p>
<ul>
<li>A file in a git repository that holds your information. For example, these repositories can include markdown versions of information on: Oscar 2024 winners, Law books, Shakespeare, Sports, Chemistry, etc.</li>
<li>A <code>qna.yaml</code> file that asks and answers questions about the information in the git repository.</li>
<li>A <code>attribution.txt</code> that includes the sources for the information used in the <code>qna.yaml</code>.</li>
</ul>
<p>You can learn more about the knowledge structure in <a href="https://github.com/instructlab/taxonomy/blob/main/README.md#getting-started-with-knowledge-contributions">Getting Started with Knowledge contributions</a>.</p>
<h2>Accepted Knowledge</h2>
<blockquote>
<p>[!IMPORTANT]
We are currently only accepting knowledge contributions as a limited private beta and sources will be limited to articles from Wikipedia.</p>
</blockquote>
<p>There are a few domains of knowledge that we are currently accepting. For a full list of knowledge fields, see <a href="https://github.com/instructlab/taxonomy/blob/main/knowledge/knowledge_domains.md">Knowledge domains</a> in the taxonomy documentation</p>
<p>A few examples are as follows:</p>
<h3>STEM fields</h3>
<ul>
<li>Physics</li>
<li>Astronomy and Astrophysics</li>
<li>Quantum Mechanics</li>
<li>Special Relativity and General Relativity</li>
<li>Chemistry &amp; Chemical Engineering</li>
<li>Organic Chemistry</li>
<li>Inorganic Chemistry</li>
<li>Chemical engineering</li>
<li>Biotechnology</li>
<li>Earth &amp; Environmental Science</li>
<li>Geology</li>
<li>Geography</li>
<li>Biology &amp; Life Sciences</li>
<li>Plants (Botany)</li>
<li>Medicine &amp; health</li>
<li>Electrical Engineering</li>
<li>Bioengineering</li>
<li>Civil Engineering</li>
<li>Industrial Engineering</li>
</ul>
<h3>Legal and regulatory</h3>
<ul>
<li>Intellectual Property</li>
<li>Criminal Law</li>
<li>Civil Rights</li>
<li>Healthcare compliance</li>
</ul>
<h3>Economy and Business</h3>
<ul>
<li>Economy and Businesses</li>
<li>Accounting and Finance</li>
<li>Marketing</li>
<li>Human Resource</li>
<li>Management</li>
</ul>
<h3>Philosophy</h3>
<ul>
<li>Philosophy</li>
<li>Metaphysics</li>
<li>Epistemology</li>
<li>Ethics</li>
<li>Parapsychology &amp; occultism</li>
<li>Philosophical schools of thought</li>
</ul>
<h3>Literature</h3>
<ul>
<li>Literature, rhetoric &amp; criticism</li>
<li>American literature in English</li>
<li>Other literatures</li>
</ul>
<h2>Avoid These Topics</h2>
<p>While the tuning process may eventually benefit from being used to help the models work with complex social topics, at this time this is an area of active research we do not want to take lightly. Therefore please keep your submissions clear of the following topics:</p>
<ul>
<li>PII (personally identifiable information) or any content invasive of individual privacy rights</li>
<li>Violence including self-harm</li>
<li>Cyber Bullying</li>
<li>Internal documentation or other that is confidential to your employer or organization, e.g. trade secrets</li>
<li>Discrimination</li>
<li>Religion</li>
<li>Facts such as, "<a href="https://en.wikipedia.org/wiki/Christianity_in_Nepal">Christianity is, according to the 2011 census, the fifth most practiced religion in Nepal, with 375,699 adherents, or 1.4% of the population</a>", are fine as a knowledge contribution. Advocating in favor of or against any religious faith is not acceptable.</li>
<li>Medical or health information</li>
<li>Facts such as, "<a href="https://opentextbc.ca/biology/chapter/11-3-circulatory-and-respiratory-systems/">In mammals, pulmonary ventilation occurs via inhalation (breathing)</a>," are fine as a knowledge contribution. Tailored medical/health advice is not acceptable.</li>
<li>Financial information</li>
<li>Facts such as "<a href="https://openstax.org/books/world-history-volume-2/pages/6-3-capitalism-and-the-first-industrial-revolution">laissez-faire economics ... argues that market forces alone should drive the economy and that governments should refrain from direct intervention in or moderation of the economic system</a>," are fine as a knowledge contribution. Tailored financial advice is not acceptable.</li>
<li>Legal settlements/mitigations</li>
<li>Gender Bias</li>
<li>Hostile Language, threats, slurs, derogatory or insensitive jokes or comments</li>
<li>Profanity</li>
<li>Pornography and sexually explicit or suggestive content</li>
<li>Any contributions that would allow for automated decision making that affect an individual's rights or well-being, e.g. social scoring</li>
<li>Any contributions that engage in political campaigning or lobbying</li>
</ul>
<p>We are also not accepting submissions of the following content:</p>
<ul>
<li>Code</li>
<li>Anything code-related that can be traced back to code for a computer. Not limited to <code>sed</code> or <code>bash</code> but <code>yaml</code>s for OpenShift or Kubernetes, to <code>python</code> snippets to <code>Java</code> suggestions. There are specific models focused on this space and this isn't for this model for the time being.</li>
<li>Jokes</li>
<li>Poems</li>
</ul>
<p>We received many joke and poem submissions at the beginning of the project, and with jokes being "in the eye of the beholder" and puns requiring nuance for native English speakers, we realized we were possibly unconsciously biasing our model. We have discovered that working with both topics has its own challenges, and if we want something generalized, finding consensus was unsuccessful. For now, we're not accepting additional submissions of jokes and poems.</p>
<h2>Building Your LLM Intuition</h2>
<p>LLMs have inherent limitations that make certain tasks extremely difficult, like doing math problems. They're great at other tasks, like creative writing. And they could be better at things like logical reasoning.</p>
<p>An LLM with knowledge helps it create a basis of information that it can learn from, then you can teach it to use this knowledge via the <code>qna.yaml</code> files.</p>
<p>For example, you can give an LLM the entire periodic table, then in a <code>qna.yaml</code> add something like:</p>
<p>question: What is the symbol and atomic number for Chlorine?
answer: |
The symbol for chlorine is Cl and the atomic number is 17.</p>
<p>With a few of these qna's, the model will learn the periodic table because it has the knowledge data.</p>
<h3>LLMs are great at</h3>
<p>For these, however, it's common for LLMs to already have excellent performance. Try 3-5 examples in <code>lab chat</code> to confirm a deficit in the model before you build your submission, and share the examples in your Pull Request (PR).</p>
<ul>
<li>Brainstorming</li>
<li>Creativity</li>
<li>Connecting information</li>
<li>Cross-lingual behavior</li>
</ul>
<h3>LLMs need help with</h3>
<p>LLM behavior in these sorts of topics are very difficult for the model to get right. Try several examples to understand the nuances of the model's ability to do these sorts of tasks, and consider using corrections to the results you get in your tuning process.</p>
<ul>
<li>Chains of reasoning</li>
<li>Analysis</li>
<li>Story plots</li>
<li>Reassembling information</li>
<li>Effective and succinct summaries</li>
</ul>
<h3>LLMs are not so great at</h3>
<p>LLMs may struggle with solving math and computation. That said, improving some of these foundational skills may be something this work tackles in the future, but not at this time.</p>
<ul>
<li>Math</li>
<li>Computation</li>
<li>"Turing-complete" type tasks</li>
<li>Generating only true real-world information (they're prone to hallucinations)</li>
</ul>