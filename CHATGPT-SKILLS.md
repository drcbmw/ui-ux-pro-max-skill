# ChatGPT skillovi za Daraceve projekte

Ovaj repozitorij od sada sadrzi automatizirani **GitHub Actions build** koji priprema 10 nezavisnih skill ZIP arhiva.

## Bez instaliranja deset repozitorija

1. Otvori **[Build ChatGPT skill packs](https://github.com/drcbmw/ui-ux-pro-max-skill/actions/workflows/chatgpt-skill-pack.yml)**.
2. Odaberi **Run workflow** i pokreni na grani main ili preuzmi zadnji uspjesan run.
3. U sekciji **Artifacts** preuzmi `darac-chatgpt-skills-ready`.
4. Izvuci `chatgpt-skills-pack.zip` i procitaj `INSTALACIJA-PRVO-PROCITAJ.md`.
5. Svaki `<skill-name>/skill.zip` ucitaj **zasebno** u ChatGPT Skills (`/skills`). Ako zelis prvo samo UI UX, ucitaj samostalni `skill.zip` iz artifacta.

Arhiva za svih deset vjestina je distribucijski paket, nije samostalni instalabilni skill. Izvorne licence ostaju pridruzene svakom paketu.

## Sadrzaj

| Skill | Namjena |
| --- | --- |
| darac-skill-router | Najavljuje i bira odgovarajucu dostupnu vjestinu prije veceg zadatka |
| ui-ux-pro-max | Katalog boja, stilova, UX pravila i pretraga putem Pythona |
| module-regression | Cross-module regresija kod Manager projekta |
| browser-qa | Browser i responsive QA |
| security-review | Sigurnost API-ja, autentifikacije, unosa |
| api-connector-builder | Integracije API-ja (SOLO, Gmail, Gemini/Groq) |
| agent-security-hardening | Sigurnost asistenta koji moze izvrsiti radnje |
| design-system | Vizualna dosljednost i tokeni |
| cost-aware-llm-pipeline | Budzet API tokena i izbor modela |
| logo-design | SVG logotipovi i produkcijski exporti |

Izvori su [ui-ux-pro-max-skill](https://github.com/drcbmw/ui-ux-pro-max-skill), [ECC](https://github.com/drcbmw/ECC) i [logo-design-skill](https://github.com/drcbmw/logo-design-skill).

GitHub Action gradi svaki put iz trenutasnih javnih grana izvornih forkova, zato `manifest.json` biljezi SHA svakog izvora i izlaznog ZIP-a. Prije aktiviranja integracija koje rade s privatnim podacima pregledaj upute i dozvole.

**Ogranicenja:** Samo dodavanje na GitHub ne instalira vjestine u ChatGPT; rad sa stvarnim preglednikom, lokalnom bazom ili API-jem zahtijeva alate i dozvole, ne samo skill.
