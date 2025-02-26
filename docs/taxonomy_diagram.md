<h2>Taxonomy diagram</h2>
<blockquote>
<p>[!Note]
This diagram shows a subset of the taxonomy. It is not a complete representation.</p>
</blockquote>
<p>```mermaid
flowchart TD;
na[not accepting contributions\n at this time]:::na
taxonomy --&gt; foundational_skill &amp; compositional_skills &amp; knowledge</p>
<p>foundational_skill:::na --&gt; reasoning:::na
reasoning:::na --&gt; common_sense_reasoning:::na
reasoning:::na --&gt; mathematical_reasoning:::na
reasoning:::na --&gt; theory_of_mind:::na</p>
<p>compositional_skills --&gt; engineering
compositional_skills --&gt; grounded
compositional_skills --&gt; lingustics</p>
<p>grounded --&gt; grounded/arts
grounded --&gt; grounded/geography
grounded --&gt; grounded/history
grounded --&gt; grounded/science</p>
<p>knowledge --&gt; knowledge/arts</p>
<p>knowledge --&gt; knowledge/miscellaneous_unknown
knowledge --&gt; knowledge/science
knowledge --&gt; knowledge/technology
knowledge/science --&gt; animals --&gt; birds --&gt; black_capped_chickadee --&gt; black_capped_chikadee-a &amp; black_capped_chikadee-q
knowledge/science --&gt; astronomy --&gt; constellations --&gt; phoenix --&gt; phoenix-a &amp; phoenix-q</p>
<p>black_capped_chikadee-a{attribution.txt}
black_capped_chikadee-q{qna.yaml}
phoenix-a{attribution.txt}
phoenix-q{qna.yaml}
classDef na fill:#EEE
```</p>