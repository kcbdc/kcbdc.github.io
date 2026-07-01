# CBDC Safety Lab — Easy User Guide (English)

> This program lets you **test "Will banks become risky if we create a new digital money
> (CBDC)?" on a computer**, before anything happens in real life. Like a flight simulator,
> you experiment safely without touching real banks.

---

## 1. Getting started (very simple)

1. Double-click `cbdc_platform_bilingual.html`. It opens right away in your web browser.
   (No installation needed.)
2. At the **top-right** there are **KOR / ENG** buttons.
   - **KOR** = everything in Korean
   - **ENG** = everything switches to English (press KOR to switch back)
3. Press the blue **"Run once"** button at the top to run one experiment and see results.

---

## 2. Screen layout

- **Left side**: the "dials" (controls). Set your conditions here.
- **Right side**: the results (numbers, charts, tables).

### Main dials on the left

| Dial | What it means | Turning it up |
|---|---|---|
| Shock severity | How strong the crisis is | More risk 🔴 |
| Digital-payment rate | How much people use digital payments | Money leaves faster 🔴 |
| Bank concentration | How much money sits in a few big banks | More risk 🔴 |
| Holding limit | How much CBDC one person may hold | Higher = more outflow risk 🔴 |
| Dynamic Cap / LOLR / Tiered | Safeguards on/off | On = less risk 🟢 |

---

## 3. How to read the result numbers ⭐ Most important

| Number | Meaning | Direction |
|---|---|---|
| **Failure probability P(Fail)** | Chance the bank system fails (0.04 = 4 times in 100) | **Lower is safer** 🟢 |
| **Stability** | How sturdy the banks are | **Higher is safer** 🟢 |
| **Welfare W** | How beneficial it is for people | **Higher is better** 🟢 |
| **Deposit outflow** | Share of money that left | Lower is safer 🟢 |

> 💡 **Key point:** the safest option is a *smartly-guarded* design (Dynamic Cap + Tiered).

---

## 4. "Paper Consistency Check" panel (new feature)

Right below the dashboard is a **Paper Consistency Check** table.

- **Paper value**: the correct numbers the real paper computed with its validated engine.
  - No CBDC 0.04 / Unconstrained 0.41 / Fixed Limit 0.32 / Dynamic Cap + Tiered **0.14**
- **This-tool value**: what this program computes (for reference)
- A green badge **"Design ranking matches ✓"** means this tool reproduced the **same order**
  the paper found (Unconstrained is riskiest, Dynamic Cap + Tiered is safest).

> This tool's fast calculation is for *exploration*; exact magnitudes come from the validated
> Python engine. **What the paper guarantees is the *ranking*:** risk falls in the order
> Unconstrained > Fixed > Dynamic Cap.

---

## 5. What can you do with the results?

1. **Choose a safer CBDC** — Dynamic Cap + Tiered (0.14) is far safer than Unconstrained (0.41).
2. **Find a good holding limit** — change the limit and watch where failure probability drops.
3. **Compare countries** — US/EU are safer; Korea/Sweden need more caution.
4. **Make a report** — use the top-right "Unified PDF" button to save results as a PDF.

---

## 6. FAQ

- **Q. Do I need to install anything?** → No. Just double-click the HTML file.
- **Q. Does switching to English also change chart text?** → Most on-screen text changes. Some
  text drawn *inside* charts is an image and may stay Korean.
- **Q. Will banks really fail by these numbers?** → No. This is not a *prediction* tool; it
  *compares* which design is safer.

---

## 7. One-line glossary

- **CBDC**: digital money issued by a central bank
- **Bank run**: many people withdrawing money from banks at once
- **P(Fail)**: probability the bank system fails (lower is safer)
- **LOLR**: lender of last resort — the central bank's safety net in a crisis
- **θ₂ = 0.2217**: the evidence number showing "concentration × shock" drives crises

The included **result CSV files** (in the `results/` folder) contain the paper's experiment values.
