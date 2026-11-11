# Lón food diary

An interactive, mobile-first prototype of a food diary for the Irish market that looks and feels like a paper notebook. It includes products from Dunnes Stores, Tesco Ireland and SuperValu.

## What it does

- Opens with a splash screen (the notebook's leather cover swings open), then sign in or create an account. New accounts go through onboarding before they can use the diary. "Explore the sample diary" opens a filled-in demo.
- Accounts are local to the browser in this prototype: there's no server, each account's diary is stored separately, and passwords are kept as salted SHA-256 hashes, never as plain text.
- Onboarding sets daily targets from one of three profiles: Athletic Performance / Sports, General Fitness Maintenance or Weight Management.
- Each day is a journal page. Swipe or use the arrows to turn pages, with a page-turn sound.
- Energy (kcal or kJ), protein, carbohydrate and fat totals are "stamped" at the top of each page.
- Food is logged by text search, barcode, photo or voice. Barcode, photo and voice are simulated in this prototype.
- Each product page shows prices per shop, pack size, servings, the full nutrition panel, ingredients, allergens and a 3D view where ingredients float out of the pack.
- Totals are calculated per item, per meal and per day, with conversions between g, ml and servings. Missing nutrition values are shown as "Not provided" and never counted as zero.
- Saved meals, bi-weekly weigh-ins, error recovery when offline, and two-tap delete with undo.

## Run it

Open `index.html` in a browser through a local web server so the `img/` photos load:

```bash
python3 -m http.server 8000
```

Then go to http://localhost:8000.

## Data and photo credits

- Nutrition values and prices are illustrative sample data based on typical Irish pack labels. Check them against real packs before any production use.
- Product photos are from [Open Food Facts](https://world.openfoodfacts.org) contributors, licensed CC BY-SA 3.0. Each product page links to its source.
- The banana, tomato and full Irish breakfast photos are from Wikimedia Commons, credited in the app: Wilfredor (CC0), Maksym Kozlenko (CC BY-SA 4.0) and IrishFireside (CC BY 2.0).
- 3D rendering uses [three.js](https://threejs.org) r128.
