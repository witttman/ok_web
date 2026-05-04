# ZADÁNÍ PRO AI: WordPress web Studentský klub Orlík

---

## ROLE

Jsi expert WordPress vývojář a designér. Vytvoříš kompletní WordPress custom theme (bez rodičovského tématu) pro **WordPress 6.9.4** s plně editovatelnými prvky pomocí Gutenberg block editoru (Full Site Editing). Web musí být responzivní a vícejazyčný (CZ + EN) pomocí pluginu **Polylang**.

---

## PŘEHLED PROJEKTU

- **Název webu:** Studentský klub Orlík
- **Tagline / slogan:** „BUĎ OK!"
- **Cílová skupina:** Studenti ČVUT Praha
- **Adresa:** Thákurova 4/6/8, 160 00 Praha 6
- **WordPress verze:** 6.9.4
- **Téma:** Čistý custom block theme (FSE – Full Site Editing)
- **Jazyky:** Čeština (výchozí) + Angličtina (plugin Polylang)
- **Fotografie:** Placeholder obrázky (není reálný obsah)
- **Texty:** Placeholder Lorem Ipsum (není reálný obsah)
- **Barevné varianty:** Světlý režim (výchozí) + Tmavý režim (dark mode)

---

## BAREVNÁ PALETA

| Název            | Hex / hodnota              | Použití                                      |
|------------------|----------------------------|----------------------------------------------|
| Primární žlutá   | `#F4C400`                  | Tlačítka, akcenty, hero pozadí, nadpisy       |
| Světlá žlutá     | `rgba(244, 196, 0, 0.68)`  | Pozadí alternativních sekcí, hover stavy      |
| Tmavá            | `#2B2D33`                  | Pozadí tmavých sekcí, text na světlém pozadí  |
| Bílá             | `#FFFFFF`                  | Pozadí, text na tmavém pozadí                 |
| Text (výchozí)   | `#2B2D33`                  | Veškerý tělo text                             |

---

## BAREVNÁ PALETA – TMAVÝ REŽIM (DARK MODE)

Tmavá varianta invertuje světlá pozadí na tmavá, přičemž žlutá zůstává jako primární akcentní barva.

| Prvek                     | Světlý režim                      | Tmavý režim                        |
|---------------------------|-----------------------------------|------------------------------------|
| Pozadí stránky            | `#FFFFFF`                         | `#2B2D33`                          |
| Alternativní pozadí sekce | `rgba(244, 196, 0, 0.68)`         | `rgba(244, 196, 0, 0.15)`          |
| Primární akcent           | `#F4C400`                         | `#F4C400`                          |
| Nadpisy                   | `#2B2D33`                         | `#FFFFFF`                          |
| Tělo textu                | `#2B2D33`                         | `#E0E0E0`                          |
| Karty / panely            | `#FFFFFF` s `box-shadow`          | `#3A3D45` s `box-shadow`           |
| Tlačítka (primární)       | `#F4C400`, text `#2B2D33`         | `#F4C400`, text `#2B2D33`          |
| Odkazy                    | `#2B2D33`, hover `#F4C400`        | `#F4C400`, hover `#FFFFFF`         |
| Header                    | `#2B2D33`                         | `#1A1C20`                          |
| Footer                    | `#2B2D33`                         | `#1A1C20`                          |
| Hero sekce pozadí         | `#F4C400`                         | `#2B2D33` s žlutými akcenty        |
| Galerie placeholder pozadí| `#CCCCCC`                         | `#4A4D55`                          |

### Implementace dark mode
- Přepínač (toggle) v pravém rohu navigace vedle přepínače jazyka CZ/EN
- Ikony: ☀️ (světlý) / 🌙 (tmavý) nebo SVG ikony
- Uložení preference do `localStorage` (vanilla JS)
- Implementace přes CSS custom properties (CSS variables) a třídu `dark-mode` na elementu `<html>`
- Plynulý přechod: `transition: background-color 0.3s ease, color 0.3s ease`
- Tmavý režim je viditelně aktivní i z obrázku prototypu – obrázky sekcí jsou bez výrazných bílých pozadí, vše na tmavém podkladu

