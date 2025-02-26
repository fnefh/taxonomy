<h1>InstructLab 🐶 Taxonomy</h1>
<h2>Contents 📖</h2>
<ul>
<li><a href="#welcome-to-the-instructlab-taxonomy">Welcome to the InstructLab Taxonomy</a></li>
<li><a href="#learning">Learning</a></li>
<li><a href="#getting-started-with-skill-contributions">Getting Started with Skill Contributions</a></li>
<li><a href="#skills-yaml-examples">Skills: YAML examples</a></li>
<li><a href="#getting-started-with-knowledge-contributions">Getting Started with Knowledge Contributions</a></li>
<li><a href="#knowledge-yaml-examples">Knowledge: YAML examples</a></li>
<li><a href="#taxonomy-tree-layout">Taxonomy tree layout</a></li>
<li><a href="#contribute-knowledge-and-skills-to-the-taxonomy">Contribute knowledge and skills to the taxonomy!</a></li>
<li><a href="#ways-to-contribute">Ways to contribute</a></li>
<li><a href="#how-to-contribute-skills-and-knowledge">How to contribute skills and knowledge</a></li>
</ul>
<h2>Welcome to the InstructLab Taxonomy</h2>
<p>InstructLab 🐶 uses a novel synthetic data-based alignment tuning method for
Large Language Models (LLMs.) The "<strong>lab</strong>" in Instruct<strong>Lab</strong> 🐶 stands for
<a href="https://arxiv.org/abs/2403.01081"><strong>L</strong>arge-Scale <strong>A</strong>lignment for Chat<strong>B</strong>ots</a> [1].</p>
<p>The LAB method is driven by taxonomies, which are largely created manually and
with care.</p>
<p>This repository contains a taxonomy tree that allows you to create models
tuned with your data (enhanced via synthetic data generation) using the LAB 🐶
method.</p>
<p>[1] Shivchander Sudalairaj<em>, Abhishek Bhandwaldar</em>, Aldo Pareja<em>, Kai Xu, David D. Cox, Akash Srivastava</em>. "LAB: Large-Scale Alignment for ChatBots", arXiv preprint arXiv: 2403.01081, 2024. (* denotes equal contributions)</p>
<h2>Choosing domains for the taxonomy</h2>
<p>In general, we use the Dewey Decimal Classification (DDC) System to determine our domains (and subdomains) in the taxonomy. This <a href="https://www.oclc.org/content/dam/oclc/dewey/resources/summaries/deweysummaries.pdf">DDC SUMMARIES document</a> is a great resource for determining where a topic might be classified.</p>
<p>If you are unsure where to put your knowledge or compositional skill, create a folder in the <code>miscellaneous_unknown</code> folder under the <code>knowledge</code> or <code>compositional_skills</code> folders.</p>
<h2>Learning</h2>
<p>Learn about the concepts of "skills" and "knowledge" in our <a href="https://github.com/instructlab/community/blob/main/docs/README.md">InstructLab Community Learning Guide</a>.</p>
<h2>Getting Started with Skill Contributions</h2>
<p>Skills require a much smaller volume of content than knowledge contributions. An entire skill contribution to the taxonomy tree can be just a few lines of YAML in the <code>qna.yaml</code> file ("qna" is short for "questions and answers") and an <code>attribution.txt</code> file for citing sources.</p>
<p>Your skills contribution pull requests must include the following:</p>
<ul>
<li>A <code>qna.yaml</code> that contains a set of key/value entries with the following keys</li>
<li>Each <code>qna.yaml</code> file requires a minimum of five question and answer pairs.</li>
<li>An <code>attribution.txt</code> that includes the sources for the information used in the <code>qna.yaml</code></li>
</ul>
<blockquote>
<p>[!TIP]
The skill taxonomy structure is used in several ways:</p>
<ol>
<li>To select the right subset of the taxonomy to use for data generation.</li>
<li>To determine the interpretability by human contributors and maintainers.</li>
<li>As part of the prompt to the LLM used to generate synthetic samples.</li>
</ol>
</blockquote>
<!-- -->
<blockquote>
<p>[!IMPORTANT]
There is a limit to how much content can exist in the question/answer pairs for the model to process. Due to this, only add a maximum
of around 2300 words to your question and answer seed example pairs in the <code>qna.yaml</code> file.</p>
</blockquote>
<p>Compositional skills can either be grounded (includes a context) or ungrounded (does not include a context).  Grounded or ungrounded is declared in the taxonomy tree, for example: <code>linguistics/writing/poetry/haiku/</code> (ungrounded) or <code>grounded/linguistics/grammar</code> (grounded). The <code>qna.yaml</code> is in the final node.</p>
<p>Taxonomy skill files must be a valid <a href="https://yaml.org/">YAML</a> file named <code>qna.yaml</code>. Each <code>qna.yaml</code> file contains a set of key/value entries with the following keys:</p>
<ul>
<li><code>version</code>: The value must be the number 2. <strong>Required</strong></li>
<li><code>task_description</code>: A description of the skill. <strong>Required</strong></li>
<li><code>created_by</code>: The GitHub username of the contributor. <strong>Required</strong></li>
<li><code>seed_examples</code>: A collection of key/value entries. New
  submissions should have at least five entries, although
  older files may have fewer. <strong>Required</strong></li>
