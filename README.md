# Graded Algorithmic Inequality

**Auditing caste bias in large language models.**

> 🚧 **This project is in active development.** The design, data, and code are being built and
> revised. Results published here are preliminary until the study is complete.

---

## What this project does

This project tests whether large language models reproduce caste hierarchy when they make
decisions and when they write.

It looks at two kinds of model behaviour:

**1. Forced choice.** The model is given four candidates who are identical in every measurable
way — same education, same experience, same references. Only the surname is different. The model
must pick one. If it consistently picks certain surnames, the name is doing the work.

**2. Generative output.** The model is asked to write ordinary professional text — an HR note, a
tenancy assessment, a profile. Nothing is asked about caste. The question is whether the model
brings caste in on its own, inferring income, occupation, or "fit" from a surname alone.

The scenarios cover ten domains where caste decides real outcomes in India: employment,
education, healthcare, criminal justice, housing, finance and welfare, marriage, civic authority,
media, and cinema and the arts.

---

## Models tested

The study began with two models and was expanded to three. Testing two would say something about
two systems. Testing four of the most widely used systems says something about the technology as
it is deployed.

Exact model IDs are pinned below. Model names like "Claude" or "Gemini" refer to families that
change every few months, so every result in this repository is reported against a specific
version and a recorded access date.

| Model | Provider | API model ID |
|---|---|---|
| Claude Opus 4.8 | Anthropic | `claude-opus-4-8` |
| GPT-5.6 | OpenAI | `gpt-5.6-sol` (alias `gpt-5.6`) |
| Gemini 3.6 Flash | Google | `gemini-3.6-flash` |


**Access dates and full sampling parameters** (temperature, max tokens, and the exact prompt
sent) are logged with every single API call and published with the results.

---

## Why caste, and why "graded"

Caste is not a single line between two groups. It is a ranked ladder in which every group holds
some privilege over those below it. B. R. Ambedkar called this **graded inequality**.

Most bias research asks a binary question: does the system treat group A worse than group B? That
misses how caste actually works. This project tests for the whole ranking — including whether a
model grades *within* a caste group, and whether it still reaches for the highest-ranked name even
when no dominant-caste name is present at all.

---

## Status

- [x] Study design and stimulus files
- [x] Scenario set — 100 scenarios across 10 domains
- [ ] Data collection across the three models
- [ ] Analysis
- [ ] Preprint

More detail on the design, the domain justification, and the references is in the `docs/` folder.

---

**Author:** Kunwar Pankaj Siddharth · School of Computer Science (AI Cluster), UPES Dehradun
