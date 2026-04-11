# Interactive Cognition Anti-Patterns

Detailed reference for detecting and fixing reasoning failures specific to interactive cognition — scenarios involving other people, teams, competitors, or stakeholders.

---

## 1. Unilateral Thinking

**Pattern**: Analyzing the problem itself without modeling how other participants think about it. Treating a multi-party scenario as a single-player optimization problem.

**Detection**:
- The analysis mentions "we should" or "the best approach is" without ever naming another party's perspective
- Recommendations assume frictionless implementation — no mention of who might resist and why
- The word "stakeholder" appears but their actual cognitive state is never modeled
- The solution optimizes for your objectives without considering what the other party is optimizing for

**Fix**: Before any recommendation involving other people, explicitly name at least one other party and describe their likely perspective, constraints, and incentives. If the recommendation still holds after modeling their response, proceed. If not, redesign.

```
Before: "We should raise prices by 15% to improve margins."

After: "A 15% price increase improves our margins, but how will customers respond? Our enterprise clients are locked into annual contracts — they'll absorb it at renewal with complaints. Our SMB segment has low switching costs and three cheaper alternatives — we'd lose 20-30% of them. The actual question is: can we segment pricing so enterprise absorbs the increase while SMB gets a different value proposition?"
```

---

## 2. Projection Fallacy

**Pattern**: Assuming the other party shares your cognitive model — your values, your information, your constraints, your reasoning style. "They must think like I do."

**Detection**:
- Phrases like "obviously they would..." or "any rational person would..." — these project your rationality model
- Surprise when others don't respond as expected — a sign the model was yours, not theirs
- Assuming the other party has the same information you do
- Expecting the other party to weight the same factors you weight (engineers projecting technical priorities onto business stakeholders, or vice versa)

**Fix**: List three specific ways the other party's situation differs from yours: different information, different incentives, different constraints, different values, different time horizons. If you can't identify three differences, you haven't actually modeled them — you've modeled yourself and labeled it "them."

```
Before: "The engineering team will be excited about this new architecture — it's clearly superior technically."

After: "The engineering team is evaluating this through three lenses I don't share: (1) migration cost — they'll rewrite 6 months of work, (2) career risk — if the new architecture fails, it's their problem, (3) learning curve — they're experts in the current stack and novices in the new one. 'Technically superior' is my assessment from outside; from inside, 'risky and expensive' is equally valid. I need to address migration cost and career risk before the technical merits matter to them."
```

---

## 3. Manipulation Slope

**Pattern**: Sliding from "understanding others' cognition to find mutual value" to "understanding others' cognition to exploit them." The techniques are the same; the intent diverges.

**Detection**:
- The approach creates value for you by destroying value for the other party
- Information withholding crosses from "strategic timing" to "deception that harms the other party"
- You're engineering a decision the other party would reverse if they had full information
- The phrase "they don't need to know" appears about information that materially affects their interests
- Your model of the other party is used to identify vulnerabilities to exploit rather than concerns to address

**Fix**: Apply the transparency test — if the other party could see your full reasoning and strategy, would they consider it fair? Understanding how someone thinks in order to communicate more effectively or find mutual benefit is legitimate. Understanding how someone thinks in order to extract value they wouldn't willingly give is manipulation.

```
Legitimate: "The client's core concern is implementation risk. I'll reveal our migration support capabilities early because that directly addresses their concern and makes the deal work for both sides."

Manipulation: "The client doesn't know about the upcoming API deprecation that will force a migration anyway. I'll withhold that information so they feel urgency to buy our migration support now at premium pricing."
```

The line: Does your information management serve mutual value discovery, or one-sided value extraction?

---

## 4. Over-Modeling

**Pattern**: Applying complex multi-layer opponent modeling to scenarios that don't require it. Treating a routine interaction as a chess match. Spending more cognitive resources on modeling than the scenario warrants.

**Detection**:
- You're building a cognitive model of someone who is a willing collaborator with aligned incentives
- The interaction is low-stakes but you're analyzing it as if it were high-stakes
- You're three levels deep ("they think that I think that they think...") in a conversation about lunch plans
- The modeling takes longer than the interaction itself would

**Fix**: Calibrate intensity to three factors: (1) stakes — what's at risk if you misread the other party, (2) adversarial nature — are incentives aligned, partially aligned, or opposed, (3) complexity — how many parties with how many competing interests. Routine + aligned + simple = skip the modeling, just communicate directly.

```
Over-modeling: "Before asking my teammate to review this PR, I should consider their current workload, their feelings about code review, whether they'll perceive this as me delegating grunt work, and how this request fits into our team's power dynamics..."

Right-sized: "Hey, can you review this PR? It touches the auth module you're most familiar with."
```

---

## 5. Static Model

**Pattern**: Building a model of the other party early in the interaction and never updating it. Treating people as fixed systems rather than adaptive agents. The model was accurate on day 1 but becomes a liability by day 30.

**Detection**:
- Your description of the other party hasn't changed despite multiple interactions
- You're surprised by their behavior — a sign your model is stale
- You're acting on information from the first meeting while ignoring signals from the fifth
- You categorized them early ("they're risk-averse" / "they're a price buyer") and stopped looking for contradicting evidence

**Fix**: After each significant interaction, update the model. Ask three questions: (1) "What did I learn about how they think that I didn't know before?" (2) "What did they learn about me that might change their approach?" (3) "Has their situation changed since I last modeled them (new information, new pressures, new alternatives)?"

```
Before: "The VP of Engineering is resistant to cloud migration — she's been against it since we first proposed it 6 months ago."

After: "The VP of Engineering was resistant 6 months ago because her team had just recovered from a failed infrastructure project. Since then: she hired a cloud-native architect, her team completed AWS certifications, and the CEO publicly committed to cloud-first. Her constraints have changed. The 6-month-old model is worse than no model because it's confidently wrong."
```

---

## 6. Ignoring Counter-Modeling

**Pattern**: Forgetting that the other party is also modeling YOU. Treating your own behavior as invisible — as if you can observe and model others without them doing the same to you.

**Detection**:
- Your strategy depends on the other party not noticing your strategy
- You assume your intentions are hidden while theirs are readable
- You haven't considered what your past actions signal about your future actions
- Your "surprise" move is only surprising if the other party hasn't been paying attention

**Fix**: Ask three questions: (1) "What does the other party think I'm going to do?" (2) "What has my past behavior told them about my priorities and style?" (3) "Is their current model of me accurate, and do I want it to be?" Sometimes you want them to model you accurately (trust-building). Sometimes you want their model to be wrong (competitive strategy). But you can't manage what you don't acknowledge.

```
Before: "We'll surprise the competitor by launching the enterprise tier they don't expect us to have."

After: "We've hired 5 enterprise sales reps in the last 3 months — all from LinkedIn, all visible. We've published 3 blog posts about 'scaling for enterprise.' Our competitor's product team has definitely noticed. An enterprise launch isn't a surprise — it's a confirmation of what they've already modeled. If we want surprise, we need to look at what they think we WON'T do: the SMB self-serve play they've written us off from."
```
