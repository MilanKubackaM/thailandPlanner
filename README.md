# Thajsko — Milan & Terka

Plánovač svadobnej cesty do Thajska, **3. – 20. február 2027**.

**Živá stránka:** https://milankubackam.github.io/thailandPlanner/

## Čo to vie

Štyri záložky:

- **Zostáva** — čo ešte treba vybaviť, zoradené podľa termínu (po termíne / najbližších 30 dní / pred odletom / počas cesty). Hotové veci sú zbalené dole.
- **Plán** — itinerár po miestach a dňoch. Pri mieste aj pri dni je tlačidlo **Tipy** (rady schované, kým ich neotvoríš), ubytovanie so stavom a rezervácie, ktoré k danému dňu patria.
- **Peniaze** — rozpočet, odhad, rezerva a položky po skupinách. Prevodník THB → €.
- **Balenie** — zoznamy **Milan**, **Terka** a **Spoločné** podľa kategórií, plus **Nákupy** (všetko, čo treba pred cestou kúpiť).

Krúžok pri položke prepína stav: prázdny = nezariadené / nezbalené, polovičný = rezervované a čaká na platbu / kúpené, plný = hotovo / zbalené.

Ťuknutím na položku sa otvorí detail, kde sa dá upraviť všetko: názov, poznámka, odkaz, termín, deň v pláne, sumy. Položky a tipy sa dajú pridávať aj mazať, upraviť sa dá aj program dňa (ceruzka).

## Ukladanie

Každá zmena sa uloží **hneď** — vždy do prehliadača (localStorage) a, ak je v prehliadači nastavený token, aj do spoločnej verzie pre oboch. Žiadne tlačidlo „Uložiť“.

- Spoločná verzia je súbor `checklist.json` na vetve **`data`** tohto repozitára (mimo `main`, aby uloženie nespúšťalo nové nasadenie stránky).
- Pri otvorení stránky a pri návrate na ňu sa spoločná verzia načíta sama. Čítanie funguje bez tokenu.
- Ak obaja meníte naraz, zmeny sa zlúčia po jednotlivých poliach; pri skutočnom konflikte vyhrá ten, kto ukladá.
- Keď sa uloženie nepodarí (neplatný token, bez spojenia), dole sa ukáže červené upozornenie a zmena ostane v prehliadači.

### Prístupový token

V stránke **nie je žiadny token** — statická stránka bez neho do repozitára zapisovať nemôže. Každý ho zadá raz na svojom zariadení:

- dole v pätičke **Zapnúť ukladanie pre oboch**, alebo
- jednorazovým odkazom `https://milankubackam.github.io/thailandPlanner/#t=TOKEN` (token sa uloží a z adresy zmizne).

Token treba vytvoriť ako **fine-grained personal access token** obmedzený na tento repozitár, s oprávnením **Contents: Read and write**.

## Štruktúra

```
index.html                    — celá aplikácia v jednom súbore (obsah je v konštantách ITEMS, PACK, PLACES, TIPS, DAYS)
vetva data: checklist.json    — spoločný stav (len zmeny oproti východziemu obsahu)
```
