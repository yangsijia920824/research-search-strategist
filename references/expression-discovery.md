# Expression Discovery

Use this reference when a concept has uncertain, numerous, formula-based, or hidden
expressions.

## Discovery Sequence

1. Search the native-language concept on the open web.
2. Find definitions, encyclopedia entries, books, institutional reports, and
   representative research announcements.
3. Extract actual English paper titles rather than relying only on machine translation.
4. Split long phrases into minimum semantic units.
5. Build candidate groups for each unit.
6. Test candidates in a scholarly database and inspect their dominant meanings.
7. Update the expression table from relevant titles, abstracts, and keywords.

## Expression Classes

Check for:

- singular and plural forms;
- spelling variants and hyphenation;
- abbreviations and full names;
- formulas and compositional notation;
- material or species names that replace a category name;
- instruments, satellites, datasets, models, products, or platforms that replace a
  generic method;
- process nouns, verbs, and adjectives;
- field-specific conventional wording;
- broader functional descriptions that omit the user's original noun.

## Minimum-Unit Rule

For a phrase containing multiple concepts, prefer:

```text
(A1 OR A2) AND (B1 OR B2 OR B3) AND (C1 OR C2)
```

over enumerating every phrase permutation:

```text
"A1 B1 C1" OR "A1 B1 C2" OR "A2 B3 C2" ...
```

Test whether word order matters before adding quotation marks.

## Hidden-Expression Test

Ask:

- Could an author study category `A` but mention only a specific member of `A`?
- Could an author state the method, formula, instrument, or mechanism instead of the
  category?
- Could the work be useful even if it is not labeled as the user's application?

If yes, either broaden the query, add supported named entities, or create a complementary
query. Do not attempt to exhaust an unbounded list when incremental updates are viable.

## Candidate Evidence Table

```text
Concept | Candidate | Source | Database test | Keep/reject | Reason
```

Reject candidates only after checking meaning and retrieval behavior. Dictionaries and
published papers can contain errors.