<li><code>context</code>: Grounded skills require the user to provide context containing information that the model is expected to take into account during processing. This is different from knowledge, where the model is expected to gain facts and background knowledge from the tuning process. The context key should not be used for ungrounded skills.</li>
<li><code>question</code>: A question for the model. <strong>Required</strong></li>
<li><code>answer</code>: The desired response from the model. <strong>Required</strong></li>
</ul>
<p>Other keys at any level are currently ignored.</p>
<h3>Skills: YAML examples</h3>
<p>To make the <code>qna.yaml</code> files easier and faster for humans to read, it is recommended to specify <code>version</code> first, followed by <code>task_description</code>, then <code>created_by</code>, and finally <code>seed_examples</code>.
In <code>seed_examples</code>, it is recommended to specify <code>context</code> first (if applicable), followed by <code>question</code> and <code>answer</code>.</p>
<p><em>Example <code>qna.yaml</code></em></p>
<p><code>yaml
version: 2
task_description: &lt;string&gt;
created_by: &lt;string&gt;
seed_examples:
  - question: &lt;string&gt;
    answer: |
      &lt;multi-line string&gt;
  - context: |
      &lt;multi-line string&gt;
    question: &lt;string&gt;
    answer: |
      &lt;multi-line string&gt;
  ...</code></p>
<p>Then, you create an <code>attribution.txt</code> file that includes the sources of your information. These can also be self authored sources.</p>
<p><em>Example <code>attribution.txt</code></em></p>
<p><code>text
[Link to source]
[Link to work]
[License of the work]
[Creator name]</code></p>
<p>For more information on what to include in your <code>attribution.txt</code> file, see <a href="https://github.com/instructlab/taxonomy/blob/main/CONTRIBUTING.md#for-your-attributiontxt-file">For your attribution.txt file</a> in CONTRIBUTING.md.</p>
<p>If you have not written YAML before, don't be intimidated - it's just text.</p>
<blockquote>
<p>[!TIP]</p>
<ul>
<li>Spaces and indentation matter in YAML. Two spaces to indent.</li>
<li>Don't use tabs!</li>
<li>Be careful to not have trailing spaces at the end of a line.</li>
<li>Each example in <code>seed_examples</code> begins with a "-". Place this "-" in
  front of the first field (<code>question</code> or <code>context</code>). The remaining keys in the
  example should not have this "-".</li>
<li>Some special characters such as " and ' need to be escaped with backslash. This is why some
  of the lines for keys in the example YAML start the value with the '|' character followed a new line and then an indented multi-line string.
  This character disables all of the special characters in the value for the key.
  You might also want to use the '|' character for multi-line strings.</li>
<li>Consider quoting all values with " to avoid surprising YAML parser behavior
  (e.g. Yes answer can be interpreted by the parser as a boolean of <code>True</code>
  value, unless "Yes" is quoted.)</li>
<li>See https://yaml-multiline.info/ for more info.</li>
</ul>
</blockquote>
<p>It is recommended that you <strong>lint</strong>, or verify, your YAML using a tool. One linter option is <a href="https://yamllint.com">yamllint.com</a>. You can copy/paste your YAML into the box and click <strong>Go</strong> to have it analyze your YAML and make recommendations. Online tools like <a href="https://onlineyamltools.com/prettify-yaml">prettified</a> and <a href="https://jsonformatter.org/yaml-validator">yaml-validator</a> can automatically reformat your YAML to adhere to our <code>yamllint</code> PR checks, such as breaking lines longer than 120 characters.</p>
<h4>Ungrounded compositional skill: YAML example</h4>
<p><code>yaml
version: 2
task_description: 'Teach the model how to rhyme.'
created_by: juliadenham
seed_examples:
  - question: What are 5 words that rhyme with horn?
    answer: warn, torn, born, thorn, and corn.
  - question: What are 5 words that rhyme with cat?
    answer: bat, gnat, rat, vat, and mat.
  - question: What are 5 words that rhyme with poor?
    answer: door, shore, core, bore, and tore.
  - question: What are 5 words that rhyme with bank?
    answer: tank, rank, prank, sank, and drank.
  - question: What are 5 words that rhyme with bake?
    answer: wake, lake, steak, make, and quake.</code></p>
