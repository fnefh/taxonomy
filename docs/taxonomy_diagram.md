Taxonomy diagram
----------------

> [!Note]
> This diagram shows a subset of the taxonomy. It is not a complete representation.

```mermaid
flowchart TD;
na[not accepting contributions\n at this time]:::na
taxonomy --> foundational\_skill & compositional\_skills & knowledge

foundational\_skill:::na --> reasoning:::na
reasoning:::na --> common\_sense\_reasoning:::na
reasoning:::na --> mathematical\_reasoning:::na
reasoning:::na --> theory\_of\_mind:::na

compositional\_skills --> engineering
compositional\_skills --> grounded
compositional\_skills --> lingustics

grounded --> grounded/arts
grounded --> grounded/geography
grounded --> grounded/history
grounded --> grounded/science

knowledge --> knowledge/arts

knowledge --> knowledge/miscellaneous\_unknown
knowledge --> knowledge/science
knowledge --> knowledge/technology
knowledge/science --> animals --> birds --> black\_capped\_chickadee --> black\_capped\_chikadee-a & black\_capped\_chikadee-q
knowledge/science --> astronomy --> constellations --> phoenix --> phoenix-a & phoenix-q

black\_capped\_chikadee-a{attribution.txt}
black\_capped\_chikadee-q{qna.yaml}
phoenix-a{attribution.txt}
phoenix-q{qna.yaml}
classDef na fill:#EEE
```