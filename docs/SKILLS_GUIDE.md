<h1>Skills Guide</h1>
<h2>What is a "Skill"?</h2>
<p>There are various types of skills that you can contribute to the taxonomy.</p>
<h3>Compositional Skills</h3>
<p>Skills are performative. When you create a skill for the model, you're
teaching it how to do something: "write me a song," "rearrange words in a sentence" or
"summarize an email."</p>
<p>There are two types of compositional skills:</p>
<h4>Freeform Compositional Skills</h4>
<p>Freeform compositional skills are performative and do <strong>not</strong> require additional context. An example of a freeform skill is teaching the model words that rhyme. You could provide examples of "words that rhyme with 'tool'". By providing those examples, you're essentially tickling the latent knowledge of the LLM. In our example, you're enabling the LLM to be able to identify words that rhyme in its latent knowledge.</p>
<p>Freeform skills include things like:</p>
<ul>
<li>Speak like Yoda</li>
<li>Convert to camel case</li>
<li>Write me a limerick</li>
<li>Generate StabeDiffusion prompts</li>
</ul>
<h4>Grounded Compositional Skills</h4>
<p>Grounded skills are performative and <strong>do</strong> require additional context. An
example of a grounded skill would be to read the value of a cell in a table
layout, or to parse a JSON file. To create a grounded skill to read a
markdown formatted table layout, the additional context could be an example
table layout. This additional context is including in the YAML for the
skill and not external to it.</p>
<blockquote>
<p>[!NOTE]
The content of the table layout will not be used in training
or aligning the model; only the table layout format itself will be used.</p>
</blockquote>
<p>Grounded skills include things like:</p>
<ul>
<li>Game creation like Sudoku or tic tac toe</li>
<li>Summarizing or extracting from a piece of text</li>
<li>Find unresolved items in a meeting transcript</li>
</ul>
<p><a href="https://github.com/instructlab/taxonomy/pull/250">Example Grounded compositional skill pull request</a></p>
<h3>Core Skills</h3>
<p>Core skills are foundational skills like math, reasoning, and coding.</p>
<blockquote>
<p>[!NOTE]
Unlike <strong>knowledge</strong> and <strong>compositional skills</strong>, core skills
are not contributable to the tree. So when you see reference to contributing
"skills" to the taxonomy from this point forward, it is <strong>compositional
skills</strong> that are being referenced.</p>
</blockquote>
<h2>Accepted Skills</h2>
<h3>Creative Writing / Poetics</h3>
<p>Adding new types of documents and writing styles to the LLM are welcome. Consider:</p>
<ul>
<li>Song lyrics</li>
<li>Soliloquies</li>
<li>Five paragraph essays</li>
<li>Arguments</li>
</ul>
<h3>Learning to Format Information</h3>
<p>Skills to better format and reassemble information are helpful.</p>
<h3>Table Analysis and Processing</h3>
<p>Consider:</p>
<ul>
<li>Drawing verbal inferences and conclusions about what's in a table</li>
<li>Sorting</li>
<li>Selecting</li>
<li>Joining</li>
</ul>
<h3>Qualitative Inference and Chain-of-Thought Reasoning</h3>
<p>Example:</p>
<blockquote>
<p>Mary is taller than John.
John is taller than Anna.
Is Anna taller than Mary?</p>
</blockquote>
<p>Example:</p>
<blockquote>
<p>An elephant, a mouse and a horse are in a room. How would they be ordered if they were standing in order by size?</p>
</blockquote>
<p>Great skills in this category should include the correct line of reasoning in the answer, not just what the answer is.</p>
<h3>Word Problems</h3>
<p>Is your LLM smarter than a second grader?</p>
<h3>Trust and Safety</h3>
<p>Please avoid HAP (hate, abuse and profanity) and PII (personal identifiable information) in your examples.</p>
<p>Anything related to trust and safety will be flagged for higher-level review.</p>
<h3>Searching, Extraction and Summarization</h3>
<p>Skills to select odd information in a document, draw conclusions, pull out information, draw insights or generate TODOs from information provided in the "context" field are welcome.</p>
<h3>Complex Rulesets and Games</h3>
<blockquote>
<p>[!NOTE]
This is a good example of the need for a <em>grounded skill</em>. Grounded skills require the user to provide context containing information that the model is expected to take into account during processing. This is different from <em>knowledge</em>, where the model is expected to gain facts and background knowledge from the tuning process.</p>
<p>Context added when tuning a grounded skill would need to be again provided by the end user at inference time. The skill here is better adherence to the rule set.</p>
</blockquote>
<p>To add a skill for a structured game or other task with a complex rule set, use a grounded skill. Add the rules to the game as "context" in every example. Add the interpretation as a question.</p>
<h3>Writing Style and Personalities</h3>
<p>When adding a skill, expect that you're tuning a fairly general purpose LLM to behave better given particular circumstances.</p>
<p>If you want to add a skill to better adopt a particular personality - say, "a little boy living in the 1800s" - that context needs to be provided in either the "context" or "question" field.</p>
<h3>Instruction-Following Behavior</h3>
<p>LLMs could be better at following extra instructions in a prompt about how to do a task, such as: "Keep your response to 200 words." Or: "Only produce 10 items." Skills to improve this behavior will help the model behave with more precision.</p>
<h2>Skills to Avoid</h2>
<p>There are several types of skills that we don't expect this procedure to improve. Most skills in these categories will be rejected.</p>
<h3>Math</h3>
<p>Trying to make the LLM solve math problems will be rejected.</p>
<h3>Real world knowledge-based skills</h3>
<p>Unless it can be framed as a "grounded skill", where the user is expected to provide context, knowledge contributions will be a separate part of the taxonomy. Skills shouldn't expect the model to come up with its own facts, but instead assemble facts provided.</p>
<h3>Red Teaming</h3>
<p>Adversarial questions and answers will be rejected at this time.</p>
<h3>Turing-complete style problems</h3>
<p>These are an edge case, but things like palindromes and regexes, where getting the right answer with a non-stochastic program would be easy, aren't good targets for the moment.</p>
<p>Open an issue in the taxonomy repository if you have an idea in this space before submitting a PR.</p>
<h3>Small Changes to Original Response</h3>
<p>If the original LLM response is pretty close, but it's not responding to your exact expectations, a skill is not the right way to solve that problem.</p>
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
<li>Jokes</li>
<li>Poems</li>
<li>Code</li>
<li>Anything code-related that can be traced back to code for a computer. Not limited to <code>sed</code> or <code>bash</code> but <code>yaml</code>s for OpenShift or Kubernetes, to <code>python</code> snippets to <code>Java</code> suggestions. There are specific models focused on this space and this isn't for this model for the time being.</li>
<li>"Guard Rails" for AI</li>
<li>We expect our upstream engineering team to create these types of skills and safe guards. We appriciate our community wanting to help with this, but there are underlying engineering decisions and taking this from the community may conflict with these.</li>
</ul>
<p>We received so many at the beginning, and with jokes being "in the eye of the beholder" and puns requiring nuance for native English speakers, we realized we were possibly unconsciously biasing our model. We have discovered that working with both topics has its own challenges, and if we want something generalized, finding consensus was unsuccessful.</p>
<h2>Building Your LLM Intuition</h2>
<p>LLMs have inherent limitations that make certain tasks extremely difficult, like doing math problems. They're great at other tasks, like creative writing. And they could be better at things like logical reasoning.</p>
<p>Consider these when you're generating skills. Skills in the first and second categories are welcomed. Skills in the third category are usually borderline and may be rejected.</p>
<h3>LLMs are great at</h3>
<p>Skills in this category are welcomed, as refining these abilities helps us get better at the kinds of tasks where LLMs can excel.</p>
<p>For these, however, it's common for LLMs to already have excellent performance. Try 3-5 examples in <code>lab chat</code> to confirm a deficit in the model before you build your submission, and share the examples in your Pull Request (PR).</p>
<ul>
<li>Brainstorming</li>
<li>Creativity</li>
<li>Connecting information</li>
<li>Cross-lingual behavior</li>
</ul>
<h3>LLMs need help with</h3>
<p>Skills in this category are welcomed, since LLM behavior in these sorts of topics are very difficult for the model to get right. Try several examples to understand the nuances of the model's ability to do these sorts of tasks, and consider using corrections to the results you get in your tuning process.</p>
<ul>
<li>Chains of reasoning</li>
<li>Analysis</li>
<li>Story plots</li>
<li>Reassembling information</li>
<li>Effective and succinct summaries</li>
</ul>
<h3>LLMs are not so great at</h3>
<p>Skills in this category are ways in which LLMs struggle, and may always struggle. Solving math and computation problems via probability on natural language queries is probably not the best way to solve them. That said, improving some of these foundational skills may be something this work tackles in the future, but not at this time.</p>
<p>Most skill submissions in these categories are likely to be rejected.</p>
<p>For hallucinations in particular, trying to solve this with a skill is unlikely to work. Consider contributing to the Knowledge taxonomy when it opens instead to improve the model's understanding of facts.</p>
<ul>
<li>Math</li>
<li>Computation</li>
<li>"Turing-complete" type tasks</li>
<li>Generating only true real-world information (they're prone to hallucinations)</li>
</ul>