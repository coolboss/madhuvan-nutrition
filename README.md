# Madhuvan Nutrition

Single-file, offline-capable nutrition tools from Madhuvan Maternity & Eye Hospital, Vadodara.

| Tool | Path | For |
|---|---|---|
| Nutrition Workstation 3.4 | `index.html` | Clinic desk: patient records, BMI and pregnancy weight gain, ICMR targets, Indian diet builder, trilingual patient sheet |
| Protein Planner 2.0 | `protein/index.html` | Patients: daily protein from Indian home food, with low-cost supplements only to fill the gap |

## Nutrition Workstation 3.4

- Patient list with search; each patient keeps assessment, targets, 7-day plan and visit history. Data stays in the browser (export/import JSON backups from Settings).
- Assessment: BMI with Indian and WHO cut-offs, waist, anaemia grading from Hb (trimester-specific in pregnancy), gestational weight gain against ICMR-NIN 2024 categories (IOM 2009 for comparison) with a weight chart, 5-10% weight-management goal for non-pregnant adults.
- Targets: Mifflin-St Jeor x PAL or the ICMR reference table, ICMR pregnancy/lactation additions, 1 g/kg or ICMR 0.83 g/kg protein rule, GDM carbohydrate split, full ICMR-NIN 2020 EAR/RDA table (editable).
- Diet builder: 542 IFCT 2017 foods (with Gujarati and Hindi names) plus label foods and 167 Gujarati/Indian dishes computed from raw ingredients; household measures; live bars for energy, protein, carbohydrate, fat, fibre, calcium, iron, folate, vitamin C, zinc, with thiamine, riboflavin, niacin, B6, magnesium, vitamin A (RAE), potassium, sodium, saturated fat, cholesterol and phytate under "More nutrients"; 15 templates (Gujarati veg, Jain, eggetarian, non-veg, GDM, protein focus, pregnancy six-small-meals, first-trimester nausea, lactation, anaemia, PMOS low-GI, weight loss, South Indian, North Indian, hypertension) scaled to the energy target; a meal-size guard flags any meal over its share of the day (pregnancy: mains ≤ 30%, snacks ≤ 15%; GDM: carbohydrate per meal) with one-tap fixes — swap for a lighter dish, reduce the cereal portion, or move an item to the next snack; custom foods and dishes.
- Protein Planner hand-off: a tab that opens (and embeds) the standalone Protein Planner pre-filled with the patient's stage, weight, height, diet, conditions, name, doctor's note and the Workstation's protein target; copy the patient link or send it on WhatsApp.
- The screen moulds to the patient category: pregnancy fields, weight-gain chart and trimester labs only in pregnancy; the weight-goal panel only for adults; the Glucose diary tab only when GDM or diabetes is ticked; lab fields on the visit form change with the category.
- Hard exclusions (milk, egg, tree nuts, peanut, soya, gluten, fish, shellfish, sesame) remove foods from search, templates, swaps and the patient sheet.
- Visits record labs by category — Hb, BP, urine protein, fasting / post-meal glucose, HbA1c, ferritin, vitamin D, B12, TSH, lipids — with flags (pre-eclampsia range, GDM targets, deficiencies), trend arrows and a BP chart; flags appear on Assessment and as tips on the patient sheet.
- Glucose diary (GDM / diabetes): home readings by slot, targets, % in range, chart, and hints that point back to the carbohydrate-by-meal table.
- Diet cost in rupees per day and month from an editable Vadodara price list, with cheaper swaps; weekly shopping list with purchase quantities and cost, printable in Gujarati / Hindi.
- Portion guide (generic drawings of katori, glass, cup, rotli, spoons, handful, paneer cube) on Guidance and optionally on the patient sheet.
- Fasting patterns: Farali (Ekadashi / vrat) and Ramzan (sehri + iftar) templates with farali dishes.
- Staff screen language: English, Gujarati or Hindi for tabs, patient form, meals and buttons.
- Two-way patient link: from her link the patient ticks what she ate, enters sugar readings and weight, and sends a short code on WhatsApp to the clinic number; pasting the code into the Workstation adds the readings, a recall and a weight visit.
- 24-hour dietary recall: enter yesterday's intake meal by meal, score it against the same targets, print an audit sheet, or copy it into the plan.
- Patient sheet in English, Gujarati or Hindi: one day or the week, targets, tips tailored to pregnancy/lactation/GDM/supplements; print or save as PDF, copy as WhatsApp text (or open WhatsApp directly when a phone number is recorded), or copy a patient link that opens the sheet on the patient's phone with a language toggle (needs the app hosted online).
- Works offline once opened; installable on phone or desktop.

