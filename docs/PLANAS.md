# Laulife — Tyrimo modulio planas

Modulio tikslas: leisti vartotojui **rinkti informaciją, ją atsirinkti, sisteminti ir daryti išvadas**, visą procesą grindžiant moksliniu metodu (klausimas → hipotezė → įrodymai → vertinimas → išvada → peržiūra).

Statusas: v0.1 — planas + raw prototipas (`prototype/tyrimo-modulis.html`). Prototipą tobuliname atskirai, tik po to keliame į patį Laulife appsą.

---

## 1. Pagrindinė idėja

Dabartiniai užrašų / žinių valdymo įrankiai (Notion, Obsidian, Readwise ir kt.) gerai **kaupia**, bet nė vienas neseka **įsitikinimų būsenos**: nėra hipotezių, pasitikėjimo lygio, „šis įrodymas prieštarauja anam teiginiui", nėra išvadų peržiūros ciklo. Tai ir yra Laulife niša (žr. `TYRIMAS.md`, skyrius „Galimybės").

Vartotojo kelias — keturi etapai:

| Etapas | Ką daro vartotojas | Mokslinis atitikmuo |
|---|---|---|
| 1. Rinkimas | Meta viską į vieną dėžutę (nuorodos, pastabos, dokumentai) be vertinimo | Duomenų rinkimas |
| 2. Vertinimas | Kiekvienam šaltiniui priskiria įrodymo lygį (A–D) ir kryptį hipotezių atžvilgiu; atmeta šlamštą | Šaltinių kritika, PRISMA atranka |
| 3. Sisteminimas | Žymos, temos, grupavimas pagal įrodymų kokybę | Duomenų sisteminimas |
| 4. Sintezė | Hipotezės su automatiškai skaičiuojamu pasitikėjimu, „už / prieš" stulpeliai, išvados, peržiūros | Analizė, išvados, revizija |

Principas: **DI siūlo, žmogus sprendžia** — vėlesnėse versijose DI gali siūlyti šaltinio lygį, žymas ir kryptį, bet patvirtina vartotojas.

## 2. Duomenų modelis (branduolys)

Pagal discourse-graph / nanopublication praktiką (šaltiniai — `TYRIMAS.md` §4):

- **Klausimas** (Question) — tyrimo rėmas, turi vieną ar kelias hipotezes.
- **Hipotezė** (Hypothesis) — patikrinamas teiginys; laukai: tekstas, būsena (`formuluojama → tikrinama → patvirtinta / paneigta → peržiūrima`), pasitikėjimas (0–100 %, išvestinis), išvada, peržiūros data.
- **Šaltinis** (Source) — URL / dokumentas / pastaba; laukai: pavadinimas, nuoroda, pastaba, būsena (`inbox → kept / discarded`), įrodymo lygis (A–D pagal GRADE įkvėptą skalę), žymos.
- **Ryšys šaltinis↔hipotezė** — tipizuotas: `palaiko / prieštarauja / neutralu` (ne plikas linkas!).
- Vėliau: **Ištrauka** (Excerpt) — cituojamas fragmentas; **Teiginys** (Claim) — atominis tvirtinimas tarp šaltinio ir hipotezės; **atnaujinimų žurnalas** — kiekvienas pasitikėjimo pokytis su jį sukėlusiu įrodymu.

Pasitikėjimo skaičiavimas v0.1: logistinė funkcija iš svertinės sumos (A=4, B=3, C=2, D=1; `palaiko` +, `prieštarauja` −). Vėliau keistina į rimtesnį Bajeso atnaujinimą su žurnalu.

## 3. Etapai (roadmap)

**v0.1 — raw prototipas (padaryta)**
- Vieno failo HTML prototipas: 4 etapų konvejeris, A–D lygiai, hipotezės, automatinis pasitikėjimas, demo duomenys, localStorage.
- Tikslas: pačiupinėti UX ir patvirtinti proceso logiką prieš integraciją.

**v0.2 — prototipo tobulinimas (artefakte, dar ne appse)**
- Ištraukos / citatos prie šaltinių; kelių klausimų (projektų) palaikymas.
- SIFT-tipo greitas šaltinio patikrinimo checklistas vertinimo etape.
- Prieštaravimų išryškinimas: įspėjimas, kai naujas įrodymas prieštarauja „patvirtintai" hipotezei.
- Eksportas / importas (JSON), kad duomenys nepradingtų.

**v1.0 — integracija į Laulife**
- Backend + sinchronizacija, vartotojo paskyros.
- Dalinimosi funkcija (share sheet / naršyklės plėtinys) į „Rinkimo" dėžutę.
- Periodinė peržiūra („spaced re-evaluation"): priminimas peržiūrėti hipotezes, kurių pasitikėjimas seniai nekito arba gavo naujų prieštaraujančių įrodymų.

**v1.x — DI sluoksnis**
- DI siūlo: šaltinio lygį, žymas, kryptį hipotezės atžvilgiu, teiginių ištraukimą — su paaiškinimu, vartotojas tvirtina.
- ACH matricos vaizdas (hipotezės × įrodymai) kaip išvestinis view.

## 4. Sėkmės kriterijai prototipui

1. Naujas vartotojas per ~2 min supranta keturis etapus be instrukcijų.
2. Pasitikėjimo juosta keičiasi iškart, kai pridedamas / pašalinamas įrodymas — matomas priežastinis ryšys.
3. Silpno šaltinio (D) pridėjimas beveik nekeičia pasitikėjimo — vartotojas *mato*, kodėl verta ieškoti geresnių šaltinių.

## 5. Atviri klausimai (spręsime tobulindami prototipą)

- Ar A–D skalė suprantama ne akademiniam vartotojui, ar reikia žodinių etikečių („labai patikima" ir pan.)?
- Kiek hipotezių vienam klausimui yra praktiška riba UI prasme?
- Ar pasitikėjimo procentas motyvuoja, ar klaidina? Alternatyva — žodinės kategorijos (silpna / vidutinė / stipri).
- Kaip elgtis su šaltiniu, aktualiu keliems klausimams (kai atsiras multi-projektai)?
