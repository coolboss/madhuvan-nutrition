# Madhuvan Nutrition

Single-file, offline-capable nutrition tools from Madhuvan Maternity & Eye Hospital, Vadodara.

| Tool | Path | For |
|---|---|---|
| Nutrition Workstation 2.0 | `index.html` | Clinic desk: energy and diet planning, 7-day review, print |
| Protein Planner 2.0 | `protein/index.html` | Patients: daily protein from Indian home food, with low-cost supplements only to fill the gap |

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
Both tools are static pages. Connect the repository to Netlify or turn on GitHub Pages; the planner then lives at `/protein/`.
