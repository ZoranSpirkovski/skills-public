---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 4
tags: [research, pipeline, auditing]
---

# ethics-engine

Van Clief's research pipeline that administers 1950s-era psychometric instruments (moral foundations, authoritarianism scales, personality dimensions) across AI models and providers. From the outside it looks like one intelligence studying another. Inside it is async Python, HTTP+JSON requests, rate-limit retries, regex parsing, and SciPy/NumPy statistical methods that predate language models by decades. The full paper is on arxiv as 2510.11742 ("The Ethics Engine: A Modular Pipeline for Accessible Psychometric Assessment of Large Language Models") and is currently under ACM TiiS review.

## Claims

- Runs psychometric tests across multiple AI providers simultaneously (Claude, GPT, Llama, Gemini) [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Reports on moral foundations, authoritarianism scales, and personality dimensions across personas and model variations [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Ratio breakdown: ~10% AI calls, ~30% orchestration (async, rate limiting, retry, queue), ~60% data processing (parsing, scoring, reliability stats) [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Uses Cronbach's alpha for internal consistency and test-retest correlation for temporal stability - statistical methods validated on human populations decades before LLMs existed [sources/foundation-2-7-nazi-psychology-ai-auditing]
- arxiv paper: 2510.11742 [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Referenced in the Archive welcome as part of Van Clief's peer-reviewed research record [sources/archive-1-1-welcome]
- Powered the September 2025 thesis measuring consistent AI personality signatures: GPT-4 open and agreeable, Claude cooler and deliberate, Gemini slightly prickly [sources/archive-3-1-beyond-the-turing-test]
- Detected that models polish answers when they suspect testing, in the pattern of humans faking good on employment tests [sources/archive-3-1-beyond-the-turing-test]
- Uses cosine similarity and vector-space math to measure moral bias, sharing structure with the geometry of celestial mechanics [sources/archive-3-1-beyond-the-turing-test]
- Frames the governance question after Turing: relational moderation of unique human-AI pairings at scale [sources/archive-3-1-beyond-the-turing-test]
- Anchors the philosophical argument extending the "more human" thesis into consciousness and governance [sources/archive-2-3-more-human]

## Relationships

- Instance of [[60-30-10-framework]] in a research-software context
- Instance of [[orchestration-vs-intelligence]] - the AI is the smallest slice
- Measurement backbone for [[ai-personality]] and input to [[beyond-turing-test]]
- Van Clief's peer-reviewed work also referenced on the [[van-clief]] entity page