---

## TYPOGRAFIE

- Nadpisy (H1–H3): tučný řez, velká písmena pro H1, barva `#2B2D33` nebo `#FFFFFF` dle pozadí
- Tělo textu: regulérní řez, 16px, barva `#2B2D33`
- Font: systémový stack nebo Google Font dle uvážení (doporučeno: **Inter** nebo **Roboto**)

---

## NAVIGACE (MENU)

Horní navigační lišta s položkami:
1. O nás
2. Členství
3. Služby
4. Kontakty
5. Galerie
6. Odkazy
7. Přepínač jazyka **CZ / EN** (vpravo)

Chování:
- Sticky header (zůstává při scrollování nahoře)
- Pozadí headeru: `#2B2D33`, text: `#FFFFFF`, aktivní položka: `#F4C400`
- Na mobilech: hamburger menu
- Přepínač dark/light mode (☀️/🌙) v navigaci vpravo vedle přepínače jazyka

---

## STRUKTURA STRÁNKY – SEKCE (shora dolů)

### 1. HERO SEKCE
- Pozadí: plná šířka, barva `#F4C400`
- Logo klubu (placeholder SVG/PNG) centrované
- Velký nadpis: **„BUĎ OK!"** – tučné, velká písmena, barva `#2B2D33`
- Podnadpis: „Studentský klub Orlík"

---

### 2. CO NABÍZÍME
- Pozadí: `#FFFFFF`
- Nadpis sekce: „Co nabízíme"
- 4 karty (columns block), každá karta obsahuje:
  - Ikona (použij dashicon nebo SVG placeholder)
  - Název služby
  - Krátký Lorem Ipsum popis (2–3 věty)
- Karty (zleva doprava):
  1. **Internet** – ikona globusu
  2. **Pošilovna** – ikona balíku / poštovní schránky
  3. **Tiskárna** – ikona tiskárny
  4. **Zábava** – ikona herního ovladače / hvězdy
- Na **desktopu**: 4 karty vedle sebe v řadě
- Na **mobilech**: horizontální carousel (1 karta plnou šířkou, šipky ← →, sousední karty viditelné z ~15 %)

---

### 3. JAK SE K NÁM PŘIDAT
- Pozadí: `rgba(244, 196, 0, 0.68)`
- Nadpis: „Jak se k nám přidat"
- Text: Lorem Ipsum odstavec popisující proces přihlášení
- Zmínka o registraci přes IS (Informační systém školy) – text s odkazem na `#` (placeholder URL)
- Kontaktní email jako odkaz: `registrace@ok.cvut.cz` (placeholder)

---

### 4. KDO JSME?
- Pozadí: `#F4C400`
- Nadpis: „Kdo jsme?"
- Text: Lorem Ipsum 2–3 odstavce o historii a poslání klubu
- Zmínka: klub funguje od roku 1999, spolupráce se Studentskou unií ČVUT

---

### 5. KONTAKTY
- Pozadí: `#FFFFFF`
- Nadpis: „Kontakty"
- 3 kontaktní karty (columns block), každá obsahuje:
  - Kulatý placeholder avatar (placeholder image 150×150 px)
  - Pozice / titul
  - Jméno: **Jan Novák** (placeholder)
  - Email jako odkaz: `jmeno@ok.cvut.cz` (placeholder)
- Karty:
  1. **Předseda** – email: `predseda@ok.cvut.cz`
  2. **Zástupce klubu** – email: `zastupce@ok.cvut.cz`
  3. **Předseda** (druhý výbor / sekretář) – email: `predseda2@ok.cvut.cz`

---

