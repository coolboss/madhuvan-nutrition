# Nutrition Workstation & Protein Planner for Indian clinics

Free, open-source (MIT) nutrition tools for Indian clinical practice. Built on **ICMR–NIN IFCT 2017** food composition, **ICMR–NIN 2020** reference intakes and the **2024 Dietary Guidelines for Indians**, with patient output in **English, Gujarati and Hindi**.

No server, no login, no subscription. Each tool is a single HTML file that runs in the browser, works offline once opened, installs on a phone or desktop like an app, and keeps patient data only in that browser.

| Tool | Path | For |
|---|---|---|
| **Nutrition Workstation 3.6** | `index.html` | The clinic desk: assessment, targets, diet plan, recall, labs, glucose diary, patient sheets |
| **Protein Planner 2.1** | `protein/index.html` | The patient's phone: daily protein from home food, with low-cost supplements only to fill the gap |
| **Aahar 1.1** | `me/index.html` | Anyone's phone: BMI, daily targets, ICMR "My Plate", tap what you ate, the basic rules — self-care, no doctor needed |
| **Lifestyle Rx 1.2** | `lifestyle/index.html` | Weight-loss planner with a Learn section: calories and protein, cardio ranked by joint load, strength, yoga, rehab; rules for GLP-1 drugs, diabetes, hypertension, injuries, pregnancy and older age |

Live copies: https://coolboss.github.io/madhuvan-nutrition/ · https://coolboss.github.io/madhuvan-nutrition/protein/ · https://coolboss.github.io/madhuvan-nutrition/me/ · https://coolboss.github.io/madhuvan-nutrition/lifestyle/

Built by Dr Rajesh Parikh, obstetrician, Vadodara, with Claude, for his own practice; shared in the hope it is useful to other small clinics and nursing homes.

---

## Nutrition Workstation

**Patient categories:** pregnancy, lactation, adult (general / weight management), preconception / PMOS. The screen moulds to the category: pregnancy fields, ICMR weight-gain chart and trimester labs appear only in pregnancy; the weight-goal panel only for adults; the Glucose diary tab only when GDM or diabetes is ticked.

**Assessment.** BMI with Indian and WHO cut-offs, waist, anaemia grading from Hb (trimester-specific in pregnancy), gestational weight gain against ICMR–NIN 2024 categories (IOM 2009 for comparison) with a weight chart, 5–10 % weight-management goal with a capped deficit for non-pregnant adults, condition flags (GDM, diabetes, hypertension, PMOS, hypothyroid, lactose, renal), hard exclusions for allergies (milk, egg, nuts, peanut, soya, gluten, fish, shellfish, sesame).

**Targets.** Mifflin–St Jeor × PAL or the ICMR reference table; ICMR pregnancy and lactation additions; protein by 1 g/kg or ICMR 0.83 g/kg with the ICMR additions, BMI-adjusted weight above BMI 30; GDM carbohydrate split; full ICMR–NIN 2020 EAR/RDA table for calcium, iron, zinc, magnesium, folate, vitamins A, C, B1, B2, B3, B6, sodium, potassium — all editable in Settings.

**Diet plan.** 542 IFCT 2017 foods (with Gujarati and Hindi names) plus label foods and 173 Indian dishes computed from raw ingredients; household measures; 21 nutrients with live bars; 17 templates (Gujarati veg, Jain, eggetarian, non-veg, GDM, protein, pregnancy six small meals, first-trimester nausea, lactation, anaemia, PMOS low-GI, weight loss, South Indian, North Indian, hypertension, Farali/Ekadashi, Ramzan) scaled to the energy target; a meal-size guard that flags any meal over its share of the day with one-tap fixes (swap, reduce, move); diet cost in rupees with cheaper swaps; weekly shopping list; custom foods and dishes.

**24-hour recall.** Enter yesterday's intake, score it against targets, print an audit, or turn a good day into the plan.

