# Metric-compatible fonts (font pack, v1)

- Families: carlito, caladea, arimo, tinos, cousine. Each has the same character widths as a common Office font, so documents keep their line breaks and page layout: Carlito for Calibri, Caladea for Cambria, Arimo for Arial, Tinos for Times New Roman, Cousine for Courier New.
- Files: Regular, Bold, Italic and Bold Italic of each family, all static TTF (a PDF embeds a subset of a static face; a variable face would embed only its default weight). Carlito, Caladea, Tinos and Cousine are copied unchanged from github.com/google/fonts (ofl/<family>) at commit e7db6ca603fd4862010383ff17ffd6cc4ffac1c0. google/fonts has only variable Arimo, so Arimo comes from github.com/googlefonts/arimo (fonts/ttf) at commit 4a6255f269916ae7ad3fc2706b0935e7621396b8, unchanged.
- Licence: SIL Open Font License 1.1. Each family folder has its OFL.txt. google/fonts has no OFL.txt in ofl/tinos at that commit, so tinos/OFL.txt is the standard OFL 1.1 text with the copyright line from ofl/tinos/METADATA.pb.
- Checksums: manifest.json.