### 6. PŘIDEJ SE K NÁM
- Pozadí: `#2B2D33`
- Text: `#FFFFFF`
- Nadpis: „Přidej se k nám"
- Lorem Ipsum text vyzývající ke členství
- Tlačítko CTA: „Zjistit více" – barva `#F4C400`, text `#2B2D33`, odkazuje na sekci „Jak se přidat" (`#jak-se-pridat`)

---

### 7. GALERIE
- Pozadí: `#FFFFFF`
- Nadpis: „Galerie"
- Horizontální image slider / carousel se šipkami doleva a doprava
- 5 placeholder obrázků (16:9, rozměr 800×450 px)
- Použij Gutenberg Gallery block nebo jednoduché řešení s CSS scroll-snap

---

### 8. INFORMACE PRO ČLENY
- Pozadí: `rgba(244, 196, 0, 0.68)`
- Nadpis: „Informace pro členy"
- Dvousloupcový layout (columns block) s odkazy:
  - Levý sloupec:
    - Usnesení členské schůze (odkaz `#`)
    - Stanovy a základní základ (odkaz `#`)
    - Vnitřní řád členů (odkaz `#`)
  - Pravý sloupec:
    - Řád o Internetu (odkaz `#`)
    - Revize elektrospolupráce (odkaz `#`)
    - FAQ (odkaz `#`)

---

### 9. INTERNET (detail služby)
- Pozadí: `#FFFFFF`
- Nadpis: „Internet" + ikona globusu
- Text: Lorem Ipsum 2–3 odstavce popisující internetové připojení
- Pod textem: image carousel / slider se 3 placeholder obrázky

---

### 10. POŠILOVNA (detail služby)
- Pozadí: `rgba(244, 196, 0, 0.68)`
- Nadpis: „Pošilovna" + ikona obálky
- Text: Lorem Ipsum 2–3 odstavce
- Pod textem: image carousel / slider se 3 placeholder obrázky

---

### 11. TISKÁRNA (detail služby)
- Pozadí: `#FFFFFF`
- Nadpis: „Tiskárna" + ikona tiskárny
- Text: Lorem Ipsum 2–3 odstavce
- Bez galerie

---

### 12. ZÁBAVA (detail služby)
- Pozadí: `rgba(244, 196, 0, 0.68)`
- Nadpis: „Zábava" + ikona herního ovladače
- Text: Lorem Ipsum 2–3 odstavce
- Pod textem: image carousel / slider se 3 placeholder obrázky

---

### 13. ODKAZY
- Pozadí: `#2B2D33`
- Text / ikony: `#FFFFFF`, hover: `#F4C400`
- Nadpis: „Odkazy"
- Grid 2 sloupce s ikonami a textem:
  | Ikona         | Text                                 | URL (placeholder) |
  |---------------|--------------------------------------|-------------------|
  | GitBucket     | GitBucket                            | `#`               |
  | Instagram     | Orlík klub                           | `#`               |
  | Discord       | discord.ok.cvut.cz                   | `#`               |
  | Kniha/IS      | Informační systém školy              | `#`               |
  | GitLab        | GitLab wiki                          | `#`               |
  | Srdce         | Studentland Linie ČVUT               | `#`               |
  | Dům/budova    | Správa sdílených zařízení ČVUT       | `#`               |

---

### 14. ADRESA
- Pozadí: `#FFFFFF`
- Nadpis: „Adresa"
- Dvousloupcový layout:
  - Vlevo: placeholder mapa (statický obrázek nebo iframe Google Maps na adresu Thákurova 4/6/8, Praha 6)
  - Vpravo: text adresy: **Thákurova 4/6/8, 160 00 Praha 6**

---

### 15. FOOTER
- Pozadí: `#2B2D33`
- Text: `#FFFFFF`
- Obsah:
  - Logo klubu (placeholder, malé)
  - Text: „© 2025, Web Orlík"
  - Slogan: **„JSEM OK!"** – tučně, barva `#F4C400`

