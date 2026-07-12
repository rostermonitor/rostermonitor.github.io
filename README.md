# rostermonitor.github.io

Legal pages for the RosterMonitor iOS app (Privacy Policy + Terms of Service, EN + CS).

- `/` — landing with links
- `/privacy/` — Privacy Policy (linked from the app's paywall as `https://rostermonitor.github.io/privacy`)
- `/terms/` — Terms of Service (linked as `https://rostermonitor.github.io/terms`)

## Jak publikovat (jednorázově, ~10 minut)

1. **Založ GitHub účet s uživatelským jménem `rostermonitor`** na https://github.com/signup.
   Doména `rostermonitor.github.io` vzniká přímo z uživatelského jména, takže jméno musí být přesně `rostermonitor`.
   *Nejdřív ověř dostupnost: otevři https://github.com/rostermonitor — pokud stránka neexistuje (404), jméno je volné.
   Uživatelská a organizační jména sdílí jeden prostor; místo druhého osobního účtu můžeš pod svým běžným účtem
   založit **organizaci** pojmenovanou `rostermonitor` (funguje stejně) — ale jen pokud je jméno volné.
   Kdyby bylo obsazené, doména `rostermonitor.github.io` není k dispozici a musí se v aplikaci změnit obě URL — dej mi vědět.*

2. **Vytvoř nový veřejný repozitář pojmenovaný přesně `rostermonitor.github.io`**
   (https://github.com/new, Owner = rostermonitor, Public, bez README).

3. **Nahraj obsah této složky** — buď přes web (repo → "uploading an existing file" → přetáhni
   `index.html`, složky `privacy/` a `terms/`, i tenhle README), nebo z terminálu:

   ```bash
   cd ~/Desktop/rostermonitor.github.io
   git init -b main
   git add .
   git commit -m "Legal pages: privacy + terms (EN/CS)"
   git remote add origin https://github.com/rostermonitor/rostermonitor.github.io.git
   git push -u origin main
   ```

4. **GitHub Pages se pro repo `<user>.github.io` aktivuje automaticky** z větve `main`.
   Kdyby ne: repo → Settings → Pages → Source: „Deploy from a branch", Branch: `main` / root.

5. **Ověř (po ~2 minutách):**
   - https://rostermonitor.github.io/privacy/ → 200, zobrazí Privacy Policy
   - https://rostermonitor.github.io/terms/ → 200, zobrazí Terms of Service
   - Verze bez lomítka (přesně ty, na které odkazuje aplikace) vrací 301 přesměrování
     na verzi s lomítkem — v prohlížeči i v aplikaci fungují obě.
     Z terminálu: `curl -IL https://rostermonitor.github.io/privacy` → očekávej 301 → 200.

## Kam URL patří v App Store Connect

- **App Privacy → Privacy Policy URL**: `https://rostermonitor.github.io/privacy`
- **Předplatné (In-App Purchase) → EULA / Terms**: `https://rostermonitor.github.io/terms`
- Volitelně **Marketing URL**: `https://rostermonitor.github.io`

## Údržba

Při změně textu uprav příslušné `index.html`, aktualizuj datum účinnosti v obou jazycích
a pushni — Pages se přegeneruje samo.
