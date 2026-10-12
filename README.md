# Spotplanner packs

Destination packs for [Spotplanner](https://github.com/dordzhiegorov-cyber/spotplanner): one JSON file per destination with its most photographed and most talked-about spots, built by `services/planner/scripts/build_city.py` from open data only. The app downloads a pack the first time a destination is opened and keeps it on the device.

- `packs/index.json` lists every pack with its area, spot count and build date.
- `packs/<id>.json` holds the area and its spots: coordinates, category, interest tags, visit length, opening hours, a short description with its source, one free photo with its credit, official links, and the open popularity signals with their sources.

Fetch them directly, e.g. `https://raw.githubusercontent.com/dordzhiegorov-cyber/spotplanner-packs/main/packs/porto.json`, or through a CDN: `https://cdn.jsdelivr.net/gh/dordzhiegorov-cyber/spotplanner-packs@main/packs/porto.json`.

## Sources and licences

- **Wikidata** — items, coordinates, classes, heritage designations, sitelinks. CC0.
- **Wikipedia** — monthly pageviews (a fame signal) and two-sentence summaries. Text: CC BY-SA 4.0, credited per spot (`summarySource`, `wikipediaTitle`).
- **Wikivoyage** — see/do listings: opening hours, prices, descriptions. CC BY-SA 4.0, credited per spot (`summarySource`, `wikivoyageTitle`).
- **OpenStreetMap** — opening hours, fees, websites, named viewpoints. © OpenStreetMap contributors, ODbL. The extracted facts are kept separate from Spotplanner's scores.
- **Wikimedia Commons** — photo counts as signals; one free photo per spot (CC0, CC BY, CC BY-SA, public domain) with author, licence and file page in `photo`.

No Google data is stored (Google content is shown only through Google's own Places UI Kit) and no Instagram data is collected or shared.

The packs (the selection and the derived defaults) are published under **CC BY-SA 4.0**, so that the share-alike text they contain stays share-alike. Credit "Spotplanner (spotplanner.app)" and the sources above when reusing them.
