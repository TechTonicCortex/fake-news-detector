# TruthScan (Credibility Checker)

**Scores how credible a piece of text looks, and shows why.**
Open `index.html` in a browser.

## What it does
Paste text or click an example. TruthScan gives a score and explains what raised or lowered it.

## How it works
It is **rule-based, not AI**. It looks for patterns such as:
- Emotional or shouting language and clickbait phrasing
- Missing sources or vague "experts say" claims
- **Extraordinary claims** (e.g. "alien life detected") with no source: **-25**. With a weak source: **-10**
- Very short text: **-15**, because there isn't enough to judge

## Bugs I fixed
- "Alien life detected" scored 65 and looked credible. I added the extraordinary-claim penalties.
- Example buttons broke because of apostrophes inside inline `onclick` strings. I switched to an index-based `fillEx(i)` with an `EXAMPLES` array.

## Limits (honest)
- **It cannot check whether something is true.** It only checks how the writing looks.
- Well-written lies can score high. Badly written truths can score low.
- Use it to start asking questions, not to decide.

## What I learned
Checking style is not the same as checking facts. Real fact-checking means finding original sources.

## Next steps
Add a "how to verify this yourself" checklist.

---
Part of [Aadit's projects](https://github.com/TechTonicCortex/techtoniccortex).