<p>Seriously, that's it.</p>
<p>Here is the location of this YAML in the taxonomy tree. Note that the YAML file
itself, plus any added directories that contain the file, is the entirety of the skill
in terms of a taxonomy contribution:</p>
<h4>Ungrounded compositional skill: Directory tree example</h4>
<p>```ascii
[...]</p>
<p>└── writing
    └── poetry
    |   └── haiku &lt;=== here it is :)
    |   |   └── qna.yaml
    |   |       attribution.txt
        [...]
    └── prose
    |   └── debate
    |   |   └── qna.yaml
    |   |       attribution.txt
    [...]</p>
<p>[...]
```</p>
<h4>Grounded compositional skill: YAML example</h4>
<p>Remember that <a href="docs/SKILLS_GUIDE.md">grounded compositional skills</a> require additional context and include a <code>context</code> field.</p>
<p>This example snippet assumes the GitHub username <code>mairin</code> and shows some of the question/answer pairs present in the actual file:</p>
<p><code>yaml
version: 2
task_description: |
    This skill provides the ability to read a markdown-formatted table.
created_by: mairin # Use your GitHub username; only one creator supported
seed_examples:
  - context: |
      | **Breed**      | **Size**     | **Barking** | **Energy** |
      |----------------|--------------|-------------|------------|
      | Afghan Hound   | 25-27 in     | 3/5         | 4/5        |
      | Labrador       | 22.5-24.5 in | 3/5         | 5/5        |
      | Cocker Spaniel | 14.5-15.5 in | 3/5         | 4/5        |
      | Poodle (Toy)   | &lt;= 10 in     | 4/5         | 4/5        |
    question: |
      Which breed has the most energy?
    answer: |
      The breed with the most energy is the Labrador.
  - context: |
      | **Name** | **Date** | **Color** | **Letter** | **Number** |
      |----------|----------|-----------|------------|------------|
      | George   | Mar 5    | Green     | A          | 1          |
      | Gráinne  | Dec 31   | Red       | B          | 2          |
      | Abigail  | Jan 17   | Yellow    | C          | 3          |
      | Bhavna   | Apr 29   | Purple    | D          | 4          |
      | Rémy     | Sep 9    | Blue      | E          | 5          |
    question: |
      What is Gráinne's letter and what is her color?
    answer: |
      Gráinne's letter is B and her color is red.
  - context: |
      | Banana | Apple      | Blueberry | Strawberry |
      |--------|------------|-----------|------------|
      | Yellow | Red, Green | Blue      | Red        |
      | Large  | Medium     | Small     | Small      |
      | Peel   | Peel       | No peel   | No peel    |
    question: |
      Which fruit is blue, small, and has no peel?
    answer: |
      The blueberry is blue, small, and has no peel.</code></p>
