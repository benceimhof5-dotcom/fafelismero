# Erdei fafelismerő – telepítés telefonra

Ez egy webalkalmazás (PWA). Egyszer fel kell tenni egy ingyenes, HTTPS-es tárhelyre, és onnan a telefon böngészőjéből „telepíthető”: ikont kap a kezdőképernyőn, teljes képernyőn fut, és a határozó internet nélkül is működik.

## 1. Feltöltés (egyszer kell, kb. 10 perc) – GitHub Pages

1. Regisztrálj a github.com oldalon (ingyenes).
2. Jobb felül **+ › New repository**. Név például `fafelismero`, legyen **Public**, majd **Create repository**.
3. Kattints az **uploading an existing file** linkre, és húzd be a mappa **tartalmát**: `index.html`, `manifest.webmanifest`, `sw.js` és az `icons` mappa. Végül **Commit changes**.
4. **Settings › Pages**. A *Branch* legyen `main`, a mappa `/ (root)`, majd **Save**.
5. 1–2 perc múlva a címed: `https://<felhasználóneved>.github.io/fafelismero/`

Bármilyen más HTTPS-es statikus tárhely is jó. HTTPS nélkül a GPS és a telepítés nem működik.

## 2. Telepítés a telefonra

**Android (Chrome):** nyisd meg a címet, majd a ⋮ menüben válaszd a **Telepítés** vagy **Hozzáadás a kezdőképernyőhöz** pontot.

**iPhone (Safari, Chrome-ból nem megy):** nyisd meg a címet, majd **Megosztás** gomb › **Főképernyőhöz adás**.

Telepítés után nyisd meg egyszer net mellett, így a határozó elmentődik offline használatra.

## 3. Használat

- **Helyszín:** a helyszínkártyán nyomd meg a **Saját helyzetem (GPS)** gombot, és engedélyezd a helymeghatározást. Térképkoppintással, településsel vagy koordinátával is megadhatod.
- **Határozó:** offline is működik.
- **Fotós felismerés:** internet és saját Claude API-kulcs kell hozzá (platform.claude.com › Settings › API Keys). A kulcs csak a telefonodon tárolódik, a díjat az API-fiókod terheli.

## Frissítés

Ha új változatot töltesz fel, írd át az `sw.js` első sorában a `fafel-v…` értéket egy számmal feljebb, különben a telefon a régit mutathatja.
