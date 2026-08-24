# Electricianul — jocul instalației electrice

Joc educativ pentru Android (fără internet, fără cont): 6 niveluri în care legi fire la prize, la bec
și întrerupător, la comutatoare cap‑scară, alegi siguranțele din tablou și dai un test final.
Fiecare greșeală îți spune de ce e greșită. Stelele și scorul se salvează pe telefon.

## Cum obții APK‑ul prin GitHub (la fel ca la Tetris și la aplicația de sănătate)

1. Pe github.com: **+** (dreapta sus) → **New repository** → nume `electricianul` → Public → **Create repository**.
2. **Add file → Upload files** → tragi/alegi TOATE fișierele și folderele din această arhivă
   (`settings.gradle`, `build.gradle`, `gradle.properties`, `.gitignore`, `README.md`, folderul `app`)
   → jos, **Commit changes**.
3. Folderul `.github` e ascuns pe multe telefoane, așa că îl faci de mână:
   **Add file → Create new file** → la nume scrii exact `.github/workflows/build.yml`
   (GitHub creează folderele singur când scrii „/”) → lipești conținutul fișierului
   `.github/workflows/build.yml` din arhivă → **Commit changes**.
4. Tab‑ul **Actions** → „Build APK” pornește singur (dacă nu, **Run workflow**). Prima dată durează 5–10 minute.
5. Când apare bifa verde: intri în rulare → jos, la **Artifacts** → descarci **Electricianul-APK**
   → dezarhivezi → instalezi `app-debug.apk` (telefonul cere „Instalare din surse necunoscute” → permiți).

## Ce e în arhivă

- `app/src/main/assets/index.html` — tot jocul (HTML + JavaScript), fără biblioteci externe
- `app/src/main/java/com/electrician/joc/MainActivity.java` — ecranul Android care afișează jocul pe tot ecranul
- `.github/workflows/build.yml` — rețeta după care GitHub compilează APK‑ul
- restul: fișierele Gradle, manifestul, iconița și tema

## Personalizare

- întrebările testului: lista `QUIZ` din `index.html`
- rândurile din tablou: lista `rows` din funcția `startTablou`
- numele aplicației: `app/src/main/res/values/strings.xml`
