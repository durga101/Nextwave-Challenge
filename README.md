# FirstAI in 60: Workshop Referral Engine

**NxtWave Growth Intern Challenge, Round 1**

A growth plan and a working referral tool to get **500 final-year engineering students** to register for the free workshop **"Build Your First AI Project in 60 Minutes"**, with a **₹2,000 budget** and **7 days**.

**Live demo:** [Open the website](https://claude.ai/artifact/8QtT2HNha9CrzG9AHDNuV2)

![Registration page](assets/screenshot-register.png)

---

## 1. The student

**Who:** final-year B.Tech students in Tier-2/3 colleges in Andhra Pradesh and Telangana, in two segments:

- CSE/IT students with no real project on their resume
- ECE/EEE/Mech students who want an IT job but think AI is "only for CS"

**Why they care:** October to February is placement season. Every interviewer asks "What have you built?", and most of these students have no answer.

**What makes them register:**

- **A concrete outcome:** a live AI project link for their resume, in 60 minutes
- **Low effort:** free, online, no coding needed
- **A trusted invite:** the message comes from a classmate, not an ad

## 2. The campaign plan

Three channels, ranked by impact, with zero ad spend:

| Priority | Channel | What happens | Planned registrations |
| --- | --- | --- | --- |
| 1 | Campus ambassadors | 25 ambassadors, one per college, post 3 times in their class WhatsApp groups | ~300 |
| 2 | Referral loop | Every registrant gets a personal code; 3 friends joining unlocks a bonus prompt pack | ~130 |
| 3 | Clubs and placement cells | Coding clubs and placement officers at 10 colleges forward a ready-made post and email | ~120 |
| | **Total** | 500 target + 10% buffer | **~550** |

**Budget (₹2,000):**

| Item | Amount |
| --- | --- |
| Top-3 ambassador vouchers (₹500, ₹400, ₹300) | ₹1,200 |
| Referral lucky draw (6 × ₹100) | ₹600 |
| Buffer | ₹200 |
| Paid ads | ₹0 |

**How the numbers add up:**

- **WhatsApp:** 25 ambassadors × 3 groups × ~80 students = 6,000 reached → 18% click → ~1,080 visits → 28% register ≈ **300**
- **Referral:** ~30% of the first ~420 registrants each bring about one friend ≈ **130**
- **Clubs and emails:** 10 colleges, ~3,000 students → ~4% register ≈ **120**

**7-day timeline:**

| Day | Action |
| --- | --- |
| 1 | Build the site and tracker; sign up 25 ambassadors |
| 2 | Onboard ambassadors; first WhatsApp post; club and placement-cell emails |
| 3 | Push the 3-friend unlock to everyone registered |
| 4 | Social-proof post; check the dashboard and cut the weakest channel |
| 5 | Double down on the top colleges; club announcements in class |
| 6 | Last-call post; leaderboard race |
| 7 | Final reminders; announce prizes |

## 3. What I built

**Not just a landing page: a working referral engine.** My plan depends on ambassadors and referrals, and those only work if I can see who brought whom.

| Feature | What it does |
| --- | --- |
| Registration with referral codes | A six-field form; every student gets a personal code and a one-tap WhatsApp invite |
| Live 500-seat map | Every dot is a student, coloured by the channel they came from |
| Leaderboards | Top colleges, top ambassadors and top student referrers, updated live |
| Ambassador kit | Ambassador codes plus ready-to-send Day 2, 4 and 6 WhatsApp posts |
| Campaign dashboard | Registrations by channel against plan, per day and by branch, with next-step suggestions |

![Campaign dashboard](assets/screenshot-dashboard.png)

### Run it locally

1. Download or clone this repository.
2. Open `index.html` in any browser.

You don't need to install anything or run a build step.

### Host it on GitHub Pages

1. In the repository, go to **Settings → Pages**.
2. Under **Source**, choose **Deploy from a branch**.
3. Pick **main** and **/ (root)**, then click **Save**.

Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/` after about a minute.

> **Demo mode:** outside the Claude-hosted version, registrations are saved in the visitor's own browser (localStorage). The site starts with simulated sample registrations so the leaderboards and dashboard aren't empty. The Claude-hosted version saves registrations to a shared live database.

### Privacy

The tracker stores only first name and initial, college, branch, source and referral codes, plus a one-way hash of the email to block duplicate sign-ups. Email addresses and phone numbers are not stored in the shared tracker. In a real campaign, contact details would go to a private CRM.

## 4. How I thought

**What changed between my first idea and the final solution?**
I started with a landing page and Instagram ads aimed at all engineering students. I ended with one specific student, three peer-driven channels, and a tracker that measures all of them. I also realised that registrations aren't attendance, so the plan ends with reminders, not with the 500th sign-up.

**What would I improve with another 24 hours?**

- Automated WhatsApp reminders 24 hours and 1 hour before the workshop, to lift show-up from about 35% to about 50%
- A Telugu version of the posts for Tier-3 colleges
- OTP verification on phone numbers, so the leaderboard can't be gamed

**What did AI suggest that I rejected, and why?**

| AI suggestion | Why I rejected it |
| --- | --- |
| Spend ₹1,500 on Meta and Instagram ads | That would buy roughly 50–100 cold sign-ups; the same money motivates 25 ambassadors who each reach hundreds of classmates |
| Bulk WhatsApp blasts to bought or scraped numbers | It's spam, breaks WhatsApp's rules, and hurts the brand |
| One big random prize, like a phone | It attracts fake sign-ups, which lowers the show-up rate |
| A long form (CGPA, resume upload) | Every extra field loses students on mobile |

## Repository contents

| Path | What it is |
| --- | --- |
| `index.html` | The website (single file: HTML, CSS and JavaScript) |
| `docs/NxtWave_Growth_Plan.pptx` | 5-slide growth plan |
| `docs/AI-Learning-Notes-and-Video-Script.md` | AI + learning notes and the demo video script |
| `assets/` | Screenshots used in this README |

## Tech stack

- Vanilla HTML, CSS and JavaScript, with no frameworks or build step
- Google Fonts: Bricolage Grotesque and Atkinson Hyperlegible
- Browser localStorage in demo mode; a shared database in the Claude-hosted version