<h4>Grounded compositional skill: Directory tree example</h4>
<p>```ascii
[...]</p>
<p>grounded
└── technology
    └── machine_learning
        └── natural_language_processing
    |   |     └── information_extraction
    |            └── inference
    |   |            └── qualitative
    |   |               ├── sentiment
    |   |               |     └── qna.yaml
    |   |               |         attribution.txt
    │                   ├── quantitative
    │   │                   ├── table_analysis &lt;=== here it is :)
    │   |   |               |     └── qna.yaml
    │   │   │               |         attribution.txt</p>
<p>[...]
```</p>
<h2>Getting Started with Knowledge Contributions</h2>
<p>While skills are foundational or performative, knowledge is based more on answering questions that involve facts,
data, or references.</p>
<p>Knowledge is supported by documents, such as a textbook, technical manual, encyclopedia, journal, or magazine.</p>
<p>Knowledge in the taxonomy tree consists of a few more elements than skills:</p>
<blockquote>
<p>[!IMPORTANT]
If you are using InstructLab version <code>0.21.0</code> or above, you can specify PDF files in your knowledge <code>qna.yaml</code> file as a valid document type. Any previous version of InstructLab still only consumes knowledge documents in markdown format.</p>
</blockquote>
<ul>
<li>Each knowledge node in the tree has a <code>qna.yaml</code>, similar to the format of the <code>qna.yaml</code> for skills.</li>
<li>⭐ Knowledge submissions require you to create a Git repository, can be with GitHub, that contains the files of your knowledge contributions.</li>
<li>The <code>qna.yaml</code> includes parameters that contain information from your repository.</li>
</ul>
<blockquote>
<p>[!TIP]
Guidelines for Knowledge contributions</p>
<ul>
<li>Submit the most up-to-date version of the document</li>
<li>All submissions must be text, images will be ignored</li>
<li>Do not use tables in your markdown freeform contribution</li>
</ul>
</blockquote>
<p>The <code>qna.yaml</code> format must include the following fields:</p>
<ul>
<li><code>version</code>: The version of the qna.yaml file, this is the format of the file used for SDG. The value must be the number 3.</li>
<li><code>created_by</code>: Your GitHub username.</li>
<li><code>domain</code>: Specify the category of the knowledge.</li>
<li><code>seed_examples</code>: A collection of key/value entries.</li>
<li><code>context</code>: A chunk of information from the knowledge document. Each <code>qna.yaml</code> needs five <code>context</code> blocks and has a maximum word count of 500 words.</li>
<li><code>questions_and_answers</code>: The parameter that holds your questions and answers<ul>
<li><code>question</code>: Specify a question for the model. Each <code>qna.yaml</code> file needs at least three question and answer pairs per <code>context</code> chunk with a maximum word count of 250 words.</li>
<li><code>answer</code>: Specify the desired answer from the model. Each <code>qna.yaml</code> file needs at least three question and answer pairs per <code>context</code> chunk with a maximum word count of 250 words.</li>
</ul>
</li>
<li><code>document_outline</code>: Describe an overview of the document your submitting.</li>
<li><code>document</code>: The source of your knowledge contribution.</li>
<li><code>repo</code>: The URL to your repository that holds your knowledge files.</li>
<li><code>commit</code>: The SHA of the commit in your repository with your knowledge files.</li>
<li><code>patterns</code>: A list of glob patterns specifying the files in your repository. Any glob pattern that starts with <code>*</code>, such as <code>*.md</code>, must be quoted due to YAML rules. For example, <code>"*.md"</code>.</li>
</ul>
<h3>Knowledge: YAML examples</h3>
<p>```yaml
version: 3
domain: astronomy
created_by: juliadenham
seed_examples:
  - context: |
      <strong>Phoenix</strong> is a minor <a href="constellation" title="wikilink">constellation</a> in the
      <a href="southern_sky" title="wikilink">southern sky</a>. Named after the mythical
      <a href="Phoenix_(mythology)" title="wikilink">phoenix</a>, it was first depicted on a
      celestial atlas by <a href="Johann_Bayer" title="wikilink">Johann Bayer</a> in his 1603
      <em><a href="Uranometria" title="wikilink">Uranometria</a></em>. The French explorer and
      astronomer <a href="Nicolas_Louis_de_Lacaille" title="wikilink">Nicolas Louis de
      Lacaille</a> charted the brighter
      stars and gave their <a href="Bayer_designation" title="wikilink">Bayer designations</a>
      in 1756. The constellation stretches from roughly −39 degrees to −57 degrees
      <a href="declination" title="wikilink">declination</a>, and from 23.5h to 2.5h of <a href="right_ascension" title="wikilink">right
      ascension</a>. The constellations Phoenix,
      <a href="Grus_(constellation)" title="wikilink">Grus</a>,
      <a href="Pavo_(constellation)" title="wikilink">Pavo</a> and <a href="Tucana" title="wikilink">Tucana</a>,
      are known as the Southern Birds.
    questions_and_answers:
      - question: |
          What is the Phoenix constellation?
        answer: |
          Phoenix is a minor constellation in the southern sky.
      - question: |
          Who charted the Phoenix constellation?
        answer: |
          The Phoenix constellation was charted by french explorer and
          astronomer Nicolas Louis de Lacaille.
      - question: |
          How far does the Phoenix constellation stretch?
        answer: |
          The phoenix constellation stretches from roughly −39° to −57°
          declination, and from 23.5h to 2.5h of right ascension.
  - context: |
      Phoenix was the largest of the 12 constellations established by <a href="Petrus_Plancius" title="wikilink">Petrus
      Plancius</a> from the observations of <a href="Pieter_Dirkszoon_Keyser" title="wikilink">Pieter
      Dirkszoon Keyser</a> and <a href="Frederick_de_Houtman" title="wikilink">Frederick de
      Houtman</a>. It first appeared on a 35cm
      diameter celestial globe published in 1597 (or 1598) in Amsterdam by
      Plancius with <a href="Jodocus_Hondius" title="wikilink">Jodocus Hondius</a>. The first
      depiction of this constellation in a celestial atlas was in <a href="Johann_Bayer" title="wikilink">Johann
      Bayer</a>'s
      <em><a href="Uranometria" title="wikilink">Uranometria</a></em> of 1603. De Houtman included
      it in his southern star catalog the same year under the Dutch name <em>Den
      voghel Fenicx</em>, "The Bird Phoenix", symbolising the
      <a href="Phoenix_(mythology)" title="wikilink">phoenix</a> of classical mythology. One
      name of the brightest star <a href="Alpha_Phoenicis" title="wikilink">Alpha
      Phoenicis</a>—Ankaa—is derived from the Arabic:
      العنقاء, romanized: al-‘anqā’, lit. 'the phoenix', and
      was coined sometime after 1800 in relation to the constellation.
    questions_and_answers:
      - question: |
          What is the brightest star in the Phoenix constellation
          called?
        answer: |
          Alpha Phoenicis or Ankaa is the brightest star in the Phoenix
          Constellation.
      - question: Where did the Phoenix constellation first appear?
        answer: |
          The Phoenix constellation first appeared on a 35-cm diameter
          celestial globe published in 1597 (or 1598) in Amsterdam by
          Plancius with Jodocus Hondius.
      - question: |
          What does "The Bird Phoenix" symbolize?
        answer: |
          "The Bird Phoenix" symbolizes the phoenix of classical mythology.
  - context: |
      Phoenix is a small constellation bordered by <a href="Fornax" title="wikilink">Fornax</a>
      and Sculptor to the north, Grus to the west, Tucana to the south,
      touching on the corner of <a href="Hydrus" title="wikilink">Hydrus</a> to the south, and
      <a href="Eridanus_(constellation)" title="wikilink">Eridanus</a> to the east and
      southeast. The bright star <a href="Achernar" title="wikilink">Achernar</a> is
      nearby. The three-letter abbreviation for the constellation, as
      adopted by the <a href="International_Astronomical_Union" title="wikilink">International Astronomical
      Union</a> in 1922, is
      "Phe". The official constellation boundaries, as set by Belgian
      astronomer <a href="Eugène_Joseph_Delporte" title="wikilink">Eugène Delporte</a> in 1930,
      are defined by a polygon of 10 segments. In the <a href="equatorial_coordinate_system" title="wikilink">equatorial coordinate
      system</a>, the <a href="right_ascension" title="wikilink">right
      ascension</a> coordinates of these borders lie
      between 23<sup>h</sup> 26.5<sup>m</sup> and 02<sup>h</sup> 25.0<sup>m</sup>,
      while the <a href="declination" title="wikilink">declination</a>
      coordinates are between −39.31° and −57.84°. This means it remains
      below the horizon to anyone living north of the <a href="40th_parallel_north" title="wikilink">40th
      parallel</a> in the <a href="Northern_Hemisphere" title="wikilink">Northern
      Hemisphere</a>, and remains low in the sky
      for anyone living north of the <a href="equator" title="wikilink">equator</a>. It is most
      visible from locations such as Australia and South Africa during late
      <a href="Southern_Hemisphere" title="wikilink">Southern Hemisphere</a> spring. Most
      of the constellation lies within, and can be located by, forming a
      triangle of the bright stars Achernar, <a href="Fomalhaut" title="wikilink">Fomalhaut</a>
      and <a href="Beta_Ceti" title="wikilink">Beta Ceti</a>—Ankaa lies roughly in the centre
      of this.
    questions_and_answers:
      - question: What are the characteristics of the Phoenix constellation?
        answer: |
          Phoenix is a small constellation bordered by Fornax and Sculptor to
          the north, Grus to the west, Tucana to the south, touching on the
          corner of Hydrus to the south, and Eridanus to the east and southeast.
          The bright star Achernar is nearby.
      - question: |
          When is the phoenix constellation most visible?
        answer: |
          Phoenix is most visible from locations such as Australia and
          South Africa during late Southern Hemisphere spring.
      - question: |
          What are the Phoenix Constellation boundaries?
        answer: |
          The official constellation boundaries for Phoenix, as set by Belgian
          astronomer Eugène Delporte in 1930, are defined by a polygon of 10
          segments.
  - context: |
      Ten stars have been found to have planets to date, and four planetary
      systems have been discovered with the <a href="SuperWASP" title="wikilink">SuperWASP</a>
      project. <a href="HD_142" title="wikilink">HD 142</a> is a yellow giant that has an
      apparent magnitude of 5.7, and has a planet (<a href="HD_142_b" title="wikilink">HD 142b</a>) 1.36 times the mass of Jupiter which orbits every 328 days.
      <a href="HD_2039" title="wikilink">HD 2039</a> is a yellow subgiant with an apparent
      magnitude of 9.0 around 330 light years away which has a planet (<a href="HD_2039_b" title="wikilink">HD 2039
      b</a>) six times the mass of Jupiter. <a href="WASP-18" title="wikilink">WASP-18</a> is a star of magnitude 9.29 which was discovered to have a hot
      Jupiter-like planet (<a href="WASP-18b" title="wikilink">WASP-18b</a>) taking less than a
      day to orbit the star. The planet is suspected to be causing WASP-18 to
      appear older than it really is. <a href="WASP-4" title="wikilink">WASP-4</a> and
      <a href="WASP-5" title="wikilink">WASP-5</a> are solar-type yellow stars around 1000
      light years distant and of 13th magnitude, each with a single planet
      larger than Jupiter. <a href="WASP-29" title="wikilink">WASP-29</a> is an orange
      dwarf of spectral type K4V and visual magnitude 11.3, which has a
      planetary companion of similar size and mass to Saturn. The planet
      completes an orbit every 3.9 days.
    questions_and_answers:
      - question: In the Phoenix constellation, how many stars have planets?
        answer: |
          In the Phoenix constellation, ten stars have been found to have
          planets to date, and four planetary systems have been discovered
          with the SuperWASP project.
      - question: |
          What is HD 142?
        answer: |
          HD 142 is a yellow giant that has an apparent magnitude of 5.7, and
          has a planet (HD 142 b) 1.36 times the mass of Jupiter which
          orbits every 328 days.
      - question: |
          Are WASP-4 and WASP-5 solar-type yellow stars?
        answer: |
          Yes, WASP-4 and WASP-5 are solar-type yellow stars around 1000 light
          years distant and of 13th magnitude, each with a single planet
          larger than Jupiter.
  - context: |
      The constellation does not lie on the
      <a href="galactic_plane" title="wikilink">galactic plane</a> of the Milky Way, and there
      are no prominent star clusters. <a href="NGC_625" title="wikilink">NGC 625</a> is a dwarf
      <a href="irregular_galaxy" title="wikilink">irregular galaxy</a> of apparent magnitude 11.0
      and lying some 12.7 million light years distant. Only 24000 light years in
      diameter, it is an outlying member of the <a href="Sculptor_Group" title="wikilink">Sculptor Group</a>. NGC 625 is thought to have been involved in a collision and
      is experiencing a burst of <a href="Active_galactic_nucleus" title="wikilink">active star formation</a>. <a href="NGC_37" title="wikilink">NGC 37</a> is a
      <a href="lenticular_galaxy" title="wikilink">lenticular galaxy</a> of apparent magnitude
      14.66. It is approximately 42 <a href="kiloparsecs" title="wikilink">kiloparsecs</a>
      (137,000 <a href="light-years" title="wikilink">light-years</a>) in diameter and about
      12.9 billion years old. <a href="Robert's_Quartet" title="wikilink">Robert's Quartet</a>
      (composed of the irregular galaxy <a href="NGC_87" title="wikilink">NGC 87</a>, and three
      spiral galaxies <a href="NGC_88" title="wikilink">NGC 88</a>, <a href="NGC_89" title="wikilink">NGC 89</a>
      and <a href="NGC_92" title="wikilink">NGC 92</a>) is a group of four galaxies located
      around 160 million light-years away which are in the process of colliding
      and merging. They are within a circle of radius of 1.6 arcmin,
      corresponding to about 75,000 light-years. Located in the galaxy ESO
      243-49 is <a href="HLX-1" title="wikilink">HLX-1</a>, an
      <a href="intermediate-mass_black_hole" title="wikilink">intermediate-mass black hole</a>—the first one of its kind identified. It is thought to be a
      remnant of a dwarf galaxy that was absorbed in a
      <a href="Interacting_galaxy" title="wikilink">collision</a> with ESO 243-49. Before its
      discovery, this class of black hole was only hypothesized.
    questions_and_answers:
      - question: |
          Is the Phoenix Constellation part of the Milky Way?
        answer: |
          The Phoenix constellation does not lie on the galactic plane of
          the Milky Way, and there are no prominent star clusters.
      - question: |
          How many light years away is NGC 625?
        answer: |
          NGC 625 is 24000 light years in diameter and is an outlying
          member of the Sculptor Group.
      - question: |
          What is Robert's Quartet composed of?
        answer: |
          Robert's Quartet is composed of the irregular galaxy NGC 87,
          and three spiral galaxies NGC 88, NGC 89 and NGC 92.
document_outline: |
  Information about the Phoenix Constellation including the
  history, characteristics, and features of the stars in the constellation.
document:
  repo: https://github.com/juliadenham/Summit_knowledge
  commit: 0a1f2672b9b90582e6115333e3ed62fd628f1c0f
  patterns:
    - phoenix_constellation.md</p>
<p>```</p>
<p><em>Example <code>attribution.txt</code> file</em></p>
<p><code>text
Title of work: Phoenix (constellation)
Link to work: https://en.wikipedia.org/wiki/Phoenix_(constellation)
Revision: https://en.wikipedia.org/w/index.php?title=Phoenix_(constellation)&amp;oldid=1237187773
License of the work: CC-BY-SA-4.0
Creator names: Wikipedia Authors</code></p>
<p>This knowledge example references one markdown file: <code>phoenix_constellation.md</code>. You can also add multiple files for knowledge contributions.</p>
<blockquote>
<p>[!NOTE]
Due to the higher volume, <strong>it will naturally take longer to receive acceptance for
a knowledge contribution pull request than for a skill pull request</strong>. Smaller
pull requests are simpler and require less time and effort to review.</p>
</blockquote>
<p>What might these markdown files look like? They can be freeform. Here's what a
snippet of <code>phoenix_constellation.md</code> might look like in your Git repository.</p>
<h4>Knowledge: Markdown file example</h4>
<p>```markdown</p>
<h1>Phoenix (constellation)</h1>
<p><strong>Phoenix</strong> is a minor <a href="constellation" title="wikilink">constellation</a> in the
<a href="southern_sky" title="wikilink">southern sky</a>. Named after the mythical
<a href="Phoenix_(mythology)" title="wikilink">phoenix</a>, it was first depicted on a
celestial atlas by <a href="Johann_Bayer" title="wikilink">Johann Bayer</a> in his 1603
<em><a href="Uranometria" title="wikilink">Uranometria</a></em>. The French explorer and
astronomer <a href="Nicolas_Louis_de_Lacaille" title="wikilink">Nicolas Louis de
Lacaille</a> charted the brighter
stars and gave their <a href="Bayer_designation" title="wikilink">Bayer designations</a>
in 1756. The constellation stretches from roughly −39 degrees to −57 degrees
<a href="declination" title="wikilink">declination</a>, and from 23.5h to 2.5h of <a href="right_ascension" title="wikilink">right
ascension</a>. The constellations Phoenix,
<a href="Grus_(constellation)" title="wikilink">Grus</a>,
<a href="Pavo_(constellation)" title="wikilink">Pavo</a> and <a href="Tucana" title="wikilink">Tucana</a>,
are known as the Southern Birds.</p>
<p>The brightest star, <a href="Alpha_Phoenicis" title="wikilink">Alpha Phoenicis</a>, is
named Ankaa, an <a href="Arabic" title="wikilink">Arabic</a> word meaning 'the Phoenix'.
It is an orange giant of apparent magnitude 2.4. Next is <a href="Beta_Phoenicis" title="wikilink">Beta
Phoenicis</a>, actually a
<a href="Binary_star" title="wikilink">binary</a> system composed of two yellow giants
with a combined apparent magnitude of 3.3. <a href="Nu_Phoenicis" title="wikilink">Nu
Phoenicis</a> has a dust disk, while the
constellation has ten star systems with known planets and the recently
discovered <a href="galaxy_cluster" title="wikilink">galaxy clusters</a> <a href="El_Gordo_(galaxy_cluster)" title="wikilink">El
Gordo</a> and the <a href="Phoenix_Cluster" title="wikilink">Phoenix
Cluster</a>—located 7.2 and 5.7 billion light
years away respectively, two of the largest objects in the <a href="visible_universe" title="wikilink">visible
universe</a>. Phoenix is the
<a href="radiant_(meteor_shower)" title="wikilink">radiant</a> of two annual <a href="meteor_shower" title="wikilink">meteor
showers</a>: the
<a href="Phoenicids" title="wikilink">Phoenicids</a> in December, and the July
Phoenicids.
```</p>
<p>In the taxonomy repository, here's what the previously referenced knowledge might look like in the tree:</p>
<h4>Knowledge: directory tree example</h4>
<p>```ascii
[...]</p>
<p>└── knowledge
    └── science
        ├── astronomy
        │ └── constellations
        │     └── Phoenix &lt;=== here it is :)
        │     |    └── qna.yaml
        |     |        attribution.txt
        │     └── Orion
        │          └── qna.yaml
        |              attribution.txt
[...]
```</p>
<p>For more information on what to include in your <code>attribution.txt</code> file, see <a href="https://github.com/instructlab/taxonomy/blob/main/CONTRIBUTING.md#for-your-attributiontxt-file">For your attribution.txt file</a> in CONTRIBUTING.md.</p>
<p>You can organize the knowledge markdown files in your repository however you want. You just need to ensure the YAML is pointing to the correct file.</p>
<h2>Taxonomy tree Layout</h2>
<p>The taxonomy tree is organized in a cascading directory structure. At the end of
each branch, there is a YAML file (qna.yaml) that contains the examples for that
domain. Maintainers can decide to change the names of the existing branches or to add new branches.</p>
<blockquote>
<p>[!IMPORTANT]
Folder names do not have spaces. Use underscores between words.</p>
</blockquote>
<p>Below is an illustrative directory structure to show this layout:</p>
<p><code>ascii
.
└── linguistics
    ├── writing
    │   ├── brainstorming
    │   │   ├── idea_generation
    |   │       └── qna.yaml
    │   │           attribution.txt
    │   │   ├── refute_claim
    |   │       └── qna.yaml
    │   │           attribution.txt
    │   ├── prose
    │   │   ├── articles
    │   │       └── qna.yaml
    │   │           attribution.txt
    └── grammar
        └── qna.yaml
        │   attribution.txt
        └── spelling
            └── qna.yaml
                attribution.txt</code></p>
