# Jak upravovat tenhle web a nezešílet

Tenhle soubor se na web nikdy nedostane, a bude jenom v tomhle repozitáři, který
je něco jako "portál pro správu webu".  Každopádně, tenhle repozitář musí být
taky veřejný (pro nahlížení), takže bych sem nedával nic tajného.

Základní změny se dělají v konfiguračním souboru `_config.yml`:
- Jméno webu v patičce a jménech záložek
- odkazy v hlavičce a patičce webu
- odkaz na logo v hlavičce
- sekce "Příspěvky"

**Hlavní stránky webu** potom jsou:
- `index.md` Domovská stránka
- `about.md` O nás
- `404.md` Pro pokus o načtení neexistující stránky

Potom se dají vcelku intuitivně přidávat **nové příspěvky** z adresáře `_posts`.
Jméno souboru musí obsahovat datum zveřejnění, obecně jakékoliv datum v
minulosti.  Tyto příspěvky pak jsou seřazené podle data v záložce "Příspěvky".

## Hlavička dokumentu

Každá ze stránek má svou **hlavičku**, která upravuje její podobu mimo samotný
obsah. Hlavička začíná a končí řádkou se sekvencí `---`. Vypadá nějak takhle:

```
---
title: Jméno stránky
feature_image: "/imgs/background_homepage.jpg"
feature_text: |
  ## Černý nadpis
  <h2 style="color: rgb(255, 255, 255)">Nadpis, kterému jde změnit barva</h2>
# indexable: false
---

Tady začíná obsah
```

Title se nezobrazí přímo na stránce, ale ve jméně záložky, a při sdílení na
sociální sítě. Je vhodné mít stejný text ještě jednou jako Feature text, nebo
jako první nadpis na stránce.

Feature image a Feature text je část s velkým obrázkem přes celou stránku, který
může (ale nemusí!) překrývat text. Text má ve výchozím stavu šedou barvu, která
s hromadou obrázků splyne. Pro nadpis jiné barvy použij druhý ze zmiňovaných
způsobů, kde jde zvolit barva pomocí RGB kódu.  RGB kód si můžeš najít třeba na
[HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp).

Fun fact: Tato hlavička fakticky není formátu Markdown, ale YAML (stejně jako
`_config.yml`). Proto jdou řádky zneplatnit zakomentováním, kdy se na začátek
přidá symbol `#`. V Markdownu by tohle udělalo nadpis. Textová hodnota parametru
v YAML formátu se píše buď na jeden řádek do "uvozovek", nebo na více řádek -
potom je potřeba na první řádku dát symbol `|`.

## Obrázky

Pokud chcete na web přidat nějaký **obrázek**, je nejlepší ho umístit do složky
`imgs/`. Ve jméně by ideálně neměly být mezery, česká diakritika atd.  Obrázek
pak lze využít v jakékoliv ze stránek webu pomocí odkazu. Odkazy ale snadno
můžou vést i na jiné stránky.

---

Užitečné odkazy:

[Github Pages](https://docs.github.com/en/pages) je služba, která stránky do
určité velikosti bezplatně nasazuje a zpřístupňuje na internet.

[Jekyll](https://jekyllrb.com/) je systém pro generování webu z lidsky čitelných
a snadno upravovatelných souborů.  Primárně překládá úvodní hlavičku stránek +
Markdown na výsledný HTML soubor.

Šablona webu:
- [Alembic](https://alembic.darn.es/)
- [Alembic | Github](https://github.com/daviddarnes/alembic)