**Visits and labs.** Weight, weeks, Hb, BP, urine protein, glucose, HbA1c, ferritin, vitamin D, B12, TSH, lipids — shown only where they apply — with flags, trend arrows, BP chart and weight/gain chart.

**Glucose diary** (GDM/diabetes). Home readings by slot, targets, % in range, chart, and hints tied to the carbohydrate-by-meal table.

**Patient sheet.** One day or the week, targets, tailored tips, exclusions, portion guide drawings, shopping list — in English, Gujarati or Hindi. Print or save as PDF, copy as WhatsApp text, open WhatsApp directly with the patient's number, or copy a patient link.

**Patient link.** Opens the sheet on the patient's phone with a language toggle. From it she ticks what she ate, enters sugar readings and weight, and sends a short code to the clinic's WhatsApp; pasting the code into the Workstation adds the readings, a recall and a weight visit. No server involved.

**Protein Planner hand-off.** A tab that opens (and embeds) the Protein Planner pre-filled with the patient's stage, weight, diet, conditions, name, doctor's note and the Workstation's protein target.

**Staff screen language.** English, Gujarati or Hindi.

## Aahar — my food, my day

For an individual, not a clinic. Fully in English, Gujarati or Hindi (auto-detected from the phone). Four screens:
- **Me** — age, sex, height, weight (pre-pregnancy weight in pregnancy), stage (adult / planning a baby / pregnant / breastfeeding), activity, diet (veg, Jain, eggs, non-veg), conditions. BMI in plain words with Indian cut-offs; energy and protein targets (Mifflin–St Jeor, ICMR additions); ICMR–NIN 2024 "My Plate for the day" scaled to those calories, in household measures.
- **Today** — tap the dishes you ate; the plate fills up by food group against ICMR shares; one-line verdict ("Add: vegetables, dal"; "Go easy on: sugar"); water glasses; a 0–100 plate score.
- **Learn** — 15 cards: half the plate vegetables, a pulse with every cereal, milk 300 ml, oil by the spoon, sugar under 25 g, vitamin C with iron, salt, small regular meals, water, packaged foods, reading a label, pregnancy, movement; plus the portion drawings.
- **Progress** — 7-day plate scores, weight log with chart, share a summary.

Same IFCT 2017 food data and 173 dishes as the Workstation. Not medical advice; says so on every screen.

## Protein Planner

