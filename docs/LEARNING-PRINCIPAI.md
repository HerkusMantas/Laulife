# Laulife „Learning" modelio informacijos rinkimo principai

Ištraukta 2026-07-15 iš `lifeos-app/apps/web/public/epist-learning.html` (skiltys „Informacijos rinkimo taisyklės", „Darbo taisyklės" ir `ENTRIES` duomenų struktūra). Šie principai — pagrindas, ant kurio derinsime tyrimo modulio Rinkimo–Vertinimo etapus.

## 1. Kanoninės taisyklės (galioja visoms temoms)

1. **Tik akademinis / mokslinis konsensusas** — be retorikos, be asmeninių pozicijų.
2. **Šaltinių hierarchija** (mažėjančio patikimumo tvarka):
   1. recenzuojami žurnalai
   2. universitetų monografijos / vadovėliai
   3. pripažintos enciklopedijos (pvz., SEP, IEP)
   4. klasikiniai pirminiai tekstai
   - Vengti: tinklaraščių ir neaiškios kilmės šaltinių.
3. **Konsensuso lygis kiekvienam teiginiui ir kiekvienam ribotumui**:
   | Ženklas | Reikšmė |
   |---|---|
   | ●●●● | visuotinis |
   | ●●●○ | vyraujantis |
   | ●●○○ | ginčijamas |
   | ●○○○ | marginalus |
4. **Privalomi įrašo elementai**: teiginys · šaltinis · patikimumas · kontroversijos (su data) · ribotumai · gyvenimiškas pavyzdys.
5. **Rekomenduojami elementai**: klausimas · istorinė raida · vidiniai ryšiai · autoriai · tarpdisciplininiai ryšiai · dažniausias nesusipratimas · sunkumas (1–3) · mąstymo eksperimentas · atviri klausimai · citata.
6. **Terminai**: LT + EN originalas; ginčytini terminai kaupiami centriniame žodyne.
7. **Faktas atskiriamas nuo interpretacijos.**
8. **Datos / versijos žymimos** — kontroversijų būsena visada su data (pvz., „konsensuso vaizdas pagal SEP 2026").

## 2. Darbo (proceso) taisyklės

1. **Tyrimas pirma** — faktai nerašomi iš atminties be patikrinimo.
2. **Šaltiniai niekada neprasimanomi** — neradus, aiškiai pažymima.
3. Kiekvienas teiginys gauna **konsensuso lygį ir gyvenimišką pavyzdį**.
4. Ribotumai — **tik akademiškai pripažinti**; visa kita žymima „marginali kritika".
5. Pridėjus įrašą atnaujinamas indeksas ir žodynas (nuoseklumo palaikymas).
6. Vartotojo nustatytos taisyklės vykdomos visada, be išimčių.

## 3. Įrašo duomenų struktūra (`ENTRIES`)

| Laukas | Reikšmė | Statusas |
|---|---|---|
| `q` | atveriantis klausimas | rekomenduojamas |
| `claim` | teiginys (atominis, patikrinamas) | privalomas |
| `c` | konsensuso lygis 1–4 | privalomas |
| `ex` | gyvenimiškas pavyzdys | privalomas |
| `src` | šaltiniai (pirminis + apžvalginis) | privalomas |
| `rel` | šaltinio patikimumo vertinimas žodžiu | privalomas |
| `contro` | pozicijos / kontroversijos su data | privalomas |
| `lims` | ribotumai, kiekvienas su savo `c` lygiu ir šaltiniu | privalomas |
| `hist` | istorinė raida | rekomenduojamas |
| `auth` | autoriai — **ir gynėjai, ir kritikai** | rekomenduojamas |
| `exp` | mąstymo eksperimentas | rekomenduojamas |
| `mis` | dažniausias nesusipratimas | rekomenduojamas |
| `inter` | tarpdisciplininiai ryšiai | rekomenduojamas |
| `links` | vidiniai ryšiai (į kitas temas) | rekomenduojamas |
| `open` | atviri klausimai | rekomenduojamas |
| `cite` | citata | rekomenduojamas |
| `d` | sunkumas 1–3 | rekomenduojamas |

## 4. Ką tai reiškia tyrimo moduliui (suderinimas)

| Learning principas | Tyrimo modulio atitikmuo | Būsena prototipe |
|---|---|---|
| Šaltinių hierarchija (žurnalai → … → pirminiai tekstai) | A–D įrodymų lygiai | ✅ yra, verta suvienodinti aprašus |
| Konsensuso lygis ●●●●–●○○○ | Pasitikėjimo % prie hipotezės | ⚠️ pakeisti/papildyti 4 lygių skale — suprantamesnė nei % |
| Kontroversijos su data | Hipotezės būsena + išvados data | ⚠️ pridėti „pagal <data>" prie išvadų |
| Ribotumai su savo konsensuso lygiu | Prieštaraujantys įrodymai | ✅ yra („prieš" stulpelis) |
| Privalomas gyvenimiškas pavyzdys | — | ❌ pridėti prie teiginių/išvadų |
| Faktas ≠ interpretacija | Šaltinio pastaba vs. vertinimas | ⚠️ atskirti laukus vertinimo etape |
| Autoriai: gynėjai ir kritikai | — | ❌ galima pridėti prie šaltinių („kas teigia / kas ginčija") |
| Tyrimas pirma, šaltinių neprasimanyti | Proceso taisyklė DI sluoksniui (v1.x) | 📋 įtraukta į planą |