The 2.1 workstation is kept at `legacy/workstation-2.1.html`.

## Protein Planner 2.0

- Pregnancy (by trimester), breastfeeding (by baby's age) and other adults. Target = 1 g/kg or the ICMR-NIN 2020 figure, whichever is higher; per-kg slider or doctor's fixed grams also available.
- English, Gujarati and Hindi interface.
- Seven-day rotation so the plan changes through the week.
- Tap any item to change its portion, swap it for another, or leave it out.
- "Today's count": tap + for each serving eaten and see what is still needed.
- Doctor's link: set the plan, add the patient's name and a note, then copy a link or send it on WhatsApp. It opens on the patient's phone with everything filled in.
- Supplements tagged by where they are sold: "Shops near me" (Amul parlour, dairy, kirana: high-protein buttermilk and lassi, Kool, sattu) or "Shops + online" (adds Amul whey, high-protein milk and paneer, Milky Mist Skyr, Indian unflavoured whey such as Nakpro / AS-IT-IS / Avvatar, blueberry shake). The doctor can add anything a local shop stocks, with its protein and price.
- Copy for WhatsApp (one day or the whole week), print handout, and a cost-per-gram-of-protein comparison with editable prices.
- Works offline once opened (service worker) and can be added to the phone's home screen.

Veg / non-veg, eggs yes or no, GDM, kidney-disease stop screen and lactose intolerance are all handled. Values are from ICMR-NIN IFCT 2017 and product labels; prices last checked October 2026.

## Hosting
All tools are static pages. Connect the repository to Netlify or turn on GitHub Pages; the workstation is at `/` and the planner at `/protein/`.

## Changelog
- **3.4 (3 Nov 2026)** — category-moulded screens; hard exclusions; labs with flags, trends and BP chart; glucose diary; diet cost and shopping list; portion guide; farali and Ramzan templates; staff UI in Gujarati/Hindi; two-way patient report code.
- **3.3 (3 Nov 2026)** — Meal-size guard with one-tap fixes (swap / reduce / move); nine more templates; templates drop items the patient's diet excludes.
- **3.2 (3 Nov 2026)** — Protein Planner tab: hand-off link/embed pre-filled from the patient record; site address setting so patient links work even when the Workstation is opened from a file.
- **3.1.1 (3 Nov 2026)** — QA pass on both apps. Fixed: IFCT data package lists all oils and ghee at 0 kcal (now 9 kcal/g, so every dish with oil was under-counted by ~45 kcal per teaspoon); chicken leg energy error in the package corrected to its macronutrient value; lactation protein additions corrected to ICMR 2020 RDA (+16.9 g / +13.2 g); protein reference weight for BMI ≥ 30 now uses the weight at BMI 23, the same rule as the Protein Planner. Automated browser QA script covers both apps (edge inputs, all modes, languages, templates, visits, custom foods, backup, links, print CSS, mobile overflow).
- **3.1** — 24-h recall, WhatsApp copy/send, patient link, 167 dishes, B vitamins/SFA/cholesterol/phytate, vitamin A as RAE.
- **3.0** — rebuilt on IFCT 2017 and ICMR–NIN 2020/2024 with patient records and trilingual patient sheet.
