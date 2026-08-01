<div align="center">

<img src="assets/emoji.png" alt="Fruit Picker" width="100">

# Fruit Picker Skill

### *Let AI pick your fruit, properly*

<img src="https://img.shields.io/badge/fruits-5_and_growing-4C9A6B?style=flat-square" alt="5 fruits and growing"> <img src="https://img.shields.io/badge/grounded_in-horticulture_research_%2B_standards-C99A3F?style=flat-square" alt="grounded in research"> <img src="https://img.shields.io/badge/license-MIT-5B7FBF?style=flat-square" alt="MIT license">

🍈 Monthong durian　👑 Musang King / D24 / Black Thorn　🥭 Mango　🥑 Avocado　🍉 Watermelon

**English** ・ [简体中文](README.zh-CN.md)

<img src="assets/storyboard.png" alt="Fruit Picker: from spotting a fruit at the stall to opening it at home" width="820">

</div>

---

## 🚀 Quick start

**The easiest way — just hand the repo to your agent:**

```text
Install this skill for me: https://github.com/Ezra-Y/fruit-picker
```

Your agent will fetch it and put it where it belongs. Nothing else to do.

<details open>
<summary><b>Prefer to do it yourself? Three other ways</b></summary>

**Install as a plugin** (auto-updates, works in every project):

```text
/plugin marketplace add Ezra-Y/fruit-picker
/plugin install fruit-picker@fruit-picker
```

**Copy the folder** into your personal skills directory:

```bash
gh repo clone Ezra-Y/fruit-picker /tmp/fruit-picker
cp -R /tmp/fruit-picker/fruit-picker ~/.claude/skills/fruit-picker
```

**Ship it with a project** so your whole team gets it — same copy, into `.claude/skills/fruit-picker/` inside the repo, then commit.

</details>

Then just send it a photo:

```text
Help me check this durian — I want to eat it tonight.
```

## 🤔 The problem it solves

Durian is expensive — can this one be opened tonight? Two watermelons look identical, so which one? That mango looks gorgeous, but when is it actually at its best?

**The hard ones are never the obviously-good or obviously-bad fruit. They are the ones that look promising and leave you unsure.**

Fruit Picker reads the stem, the base, the seam lines, the ground spot, the shoulders, any splits or damage — then combines that with when you plan to eat it and how it feels in your hand, turning "not sure" into one of four clear answers:

> 🟢 **Buy it** ・ 🟡 **Buy under conditions** ・ 🔵 **Needs confirmation** ・ 🔴 **Pick another one**

## 🍈 A full walkthrough

Say you have a Monthong durian you want to open tonight.

### 1️⃣ Send everything in one go

Number the fruit and send four angles:

| Shot | What it should show |
|---|---|
| **Whole fruit** | Full outline and several chambers |
| **Spine tips & seams** | Mid-body, over the bulging chambers |
| **Stem close-up** | Stem and the joint |
| **Base close-up** | Base, any openings, anything unusual |

Then just ask:

```text
Use the fruit-picker Skill — is this Monthong worth buying?

I plan to eat it tonight. Photos taken under white store lighting.
Two adjacent spines in the middle squeeze together slightly,
and there's a faint sweet smell near the stem.
```

💡 **A few things worth knowing**

**1. Tell it when you plan to eat.** "Tonight" and "in two days" call for genuinely different fruit.

**2. Lighting decides whether colour can be used.** How yellow the ground spot is, how far an avocado has darkened, whether spine tips lean green or brown — colour reads are sensitive to light, so it will ask what light you shot under.

- ☀️ **Best**: outdoor diffuse daylight. If the shop lighting is messy, carry the fruit to the doorway or a window and take one there.
- 💡 **Indoor white / cool LED**: usable; colour is treated as weaker evidence.
- 🏮 **Warm yellow, supermarket yellow, mixed light**: put a **sheet of white paper or a receipt turned blank-side up** next to the fruit, in the same frame, and it can calibrate the colour cast. Best references, in order: grey card > clean white paper or card > back of a receipt > white tissue. Phone screens, metal, glass and glossy packaging don't help.
- 📵 Harsh shadows, glare, blown highlights and beauty filters distort colour — a quick reshoot beats squinting at a bad photo.

No white reference to hand? That's fine — it skips colour and works from shape, texture, seam lines and openings instead, just more cautiously.

**3. Feel it yourself.** A squeeze or a sniff carries more weight than a photo, so try it and tell it what you found. What the vendor claims doesn't count as evidence.

**4. All at once beats drip-feeding.** Photos, timing and hand-feel in a single message gets you a complete verdict without back-and-forth.

### 2️⃣ It reads each photo for what only that photo can show

The whole-fruit shot for chamber fullness and overall balance; the mid-body close-up for seam lines, grooves and spine shape; the stem for maturity; the base to confirm openings and the state of critical areas. Squeeze, smell and timing are then weighed together against "eating tonight."

**Risk signals are always handled first.**

### 3️⃣ You get a clear verdict

```text
This one's a keeper — open it tonight.

Recommendation: buy, good for tonight
Ripeness window: matched. Seam lines and grooves lean ripe, adjacent spines give slightly
Risk: critical areas clean, base closed
Flesh appearance: good. Several continuous chambers, well-filled outline
Confidence: medium
```

Reasoning, risk and how sure it is, all together. Open the fruit and you'll know how well it called it ✅

## 🧺 What it covers today

| Fruit | What it does for you |
|---|---|
| 🍈 **Monthong durian** | Ripeness window, opening check, flesh appearance, buy verdict |
| 👑 **Musang King / D24 / Black Thorn** | Variety identity cues, inspection once opened |
| 🥭 **Mango** | Matching firmness to how you'll eat it, ripening potential |
| 🥑 **Avocado** | Eat today or wait, slicing versus mashing |
| 🍉 **Watermelon** | Ranking candidates from the same variety and batch |

More fruits and durian varieties are being researched and added 🚧

## 🤔 Why you can trust it

**Each fruit gets its own checklist**:
Monthong leans on stem, seam lines, openings and the spine squeeze; watermelon compares ground spot and shape; mango looks at shoulders, firmness and intended use; avocado trusts your palm most. Every signal comes from horticultural research, official grading standards and postharvest literature, reworked for what an ordinary phone camera can actually see.

**Evidence is weighted**:
Decisive evidence outranks supporting detail. Blurry photos, wrong angles or colour-distorting light automatically reduce a signal's weight, and missing information stays neutral. When one more photo would change the answer, it tells you exactly which one to take.

**Safety comes first, always**:
Mould, rot, weeping, unusual softness and dangerous splits are handled ahead of everything else. Keeping you out of trouble outranks finding you a bargain.

**It says only as much as it can back up**:
Every verdict carries a high / medium / low confidence level, plus what limits it — photo quality, coverage, or the signals themselves.


## 📄 License

MIT — see [LICENSE](LICENSE). Also see the [Privacy Notice](PRIVACY.md) and
[Terms](TERMS.md).
