---
title: padding-right
slug: Web/CSS/padding-right
tags:
  - CSS
  - CSS Referenz
translation_of: Web/CSS/padding-right
---
{{ CSSRef() }}

## Übersicht

Die `padding-right` Eigenschaft legt den rechten Innenabstand eines Elementes fest. Der Innenabstand ist der Bereich zwischen dem Inhalt und dem [Rahmen](/de/CSS/border "de/CSS/border") (auch: _padding area_).

- Standardwert: `0`
- Anwendbar auf: alle Elemente außer `table-*-group`, `table-row` und `table-column`
- Vererbbar: Nein
- Prozentwerte: beziehen sich auf die [Breite](/de/CSS/width "de/CSS/width") des umschließenden Blocks.
- Medium: visuell
- berechneter Wert: eine Prozentzahl wie festgelegt oder die absolute Länge.

## Syntax

    padding-right: <Längenangabe> | <Prozentzahl> | inherit

### Werte

- \<Längenangabe>
  - : Legt eine bestimmte [Länge](/de/CSS/Einheiten#L.c3.a4ngen "de/CSS/Einheiten#L.c3.a4ngen") fest. Negative Werte sind **nicht** erlaubt.
- \<Prozentzahl>
  - : Ein [prozentualer](/de/CSS/Einheiten#Prozent "de/CSS/Einheiten#Prozent") Wert, der sich auf die Breite des umschließenden Blocks (containing block) bezieht. Negative Werte **nicht** sind erlaubt.
- inherit
  - : Der Wert des Elternelements wird geerbt.

## Beispiele

    .content { padding-right: 5%; }
    .sidebox { padding-right: 10px; }

## Browser Kompatibilität

| Browser           | ab Version |
| ----------------- | ---------- |
| Internet Explorer | 4.0        |
| Firefox (Gecko)   | 1.0 (1.0)  |
| Opera             | 3.5        |
| Safari (WebKit)   | 1.0 (85)   |

## Spezifikation

- {{ spec("http://www.w3.org/TR/CSS21/box.html#padding-properties","CSS 2.1 Box: padding", "CR") }}

## Siehe auch

- [`padding`](/de/CSS/padding "de/CSS/padding"), [`padding-top`](/de/CSS/padding-top "de/CSS/padding-top"), [`padding-bottom`](/de/CSS/padding-bottom "de/CSS/padding-bottom"), [`padding-left`](/de/CSS/padding-left "de/CSS/padding-left")
- [`-moz-padding-start`](/de/CSS/-moz-padding-start "de/CSS/-moz-padding-start"), [`-moz-padding-end`](/de/CSS/-moz-padding-end "de/CSS/-moz-paddding-end")
- [`margin`](/de/CSS/margin "de/CSS/margin")

{{ languages( { "en": "en/CSS/padding-right", "ja": "ja/CSS/padding-right" } ) }}