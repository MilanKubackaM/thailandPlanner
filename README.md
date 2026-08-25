# 🌴 Thajsko Honeymoon — Milan & Terka

Interaktívny plán svadobnej cesty do Thajska, **3.–20. február 2027**.

👉 **Živá stránka:** https://milankubackam.github.io/thailandPlanner/

## Čo to vie

- **Denný itinerár** s presunmi, letmi a nocľahmi
- **Checklist po dňoch** — trojstavové odklikávanie (nič / vybraté / hotové), editovateľné texty, vlastné položky a odkazy
- **Rozpočet** rozpísaný po kategóriách
- **Ubytovania a aktivity** s cenami a linkami
- **ⓘ značky** — ukazujú, čo bolo na danom mieste pred poslednou zmenou plánu

## Ukladanie

Stav checklistu sa ukladá **automaticky do prehliadača** každého z nás zvlášť (localStorage), takže si každý môže klikať po svojom.

Navyše je hore v checkliste **spoločný zoznam**:

- **⬇︎ Načítať spoločné** — stiahne poslednú spoločnú verziu z tohto repozitára (`data/checklist.json`). Funguje bez tokenu.
- **⬆︎ Uložiť do spoločného** — zapíše tvoj stav sem do repozitára, aby ho videl aj ten druhý. Vyžaduje prístupový token.

### Prístupový token

V stránke **nie je žiadny token uložený**. Kto chce ukladať do spoločného zoznamu, vloží si vlastný token cez tlačidlo 🔑 **Token** — uloží sa len do jeho prehliadača.

Token treba vytvoriť ako **fine-grained personal access token** obmedzený na tento repozitár, s oprávnením **Contents: Read and write**.

## Štruktúra

```
index.html            — celá aplikácia (jeden súbor, bez závislostí)
data/checklist.json   — spoločný stav checklistu
```
