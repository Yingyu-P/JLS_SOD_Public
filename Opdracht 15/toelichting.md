# Toelichting – bestelscherm Ruilkast Kledingruil

## 1. Id- en class-selectors

**`#winkelnaam` (id).** De winkelnaam in de `<h1>` komt maar één keer op de pagina voor. Een id mag per pagina maar één keer gebruikt worden, dus dit is een uniek onderdeel waar een id bij past. Ik kan er ook later naar verwijzen (bijvoorbeeld met een link).

**`.kaart` (class).** Elk kledingstuk is een kaart met dezelfde opmaak. Een class mag je op meerdere elementen zetten, dus één regel CSS styled alle kaarten.

**`.bestelknop` (class).** De knop kan later meerdere keren voorkomen (bijvoorbeeld per sectie), dus ook hier een class.

**Overige classes.** `.instructie`, `.tip`, `.veld` en `.kaarten` gebruik ik voor herhaalde of groepsgewijze onderdelen.

**Vuistregel:** id = één uniek element; class = onderdeel dat herhaald wordt.

## 2. Het boxmodel

Elk element is een doos met vier lagen, van binnen naar buiten:

1. **Content:** de inhoud zelf. Bij de Winterjas: de titel, de omschrijving en de checkbox.
2. **Padding:** ruimte tussen de inhoud en de rand, *binnen* de doos. De Winterjas-kaart heeft `padding: 1rem`, zodat de tekst niet tegen de rand aan staat.
3. **Border:** de rand om de padding. De kaart heeft `border: 2px solid #1f5a43`, waardoor hij als los blok herkenbaar is.
4. **Margin:** ruimte *buiten* de rand. Met `margin: 1rem` staat de Winterjas-kaart niet tegen de Wollen trui aan.

Dus: padding zit **binnen** de rand, margin **buiten** de rand.

## 3. Font-eigenschappen en text-eigenschappen

De winkelnaam en de kopjes zijn vetgedrukt met `font-weight: 700`. De instructie en de tip zijn cursief met `font-style: italic`. Dit zijn font-eigenschappen: ze bepalen hoe het lettertype eruitziet. Een text-eigenschap zoals `text-align` bepaalt juist hoe de tekst in de ruimte wordt geplaatst (uitlijning).

- **Scheiding van HTML en styling:** de HTML beschrijft alleen structuur en inhoud, de CSS het uiterlijk. Zo blijft de code leesbaar en kan ik het uiterlijk aanpassen zonder de HTML aan te raken.
- **Herbruikbaarheid:** één regel voor `.kaart` geldt voor alle kaarten. Voegt de winkel later een nieuwe jas, rok of sjaal toe, dan kopieer je alleen een `<article class="kaart">` en heeft die direct dezelfde opmaak.
- **Onderhoud:** wil de winkel de randkleur of padding aanpassen, dan wijzig je dat op één plek in plaats van in tientallen inline `style`-attributen.
- **Meerdere pagina's:** dezelfde stylesheet kan gekoppeld worden aan andere pagina's, zodat de hele site een consistente uitstraling houdt.