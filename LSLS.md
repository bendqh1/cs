In computer science, what is the topic that describes possible changes in the execution of a code due to the code going from multilined to singlelined or vice versa? It has to do with spacing characters, line breaks, partial line breaks (as in `<br>` or anything that behaves like it), carriage returns, etc.

There should be one topic that covers it; if the literature doesn't define such a topic in a coherent way, invent a name of 2-10 words.

There might be connections to regex, but regex is much too broad of a term to cover it, I guess.

Very short answer. No waffling. No icons or emojis.

---

The closest established topic is **whitespace sensitivity** (or **layout-sensitive syntax**): how spaces, tabs, line breaks, carriage returns, and related formatting affect parsing or execution.

For the broader phenomenon you describe—including `<br>`-like partial breaks—I’d call it **line-break-sensitive semantics**.

---

Does the literature has one single definition to cover both whitespace sensitivity and/or linebreak sensitivity? Keep searching the field's literature and also check Math books if these are relevant (multilining mathematical code may change an algorithm), but mostly focus on CS literature. Short answer.

---

No. **There is no single standard CS term/definition that cleanly covers both whitespace sensitivity and line-break sensitivity.**

The closest established umbrella is **layout-sensitive syntax / layout sensitivity**: literature explicitly treats whitespace and indentation as affecting program structure.

But it does **not** uniformly cover arbitrary line-break/CR/LF changes, `<br>`-like delimiters, etc. C/C++ literature instead treats these under lexical/grammar rules for **whitespace and new-lines**.

So if you need one name for your broader phenomenon, I'd use:

**layout-sensitive semantics**

That is broader than *layout-sensitive syntax* and captures cases where changing the physical layout can change the resulting behavior/algorithm.

---

The broader topic is **lexical/syntactic sensitivity to layout**. Regex can describe or detect whitespace/line-break patterns, but it doesn't cover the semantic effects of changing them.
