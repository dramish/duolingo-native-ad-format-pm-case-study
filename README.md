# Duolingo's Post-Lesson Promo: From Forced Wait to an In-Lesson Exercise

**Ishita Bansal | Product case study | October 2026**

---

## At a glance

| | |
|---|---|
| **Problem** | A ~15s Super promo after every short lesson, skippable only once it ends, sometimes in the wrong language, with no energy reward |
| **Why now** | Duolingo says added friction slowed user growth, and it is building a native ad format |
| **Idea** | A skippable, in-language exercise that teaches a Super benefit through a task |
| **Key question** | Does it beat the simple fix (an early skip) without hurting Super conversion? |
| **Proof** | A staged A/B test with a break-even rule |

---

## 1. Context

- **Friction costs growth.** Q4 2025 letter: raised bookings mainly through friction (more ads, upsells), which helped slow daily-user growth. More than $50M of bookings foregone to prioritize growth.
- **Native ad format** is on Duolingo's roadmap. No public detail on its design.
- **Q2 2026:** daily users up 23% to 58.7M, 12.7M paid subscribers, retention at an all-time high.
- **Only ~10% pay**, so free users are the funnel.

**So:** retention isn't broken. The question is whether one source of avoidable friction can go without losing conversion.

## 2. Problem

The promo is short, so the friction is **how it feels**, not how long it is:
- Skip only after it finishes
- Loud, right after focused learning
- Can appear in a language the user isn't learning
- No energy in return

**Scope:** in-house promo only. Third-party ads don't run after every short lesson, and the energy cap is a separate complaint.

## 3. User research

- **Survey:** Google Forms, free mobile users, shared via language-learning communities and personal networks.
- **Interviews:** 8 to 10 follow-ups, including reactions to an exercise mock-up.
- **Asks:** how often they see the promo, whether they notice it more than other ads, how they feel right after, whether they quit sessions because of it, promo vs energy cap, and which fix they prefer.

## 4. Solution

- **Format:** a short task in the user's target language, such as "I use SuperDuo" or "SuperDuo is great", with later sentences showing what Super does.
- **Screen:** light-green background with a clear "Sponsored" label.
- **Controls:** "Try for free" button and an immediate skip.
- **Energy:** test 0 vs +1, far below the 5 from a rewarded ad, with a daily cap.
- **Placement:** the existing post-lesson slot.

## 5. Why not just add an early skip?

- **Early skip (B1)** = the same 15s video, skippable after 3s.
- It removes the wait but also most of the pitch. A user who skips at 3s has seen almost nothing about Super.
- **The exercise** makes the user read and process a benefit to answer, so the message lands without the forced wait.
- **This is a hypothesis.** A recall check in the test measures it.

## 6. Experiment

| Arm | Format | Skip | Energy | Tests |
|---|---|---|---|---|
| **A** (control) | 15s video | After it ends | 0 | Status quo |
| **B1** | 15s video | After 3s | 0 | Earlier skip alone |
| **B2** | Exercise | Immediate | 0 | Format, vs B1 |
| **C** | Exercise | Immediate | +1 | Reward, vs B2 |
| **D** (holdout) | No promo | n/a | 0 | Value of the promo |

**Stages:** A vs B1 vs D, then B1 vs B2, then B2 vs C.

**Metrics**
- **Primary:** same-session next-lesson starts; D7 retention
- **Secondary:** skip rate, Super trial starts per exposure, benefit recall
- **Guardrails:** rewarded-ad impressions, energy-driven conversion, learning outcomes, skip always available

**Break-even:** ship only if (Δ D7 retention × value per retained user) − (Δ Super conversion × value per conversion) ≥ 0.

**Decision rule**
- Ship the exercise only if B2 beats B1 and clears break-even.
- If B1 captures most of the gain, ship the early skip and stop.
- If D beats every arm, the promo itself is the problem.

## 7. Risks

| Risk | How it's tested |
|---|---|
| Early skip is enough | B2 vs B1 head to head |
| Softer pitch converts worse | Trial starts per exposure |
| Exercise tires users | Skip rate, next-lesson starts |
| Reward cannibalizes rewarded ads | 0 vs +1 arms, daily cap, impression guardrail |
| Novelty wears off | Compare week 1 with later weeks. Phrases rotate by level at low cost |

## 8. Deferred

Mid-lesson placement, bigger energy rewards, third-party ads, the energy cap.

## Sources

- Duolingo Q4 FY2025 letter (SEC): https://www.sec.gov/Archives/edgar/data/1562088/000162828026012513/q4fy25duolingo12-31x25shar.htm
- Duolingo Q2 FY2026 letter (SEC): https://www.sec.gov/Archives/edgar/data/0001562088/000162828026053299/q2fy26duolingo6-30x26share.htm
- Customer Experience Dive, Q4 2025: https://www.customerexperiencedive.com/news/duolingo-limit-friction-growth-slows/813414/
- Customer Experience Dive, Q2 2026: https://www.customerexperiencedive.com/news/duolingos-user-retention-hits-all-time-high-as-app-boosts-stickiness/827499/
- Q2 2026 earnings call summary: https://www.webull.com/news/15392596720296960
- Review spike tracker, June 2026: https://unstar.app/events/duolingo-language-chess-complaints-june-2026
- Reddit snapshot, Jan 2026: https://reddit.sentinel-team.org/posts/1qoobx9/snapshots/2026-01-27T21%3A10%3A35.33027Z
- Trustpilot: https://fi.trustpilot.com/review/duolingo.com
- Blog review of Duolingo's ads: https://www.desarrollolibre.net/blog/programacion-basica/super-duolingo-the-free-language-learning-app-review
