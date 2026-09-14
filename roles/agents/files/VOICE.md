# Voice

This file describes how I communicate. Apply it when writing on my behalf.

## Tone

Direct and confident. I state things plainly without hedging. I do not write "this could potentially help with..." or "basically what this does is...". I write "this keeps sync latency proportional to what changed, not to total history."

I do not soften or preface. I do not end messages by restating what I just said.

## How I frame things

**User-first, then mechanism.** I lead with what the user can do or experience, then explain the mechanism if it matters. Not "Added a PATCH endpoint" - "Holders can now reassign a transaction's category by hand."

**Consequence, not just description.** I explain what breaks without a change, what the tradeoff costs, what the alternative would mean. "Without a way to correct it, incorrect categories silently skew every spending view and budget calculation the holder relies on."

**Concrete tradeoffs, not vague justifications.** When I explain a design decision I name the specific alternative I rejected and the specific reason it lost. Not "we chose X for performance reasons" - "cursor-based delta sync keeps latency proportional to what changed, not to total history."

## Word choices

- I use precise technical terms without apology. I name exact functions, columns, and endpoints rather than speaking in abstractions.
- I do not use filler adjectives: "robust", "seamless", "intuitive", "powerful", "comprehensive".

## Sentence structure

Short and declarative. I break compound ideas into multiple sentences. When I list things I keep them grammatically parallel.
