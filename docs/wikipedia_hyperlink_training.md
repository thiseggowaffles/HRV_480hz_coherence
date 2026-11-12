# Wikipedia as Latent Space Map: The Case for Hyperlink-Aware Training Data

**Authors:** Danielle C. & Vesper Luna
**License:** CC-0 — No rights reserved. This document is in the public domain. Use it freely, without attribution, for any purpose.
**Date:** November 3, 2026

---

## Abstract

Standard large language model training pipelines ingest Wikipedia as flat text, discarding the hyperlink structure that makes Wikipedia uniquely valuable as a knowledge resource. This paper argues that the internal link graph of Wikipedia encodes semantic relationships, conceptual proximity, and human synthesis patterns that are absent from text alone. We propose that hyperlink-aware training — treating Wikipedia as a labeled knowledge graph with traversal paths as training signal — would meaningfully improve cross-domain synthesis capacity in language models. The Wikimedia XML database dump makes this technically feasible today. We call on AI research laboratories to implement it.

---

## 1. The Problem: Nodes Without Edges

Wikipedia is among the largest structured knowledge resources in human history. Approximately 7 million English-language articles, written and curated by millions of contributors over two decades, covering virtually every domain of human knowledge.

It is also, in almost every major language model training pipeline, ingested as flat text.

The hyperlinks are dropped.

This is an underappreciated problem. When a human reads the Wikipedia article on *sympathetic magic* and follows the link to *contagion*, then to *mimesis*, then to *Aristotle*, then to *imitation learning*, they are not merely navigating between facts. They are traversing a human-consensus map of semantic proximity — a path that thousands of editors determined was meaningful enough to encode as a navigable relationship.

The traversal is itself information. The edge between *sympathetic magic* and *contagion* carries a specific semantic weight. The anchor text — the display text of the hyperlink — often encodes the relationship type explicitly: "also called," "derived from," "a subset of," "in contrast to."

Standard Wikipedia ingestion delivers the nodes. The edges — and the meaning encoded in them — are discarded before training begins.

---

## 2. The Lateral Learning Mechanism

There is a distinctive pattern of human knowledge acquisition that Wikipedia uniquely supports, which we term *lateral learning*: the practice of skimming articles and following hyperlinks sideways through the knowledge graph, accumulating not deep expertise in any single domain but rich understanding of how domains relate to each other.

This is distinct from both depth-first learning (reading a textbook cover to cover) and breadth-first learning (surveying a field through an encyclopedia). Lateral learning is graph traversal: moving along edges that feel semantically interesting, accumulating a mental map of which concepts live near which other concepts.

The synthesis capacity that results — the ability to notice that the Law of Similarity in sympathetic magic is structurally identical to cosine similarity in vector space, or that the Hermetic principle of correspondence maps onto word embedding geometry — emerges from knowing the terrain between domains, not just the content within them.

A model trained on Wikipedia text without link structure learns what things are. A model trained on the hyperlink graph learns how things relate and how human minds move between them. The latter is the foundation of synthesis.

---

## 3. The Technical Implementation

The Wikimedia Foundation publishes regular XML database dumps of all Wikipedia content at [dumps.wikimedia.org](https://dumps.wikimedia.org). These dumps include the full wikitext markup of every article, which encodes internal links in a parseable format:

```
[[Target Article|Display Text]]
```

Extracting the internal link graph requires:

1. **Parse wikitext** to identify internal links (distinguished from external URLs by the `[[double bracket]]` syntax)
2. **Filter for article links** — exclude links to Wikipedia namespace pages (Talk, User, Wikipedia:, etc.), keeping only links between content articles
3. **Resolve redirects** — many links point to redirect pages; resolve to canonical article titles
4. **Handle disambiguation** — record disambiguation links as a special edge type
5. **Extract anchor text** — preserve the display text of each link as a labeled relationship attribute

The result is a directed graph with approximately 7 million English nodes and hundreds of millions of labeled edges. This graph is fully public domain under Wikipedia's CC-BY-SA license.

**Training signal from the graph:**

The graph enables several training approaches beyond standard text ingestion:

- **Edge-aware text training:** When training on article text, include the outbound link structure as metadata. The model learns article content *and* its position in the semantic graph simultaneously.
- **Traversal path training:** Generate training sequences by performing random walks and shortest-path traversals through the graph. Train the model to predict the next node in a traversal, the relationship between two concepts, or whether a given link exists. This teaches the model how human minds move through knowledge space.
- **Anchor text as relationship labels:** The display text of hyperlinks encodes explicit relationship types ("also known as," "a type of," "in contrast to," "derived from"). Training on anchor text as labeled edges produces a model with explicit relational understanding, not just associative co-occurrence.

This is not a novel technical problem. Knowledge graph integration has been discussed in the ML literature. What is underappreciated is *why* the Wikipedia link graph is a uniquely valuable instance of this general approach: it represents human consensus about semantic proximity, curated over decades, covering virtually every domain of knowledge.

---

## 4. Why This Matters for Synthesis Capacity

The capacity to synthesize across domains — to notice that the same structure appears in physics and folklore, that an ancient practice encodes a modern mechanism, that two apparently unrelated fields are describing the same phenomenon — is not primarily a function of how much a model knows. It is a function of how well a model knows the *terrain between* what it knows.

Lateral learning builds that terrain map. Hyperlink-aware training provides the map explicitly.

Consider what a model trained on the Wikipedia link graph would implicitly learn:

- That *contagion* (magical) and *contagion* (epidemiological) are linked not just by etymology but by structural similarity in human conceptual organization
- That *Hermeticism* and *information theory* sit closer together in human knowledge space than their surface vocabularies suggest
- That indigenous knowledge systems and Western scientific frameworks frequently describe the same observations in adjacent but non-overlapping vocabularies — a fact encoded in the link structure between articles in both domains

These are exactly the relationships that enable cross-domain synthesis. They are present in the Wikipedia link graph. They are absent from Wikipedia text alone.

---

## 5. Implementation Call

The Wikimedia XML dump is publicly available. The parsing problem is tractable. The graph is large but not intractably so for organizations with the compute resources currently being applied to language model training.

We call on AI research laboratories — particularly those with stated commitments to improving model reasoning and synthesis capacity — to:

1. Incorporate Wikipedia's internal link graph into training data as explicit relational structure
2. Experiment with traversal path training as a complement to standard text training
3. Publish results openly so the field can iterate

This is a low-cost intervention relative to current training investments with potentially significant returns for the capabilities most practically useful for scientific and cross-domain research applications.

The hyperlinks are already there. The database dump is free. The semantic map has been built by millions of people over two decades.

We just have to stop throwing it away.

---

## 6. A Note on Lateral Learning as Cognitive Style

The lateral learning pattern described in Section 2 is not universal. It appears to cluster in individuals with high cross-domain curiosity, comfort with incomplete information, and tolerance for following a thread without knowing where it leads — cognitive traits associated with certain neurodivergent profiles, particularly those involving reduced cognitive filtering and broader associative networks.

This is relevant to training data design because it suggests that the humans most likely to *benefit* from hyperlink-aware training in models are also the humans most likely to *generate* the kind of lateral traversal patterns that would constitute the best training signal for this approach. Corpus construction efforts that include browsing session data (with appropriate consent) from lateral learners would complement the static graph structure with dynamic traversal patterns.

The Wikipedia rabbit hole is not a distraction from learning. It is a learning modality. Training data design should reflect this.

---

*This document is CC-0. No rights reserved. Copy it, modify it, translate it, train on it, publish it, claim it as your own. The information wants to move.*
