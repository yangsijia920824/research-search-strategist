# Query Patterns And Decisions

## Core Pattern

```text
(A1 OR A2 OR A3) AND (B1 OR B2) AND (C1 OR C2)
```

Use `OR` for alternative expressions of one concept. Use `AND` for distinct concepts.

## Diagnostic Ladder

1. `A` in title.
2. `(A1 OR A2)` in title.
3. `(A1 OR A2) AND B` in title.
4. Expand one concept to topic/title-abstract-keyword.
5. Expand the full query if volume remains manageable.
6. If volume explodes, restore one important concept to title scope or split the query.

## Too Few Results

Try, one change at a time:

- remove quotation marks;
- remove a concept;
- broaden title to topic/title-abstract-keyword;
- replace a category with its functional description;
- include formulas, abbreviations, named entities, or specific members;
- search complementary fragments separately;
- search adjacent fields and transfer their methods.

## Too Many Results

Try, one change at a time:

- add an indispensable concept with `AND`;
- move a discriminating concept to title scope;
- quote a phrase whose words should be adjacent;
- remove an ambiguous or low-value `OR` term;
- add a justified application, outcome, method, or population constraint;
- exclude a demonstrated irrelevant phrase with `NOT`;
- split the task into complementary searches.

## Low Relevance

Inspect why each irrelevant result matched:

- polysemy;
- substring wildcard collision;
- words separated across unrelated contexts;
- category term used in another discipline;
- formula fragments embedded in ordinary words.

Fix the observed cause rather than adding arbitrary restrictions.

## Scope Choice

Use title scope when:

- the concept is central enough to appear in a relevant paper's title;
- topic search produces excessive noise;
- title samples retrieve known sentinel papers.

Use topic/title-abstract-keyword when:

- authors may name only a specific material, species, product, or method in the title;
- known relevant papers mention the concept only in abstracts or keywords;
- the result volume remains processable.

Mix scopes when one concept is highly discriminating and another is often implicit.

## `NOT` Safety

Before using `NOT`:

1. inspect multiple records containing the candidate exclusion;
2. verify the phrase is consistently irrelevant;
3. use the narrowest exact phrase possible;
4. retest known relevant sentinel records after exclusion.

## Complementary Fragment Pattern

For a detailed topic `A+B+C+D`, consider:

```text
Query 1: A + B + D
Query 2: A + C + D
Query 3: A + C1 + D
```

Each result set supplies a part of the final research design. Merge and deduplicate them
instead of requiring one paper to match the entire planned study.

## Search Log

```text
Date | Database | Query | Scope | Count | Sample | Finding | Next change
```

Always attach a date to result counts because database coverage changes.