---

## TECHNICKÉ POŽADAVKY

### Theme struktura (custom block theme / FSE)
Vygeneruj kompletní WordPress custom theme s těmito soubory:

```
/wp-content/themes/orlik/
  style.css               – hlavičkový soubor theme
  theme.json              – globální styly (barvy, typografie, spacing)
  functions.php           – registrace scriptu, stylů, Polylang support
  index.php               – fallback
  templates/
    index.html            – výchozí šablona stránky
    front-page.html       – šablona úvodní stránky (celý layout)
    404.html              – 404 stránka
  parts/
    header.html           – header s navigací a přepínačem jazyka
    footer.html           – footer
  assets/
    css/
      style.css           – doplňkové styly (carousel, hover efekty atd.)
      dark-mode.css       – CSS variables pro tmavý/světlý režim
    js/
      carousel.js         – jednoduchý vanilla JS carousel pro galerie
      dark-mode.js        – přepínač dark/light mode s uložením do localStorage
    images/
      logo-placeholder.svg – placeholder logo
```

### Plugin požadavky
- **Polylang** (vícejazyčnost CZ/EN) – instrukce pro aktivaci a nastavení
- Žádné další povinné pluginy

### Dark mode – technická specifikace CSS
V souboru `dark-mode.css` definuj CSS custom properties:
```css
:root {
  --color-bg:          #FFFFFF;
  --color-bg-alt:      rgba(244, 196, 0, 0.68);
  --color-bg-dark:     #2B2D33;
  --color-text:        #2B2D33;
  --color-text-inv:    #FFFFFF;
  --color-text-muted:  #555555;
  --color-accent:      #F4C400;
  --color-card-bg:     #FFFFFF;
  --color-card-shadow: rgba(0,0,0,0.1);
}
html.dark-mode {
  --color-bg:          #2B2D33;
  --color-bg-alt:      rgba(244, 196, 0, 0.15);
  --color-bg-dark:     #1A1C20;
  --color-text:        #E0E0E0;
  --color-text-inv:    #FFFFFF;
  --color-text-muted:  #AAAAAA;
  --color-accent:      #F4C400;
  --color-card-bg:     #3A3D45;
  --color-card-shadow: rgba(0,0,0,0.4);
}
```
Všechny barvy v `style.css` musí používat tyto custom properties místo pevných hodnot.

### Responzivita
- Mobile first přístup
- Breakpointy: 480px (mobile), 768px (tablet), 1200px (desktop)
- Hamburger menu na mobilech

---

## MOBILNÍ VERZE – DETAILNÍ SPECIFIKACE

Mobilní zobrazení vychází z připojených screenshot prototypů (světlá i tmavá varianta).

### Navigace (mobile – ≤ 768px)
- Logo Orlík vlevo (malé, cca 40px výška)
- Hamburger ikona (≡) uprostřed nebo vpravo
- Přepínač jazyka **EN** vpravo
- Přepínač dark/light mode (🌙/☀️) zcela vpravo
- Po kliknutí na hamburger se rozbalí fullwidth dropdown menu se všemi položkami
- Pozadí headeru: `#2B2D33` (světlý i tmavý režim)

### Hero sekce (mobile)
- Logo klubu (orel) centrované, cca 120px výška
- Nadpis „Studentský klub Orlík" – velký, tučný, zalomení na 2 řádky
- Tagline **„BUĎ OK!"** pod nadpisem, kurzíva nebo tučné
- Pozadí: `#F4C400` (světlý) / `#2B2D33` se zlatými akcenty (tmavý)

### Sekce „Co nabízíme" (mobile)
- 1 karta na řádek (scrollovatelný horizontální carousel se šipkami ← →)
- Aktivní karta je vycentrovaná, sousední karty jsou vidět z cca 15 %
- Karta: ikona nahoře, název, krátký text
- Šipky ← → jsou viditelné po stranách