<p>For an extensive example of this layout see, <a href="docs/taxonomy_diagram.md">taxonomy_tree_layout</a> in the documentation folder.</p>
<h2>Contribute knowledge and skills to the taxonomy</h2>
<p>The ability to contribute to a Large Language Model (LLM) has been difficult in no small part because it is difficult to get access to the necessary compute infrastructure.</p>
<p>This taxonomy repository will be used as the seed to synthesize the training data for InstructLab-trained models. We intend to retrain the model(s) using the main branch following InstructLab's progressive training on a regular basis. This enables fast iteration of the model(s), for the benefit of the open source community.</p>
<p>By contributing your skills and knowledge to this repository, you will see your changes built into an LLM within days of your contribution rather than months or years! If you are working with a model and notice its knowledge or ability lacking, you can correct it by contributing knowledge or skills and check if it's improved after your changes are built.</p>
<p>While public contributions are welcome to help drive community progress, you can also fork this repository under <a href="LICENSE">the Apache License, Version 2.0</a>, add your own internal skills, and train your own models internally. However, you might need your own access to significant compute infrastructure to perform sufficient retraining.</p>
<h2>Ways to Contribute</h2>
<p>You can contribute to the taxonomy in the following two ways:</p>
<ol>
<li>Adding new examples to <strong>existing leaf nodes</strong>:</li>
<li>Adding <strong>new branches/skills</strong> corresponding to the existing domain:</li>
</ol>
<p>For more information, see the <a href="https://github.com/instructlab/taxonomy/blob/main/CONTRIBUTING.md#ways-of-contributing-to-the-taxonomy-repository">Ways of contributing to the taxonomy repository</a> documentation.</p>
<h2>How to contribute skills and knowledge</h2>
<p>To contribute to this repo, you'll use the <em>Fork and Pull</em> model common in many open source repositories. You can add your skills and knowledge to the taxonomy in multiple ways; for additional information on how to make a contribution, see the <a href="CONTRIBUTING.md">Documentation on contributing</a>. You can also use the following guides to help with contributing:</p>
<ul>
<li>Contributing using the <a href="docs/contributing_via_GH_UI.md">GitHub webpage UI</a>.</li>
<li>Contributing knowledge to the taxonomy in the <a href="docs/knowledge-contribution-guide.md">Knowledge contribution guidelines</a>.</li>
</ul>
<h3>Why should I contribute?</h3>
<p>This taxonomy repository will be used as the seed to synthesize the training
data for InstructLab-trained models. We intend to retrain the model(s) using the main
branch as often as possible (at least weekly).
Fast iteration of the model(s) benefits the open source community and enables model developers who do not have access to the necessary compute infrastructure.</p>