# Vorgehen: Eine Preisliste von Avides lesen

Geprüft am 3. November 2026 an der Datei `Electronics/261030 Apple accessories.xlsx`.

## Wo die Listen liegen
- Dropbox-Ordner „Pricelists“ von Avides Media AG. Der Link steht in `Passwoerter/zugaenge.txt`. Keine Anmeldung nötig.
- 9 Unterordner: Defective Goods, Electronics, Electronics Kilo Price, Fashion single boxes, Fashion Sportswear single boxes, Fashon Stocks, Manufacturer Stocks, Other Pricelists, Special Offers.
- Dateiname beginnt mit dem Datum als JJMMTT, zum Beispiel `261030` = 30. Oktober 2026. Daran erkennt man neue Listen.
- Herunterladen: Ordner- oder Datei-Link mit `dl=1` statt `dl=0`.

## So ist eine Liste aufgebaut
- Ein Tabellenblatt namens „Packinglist“.
- Zeile 1 ist die Überschrift. Spalten:

| Spalte | Überschrift | Bedeutung |
|---|---|---|
| A | Lager-ID | Nummer des einzelnen Artikels (z. B. W26-EL6243) |
| B | SKU | Nummer der **Palette** (z. B. K26878-232). Alle Artikel einer Palette haben dieselbe SKU. |
| C | Bezeichnung | Name des Artikels, oft in der Sprache des Herkunftslands |
| D | EAN | Strichcode-Nummer |
| E | ASIN | Amazon-Nummer |
| F | Condition | Zustand: „Retourware“ oder „B-Ware“ |
| G | Land | Herkunftsland (DE, IT, FR, UK, PL, NL, BE, SE …) |
| H | VK Netto | **Avides-Preis** des Artikels, netto, in Euro |

- Eine Datei kann mehrere Paletten enthalten. Nach jeder Palette folgt eine Summenzeile: nur Spalte H, mit einer Formel wie `SUM(H2:H85)`. Diese Zeile ist kein Artikel.
- Spalte J enthält manchmal eine 1 beim letzten Artikel einer Palette. Ohne Bedeutung für uns.

## Beispiel aus der geprüften Datei
| Palette (SKU) | Artikel | Avides-Preis | Unser Preis (+20 %) |
|---|---|---|---|
| K26878-232 | 84 | 2.425,01 € | 2.910,29 € |
| K26896-028 | 119 | 2.899,51 € | 3.479,73 € |

Zweimal auf zwei verschiedenen Wegen nachgerechnet. Das Aufrunden je Artikel bringt etwa 0,01 % mehr als genau 20 %.

## So rechnen wir
- Jeder Artikel: Avides-Preis mal 1,2, **auf den Cent aufgerundet**.
- Palettenpreis = Summe der gerundeten Artikelpreise. So stimmt die Summe in der Liste für den Kunden immer, und der Aufschlag ist nie kleiner als 20 %.
- In der Liste für den Kunden fehlt der Avides-Preis ganz. Auch keine versteckte Spalte, keine Formel, keine Notiz in der Datei.

## Woran es scheitern kann
- Summenzeilen nicht als Artikel zählen.
- Preise haben manchmal Rechenfehler-Nachkommastellen (70.150000000000006). Immer erst auf Cent runden, dann rechnen.
- Umlaute in Bezeichnungen sind manchmal kaputt (z. B. „USBâ€‘C“). Beim Lesen als UTF-8 behandeln, beim Schreiben prüfen.