### Sekce „Jak se k nám přidat" (mobile)
- Plná šířka, text ve sloupci
- Zvýraznění odkazů (Discord, email) jako podtržené aktivní linky
- Žádný dvousloupcový layout – vše pod sebou

### Sekce „KDO JSME?" (mobile)
- Nadpis velkým písmem, výrazný
- Pozadí: `#F4C400` (světlý) / tmavá varianta s průhlednou žlutou
- Text ve sloupci, plná šířka

### Sekce „Kontakty" (mobile)
- Horizontální carousel se šipkami ← → (jedna karta najednou)
- Karta: kulatý avatar (placeholder), pozice, jméno, email
- Šipky jsou aktivní interaktivní prvky
- V prototypu viditelná pouze karta „Předseda" – ostatní dostupné scrollem

### Sekce „Přidej se k nám" (mobile)
- Pozadí: `rgba(244,196,0,0.68)` (světlý) / tmavá varianta
- Text plnou šířkou, žádné sloupce

### Sekce „Galerie" (mobile)
- Horizontální carousel, 1 obrázek najednou, plná šířka
- Šipky ← → po stranách obrázku
- Výška obrázku: cca 200–250px

### Sekce „Informace pro členy" (mobile)
- Jednosloupcový seznam odkazů (ne dvousloupcový)
- Pořadí: Usnesení představenstva → Stanovy a předpisová základna → Vedení klubu a aktivní členové → Revize elektrospotřebičů → Síť a Internet → FAQ
- Každý odkaz na samostatném řádku, barva `#F4C400` nebo podtržení

### Sekce detailů služeb – Internet, Pošilovna, Tiskárna, Zábava (mobile)
- Text plnou šířkou
- Galerie / carousel pod textem – 1 obrázek najednou, šipky ← →
- Střídání pozadí sekcí zachováno i na mobilu

### Sekce „Odkazy" (mobile)
- Jednosloupcový seznam (ne grid)
- Ikona + text na každém řádku
- Položky (přesně dle prototypu):
  1. Facebook – @kluborlik
  2. Instagram – orlik.klub
  3. Discord – discord.ok.cvut.cz
  4. Informační systém klubu
  5. Klubová wiki
  6. Studentské Unie ČVUT
  7. Správa účelových zařízení ČVUT

### Sekce „Adresa" (mobile)
- Mapa jako placeholder obrázek nebo iframe, plná šířka, výška cca 200px
- Pod mapou: ikona kolíku + text „Terronská 694/6, 160 00 Praha 6"

### Footer (mobile)
- Centrovaný text
- Slogan **„JSEM OK!"** tučně, `#F4C400`
- Text „© 2025 Klub Orlík" pod sloganem

### Obecná CSS pravidla pro mobilní zobrazení
- Veškerý padding sekcí na mobile: `24px 16px`
- Nadpisy sekcí: `font-size: clamp(1.4rem, 5vw, 2rem)`
- Tělo textu: `font-size: 15px`, `line-height: 1.6`
- Tlačítka a odkazy: minimální výška touch targetu `44px`
- Carousel šipky: kruhové, průměr `40px`, pozadí `#F4C400`, ikona `#2B2D33`
- Obrázky: `width: 100%`, `height: auto`, `border-radius: 8px`

### Přístupnost
- Správná heading hierarchie (H1 → H2 → H3)
- Alt texty na všech placeholder obrázcích
- Dostatečný kontrast barev (WCAG AA)

### SEO
- Správné meta title a description přes WordPress SEO funkce
- Open Graph meta tagy v `<head>`

---

## VÝSTUPNÍ STRUKTURA

### ČÁST 1: SOUBORY K VYTVOŘENÍ
Vygeneruj obsah každého souboru kompletně. Každý soubor jen jednou.

### ČÁST 2: INSTALAČNÍ INSTRUKCE
Číslovný seznam kroků pro instalaci theme a pluginů na WordPress 6.9.4.