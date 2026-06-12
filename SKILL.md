---
name: research-search-strategist
description: Design, test, refine, and document rigorous literature-search strategies for research questions across disciplines. Use when Codex needs to turn a vague topic into database-ready search queries; discover synonyms, abbreviations, formulas, named entities, or hidden expressions; apply deletion tests and Less-is-more reasoning; choose title versus topic/title-abstract-keyword scope; balance recall, relevance, and result volume; combine multiple searches as complementary evidence fragments; identify research gaps or transferable ideas; or audit why a literature search finds too few, too many, or misleading results.
---

# Research Search Strategist

Treat literature searching as iterative problem solving, not direct translation.
Optimize for a useful evidence universe that contains the important work and can be
processed efficiently. Do not promise perfect completeness.

## Start With The Research Goal

1. Restate the user's practical endpoint: orient a field, choose a topic, test novelty,
   design experiments, solve a specific problem, write a review, or build a literature
   library.
2. Preserve the user's constraints, but distinguish true requirements from wording
   inherited from a supervisor, title, or initial assumption.
3. Identify the failure mode: too few results, too many results, low relevance,
   suspected omissions, unclear terminology, or no actionable ideas.
4. Browse current databases or the web when actual search execution, current result
   counts, database syntax, or recent literature is required. Treat counts as dated
   observations, not permanent facts.

## Build A Concept Map

1. Rewrite the question as atomic concepts `A + B + C`.
2. Mark each concept as:
   - indispensable;
   - removable for a deletion test;
   - replaceable by a broader functional concept;
   - a possible application, material, method, mechanism, outcome, or population.
3. For a complex topic, define complementary fragments instead of demanding one query
   match every detail. Example: `A+B+D`, `A+C+D`, and `A+C1+D`.
4. Read [references/expression-discovery.md](references/expression-discovery.md) when
   terminology is uncertain, formula-heavy, named after instruments/products/species,
   or difficult to exhaust.

## Run Deletion Tests First

1. Start from the smallest concept that still preserves the research purpose.
2. Remove one concept at a time and inspect what newly appears.
3. Prefer deleting a term whose expressions are numerous or impossible to exhaust.
   A broader query may recover relevant work that never names that concept directly.
4. Reintroduce constraints only when result volume or irrelevant meanings become
   unmanageable.
5. Do not equate indirect relevance with irrelevance. A paper may contribute a method,
   mechanism, material, variable, model, dataset, or comparison needed for the user's
   larger research design.

## Discover Expressions

Use multiple evidence channels rather than trusting one translator or glossary:

1. General web search for definitions, English names, representative papers, product
   names, formulas, species, instruments, and field-specific language.
2. Academic dictionaries or bilingual databases for candidate expressions.
3. Titles, abstracts, and keywords from representative records.
4. Search-result feedback itself: remove a term, inspect the language used by relevant
   records, and add only expressions supported by evidence.
5. Test suspect expressions in a scholarly database. Reject mistranslations, spelling
   errors, partial words, or terms used mainly in an unrelated sense.

Record expressions by concept:

```text
A: A1 OR A2 OR A3
B: B1 OR B2
C: C1 OR C2 OR C3
```

Use wildcards only after testing database behavior. Preserve formulas and abbreviations
when authors may use them instead of names.

## Iterate Queries

Follow small, debuggable steps:

1. Test the simplest query in titles.
2. Sort by date rather than relevance when possible, so relevance is not artificially
   improved by the ranking algorithm.
3. Inspect a small unbiased sample, usually 5-20 titles. Open abstracts only when the
   title cannot answer the current test question.
4. Change one variable at a time:
   - add an `AND` concept;
   - remove a weak `OR` synonym;
   - add or remove quotation marks;
   - test a wildcard;
   - move one concept between title and topic/title-abstract-keyword;
   - add a narrowly justified `NOT`;
   - split one overloaded query into complementary queries.
5. Log the query, scope, observed count, sample relevance, discoveries, and next change.
6. Read [references/query-patterns.md](references/query-patterns.md) for syntax patterns
   and decision rules.

Default logical shape:

```text
(A1 OR A2 OR A3) AND (B1 OR B2) AND (C1 OR C2)
```

Keep synonyms for one concept within the same `OR` group. Connect distinct concepts
with `AND`. Avoid opaque logic that the researcher cannot explain.

## Decide Scope And Stopping Point

Use title search for diagnosis and precision. Expand to topic or
title-abstract-keyword when relevant work may omit the concept from its title.

Evaluate both:

- recall risk: are known relevant records missing?
- processing value: is the result set relevant enough and small enough for the intended
  downstream workflow?

Do not force a universal numeric threshold. A small emerging field may yield dozens of
records; a mature field may legitimately yield thousands. Stop refining when:

1. known sentinel records are retrieved;
2. sampled results contain a useful proportion of direct or fragment-level evidence;
3. additional restrictions would likely remove valuable work;
4. the remaining volume is processable by the user's review method.

## Use Complementary Searches

When one query cannot balance breadth and precision:

1. Create separate queries for different evidence fragments.
2. Import or merge them into one deduplicated literature library.
3. Record the source query for every batch.
4. Update incrementally when new expressions, entities, or research directions appear.
5. Do not repeatedly re-screen records already processed.

## Extract Research Value

While testing, capture:

- newly discovered terminology;
- methods transferable from adjacent fields;
- combinations of established fields with a small intersection;
- variables, mechanisms, materials, datasets, or populations that can be substituted;
- evidence that the original question is too narrow, too broad, or incorrectly framed.

Distinguish a genuine research gap from a search failure. Before claiming novelty, run
targeted sentinel searches for the proposed idea and close variants.

## Deliver A Reproducible Search Brief

Unless the user requests another format, provide:

1. research objective and working interpretation;
2. concept decomposition;
3. expression table with evidence and rejected terms;
4. query iteration log;
5. recommended final query or complementary query set;
6. databases and scopes used;
7. observed result counts with search dates;
8. known limitations and likely omission paths;
9. incremental-update plan;
10. research ideas or transferable fragments discovered during testing.

Use [references/output-template.md](references/output-template.md) for substantial
search projects.

## Guardrails

- Do not fabricate database counts, search results, paper titles, or coverage claims.
- Do not call a query exhaustive merely because it has many synonyms.
- Do not use `NOT` until excluded records have been sampled and the exclusion is shown
  not to remove important work.
- Do not read full papers during query diagnosis unless required to resolve a specific
  ambiguity.
- Do not confuse downloading records with reading every paper.
- Separate the source author's heuristics from verified database behavior and the
  current user's constraints.