Pregnancy (by trimester), breastfeeding (by baby's age) and other adults. Target = 1 g/kg or the ICMR-NIN 2020 figure, whichever is higher; per-kg slider or a doctor's fixed figure. Seven-day rotation, tap-to-swap, daily tally, supplements tagged by where they are sold (local shop vs online) with cost per gram of protein, doctor's link, WhatsApp copy, print. English, Gujarati, Hindi. Handles veg / non-veg, eggs, GDM, kidney disease and lactose intolerance.

---

## Setting up for your clinic

1. Open the Workstation. The first-run screen asks for clinic name, doctor, WhatsApp number and languages. That's all.
2. Optional: edit `clinic-config.js` (same folder as `index.html`, and again in `protein/`) to pre-fill those values and the site address, so every device in the clinic starts configured. Leave it blank for a neutral copy.
3. Settings → check the ICMR reference values and the food price list against your own sources; both are editable.
4. Take a backup (Settings → Download backup) at the end of each clinic day. Data lives in the browser; clearing the browser erases it.

### Hosting
Both tools are static pages. Fork this repository and turn on GitHub Pages (Settings → Pages → branch `main`, folder `/`), or drop the folder on Netlify. The Workstation is then at `/` and the Planner at `/protein/`. The site address goes in Settings so patient links work.

### Limits, stated plainly
- One browser, one device: no sync, no multi-user, no cloud. Backup/restore JSON moves data between devices.
- WhatsApp sending opens the message for you to press send; there is no silent automated sending (that needs the WhatsApp Business API and a server).
- No appointments, billing or reminders.
- Dish nutrition is computed from raw ingredients and is an estimate, not a laboratory analysis.

## Sources
- Longvah T et al. *Indian Food Composition Tables 2017*, ICMR–NIN, Hyderabad (data via the `@ifct2017` npm packages).
- ICMR–NIN. *Nutrient Requirements for Indians, RDA and EAR, 2020* (2024 revised summary).
- ICMR–NIN. *Dietary Guidelines for Indians, 2024*.
- Institute of Medicine 2009 gestational weight gain ranges (comparison only).
- Mifflin MD et al. 1990 resting energy equation.
- Label foods: manufacturer packs (marked "Label", verify); USDA FoodData Central; NIN Nutritive Value of Indian Foods.

## Disclaimer
These tools are clinical decision aids for qualified clinicians. Values are estimates, reference intakes are defaults you are expected to verify, and every target or flag is a starting point for clinical judgement. The treating doctor remains responsible for every prescription. See `LICENSE`.

## Changelog
- **3.6 / Aahar 1.1 (5 Nov 2026)** — Severe-scrutiny release after an independent clinical review (37 findings, all addressed). Template fitter rewritten: 1–3 rotli per main meal (2 in GDM), rice ½–1½ katori, energy gap filled with milk, dal, dahi, fruit, nuts, paneer, egg before cereals; fallbacks when an exclusion empties a meal; protein-short warning. Whole pregnancy now uses pregnancy micronutrient targets (first trimester was getting non-pregnant folate). New patients no longer get a weight-loss deficit by default. Jain patients keep condition templates. GDM macro split sums to 100%. Protein on continuous adjusted weight above BMI 25, 1.2 g/kg during restriction; energy on adjusted weight for obese pregnant/lactating women; +300 kcal for underweight adults. Ferritin, TSH (trimester-specific), HDL, BP-before-20-weeks and non-GDM pregnancy glucose flags corrected; glucose slots named "2 h after"; low readings flagged. Anaemia template no longer pairs dairy or tea with iron meals; sugared nimbu pani replaced. MoHFW supplement schedule wording. Lactation gets alcohol, caffeine and fish cards. Mohanthal, sukhdi, basundi portions corrected; unfortified bread values. Aahar: never advises weight loss in pregnancy or lactation, requires pre-pregnancy weight for BMI, no deficit under 18 or over 60, fixed vegetable/fruit/milk minimums, sugar capped at 25 g (0 in diabetes), health chips now change targets and tips, potatoes no longer count as vegetables, fried food and sweets penalised in the plate score, cereal line reads as a per-meal example.
- **Aahar 1.0 (4 Nov 2026)** — new self-service app at `/me/`.
- **3.5 (4 Nov 2026)** — Public release: neutral branding with first-run clinic setup and optional `clinic-config.js`; MIT licence; Protein Planner takes the clinic name from the link or config instead of hard-coding it.
- **3.4 (3 Nov 2026)** — Category-moulded screens; hard exclusions; labs with flags, trends and BP chart; glucose diary; diet cost and shopping list; portion guide; farali and Ramzan templates; staff UI in Gujarati/Hindi; two-way patient report code.
- **3.3** — Meal-size guard with one-tap fixes; nine more templates.
- **3.2** — Protein Planner hand-off tab.
- **3.1.1** — QA pass: oil/ghee energy (IFCT package lists oils at 0 kcal), chicken-leg energy, lactation protein RDA, BMI-30 protein weight.
- **3.1** — 24-h recall, WhatsApp copy/send, patient link, 167 dishes, B vitamins/SFA/cholesterol/phytate, vitamin A as RAE.
- **3.0** — Rebuilt on IFCT 2017 and ICMR–NIN 2020/2024 with patient records and trilingual patient sheet. The earlier 2.1 workstation is kept at `legacy/workstation-2.1.html`.
