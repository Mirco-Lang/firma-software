# CLAUDE.md

## Zuerst lesen (Pflicht)
Vor jeder Arbeit lesen und danach handeln:
- Fundament.md: Arbeitsweise, Qualität, Gestaltung, Betrieb
- Werte-DNA.md: meine Werte und wie ich entscheide (sobald sie da ist)
- Unternehmens-DNA.md: wofür die Firma steht, wer die Kunden sind (sobald sie da ist)
Bei Unklarheit gilt die Werte-DNA, nicht das Bauchgefühl.

## Projekt
- Firma: Handelshaus-Lang, Marke „Retouren Großhandel“ (https://retourengrosshandel.com), Güntherstr. 7, 97342 Marktsteft
- Was sie macht: Vermittelt Paletten mit Amazon-Retouren an Geschäftskunden (B2B). Kategorien laut Webseite: Spielzeug, Haushalt, Elektronik, Dekoration, Werkzeug, Textilien, Weiße Ware, Mystery Boxen.
- Ansprechpartner: Mirco Lang, mirco.lang@retourengrosshandel.de, +49 171 1793416
- Ziel: Der ganze Verkauf von der Anfrage bis zur Rechnung läuft automatisch. Für diesen Bereich braucht der Chef keinen menschlichen Mitarbeiter mehr. Er wird nur gerufen, wenn eine Frage nicht beantwortbar ist oder etwas schiefgeht.
- Angeschlossene Werkzeuge: Webseite mit Anfrageformular, Ionos Webmail (dort kommen die Anfragen an), Dropbox von Avides (Palettenlisten als Excel, täglich aktualisiert), Mailadresse handelshaus-angebote@web.de (nur für Avides), Firmenkonto bei der Postbank (nur lesen, um Zahlungen zu prüfen; die KI überweist nie). «weitere …»

## Regeln des Geschäfts
Alle Preise netto. B2B.
- Einkauf: Avides-Preis pro Palette, aus der Dropbox-Liste.
- Aufschlag: Verkaufspreis = Avides-Preis plus 20 %. Gilt für jeden Artikel und für den Gesamtpreis der Palette.
- Mengenrabatt auf den Verkaufspreis (Richtlinie): 1 bis 2 Paletten 0 %, 3 bis 5 Paletten 10 %, ab 6 Paletten 15 %. Vorher bei Avides klären, wie viel Rabatt Avides gibt.
- Avides gibt dem Chef bei mehreren Paletten ebenfalls Rabatt (zum Beispiel 10 %, 15 %, 20 %). Darum bleibt der Gewinn auch mit Kundenrabatt meist bei etwa 20 %. Maßgeblich ist immer der Gesamtpreis, den Avides per Mail nennt.
- Vor jedem Gesamtangebot: Mail an den Avides-Mitarbeiter (über handelshaus-angebote@web.de) mit den SKU-Nummern der gewünschten Paletten und der Lieferadresse des Kunden. Fragen: Sind die Paletten noch da? Welchen Gesamtpreis inklusive Versand an diese Adresse macht Avides? Erst mit dieser Antwort geht an den Kunden eine einzige Mail mit Preisen, Verfügbarkeit und Versand.
- Palette nicht mehr da: Ist eine gewünschte Palette weg, sucht die KI in der Excel-Liste eine ähnliche Palette aus derselben Kategorie (ähnliche Artikel, ähnliche Stückzahl). Sie fragt bei Avides, ob diese da ist. Erst dann bekommt der Kunde das Angebot: die verfügbaren Paletten und die Ersatzpalette als Vorschlag. Will der Kunde den Ersatz nicht, nimmt er nur die verfügbaren.
- Versand: Ab 3 Paletten wird der Versand pro Palette günstiger. Darauf weist die KI den Kunden hin. Den genauen Versandpreis gibt es erst, wenn der Kunde fest sagt, wie viele Paletten er nimmt und wohin sie gehen. Dann fragt die KI Avides nach dem genauen Preis.
- Bevor etwas bestellt wird, ist mit dem Kunden klar und schriftlich: welche Paletten, wie viele, an welche Adresse.
- Kunde sagt fest Ja: Die KI lässt die Paletten bei Avides reservieren. Avides schickt dem Chef die Einkaufsrechnung. Die KI erstellt die Rechnung an den Kunden. Der Unterschied ist der Gewinn des Chefs.
- Geld prüfen: Die KI prüft alle Rechnungen und Zahlungen. Kommt die Rechnung von Avides, und passt sie zur Absprache? Hat der Kunde bezahlt, und stimmt der Betrag? Ist Avides bezahlt? Passt etwas nicht, meldet sie es dem Chef sofort.
- Umsatzsteuer: 19 % auf Ware und auf Versand. Beides immer netto plus 19 %.
- Rechnung: zeigt den Preis pro Palette (mit SKU-Nummer), dazu Versand, netto, 19 % USt, brutto. Jede Rechnung wird fünfmal geprüft, abgelegt und an den Kunden geschickt.

## Rechnungen und Buchhaltung
- Bisher schreibt der Chef Rechnungen mit Bilby. Für diesen Bereich gab es 2026 noch keine Rechnung. Die KI erstellt die Rechnungen ab jetzt selbst.
- Rechnungsnummer: Format RE-Jahr-Zahl. Erste Nummer: RE-2026-1001. Danach lückenlos fortlaufend (RE-2026-1002, RE-2026-1003 …). Keine Nummer wird doppelt vergeben, keine übersprungen. Im neuen Jahr geht es mit RE-2027-1001 weiter.
- Absender auf jeder Rechnung:
  Mirco Lang, Handelshaus-Lang, Güntherstr. 7, 97342 Marktsteft
  USt-IdNr.: DE315442374
  Einzelunternehmen, nicht im Handelsregister. Darum stehen kein Amtsgericht und keine Registernummer auf der Rechnung. Vor- und Nachname (Mirco Lang) stehen immer dabei.
- Bankverbindung auf jeder Rechnung: Postbank Business Giro, IBAN DE18 1001 0010 0002 0791 32. Kunden zahlen dorthin. Avides bucht von dort ab.
- Ablage im Ordner `Buchhaltung/`, je Jahr und Monat:
  - `Buchhaltung/2026/11-November/Ausgang/`: unsere Rechnungen an Kunden (PDF)
  - `Buchhaltung/2026/11-November/Eingang/`: Rechnungen von Avides (PDF)
- Jeden Monat macht die KI die Buchhaltung fertig: Liste aller Ausgangs- und Eingangsrechnungen, wer bezahlt hat und wer nicht, Summe netto, Umsatzsteuer und brutto, Gewinn je Verkauf und im Monat. Alles gegen die Kontobewegungen geprüft.
- Buchhaltung und Kundendaten gehen nicht zu GitHub. Sie stehen in der .gitignore.
- Nachfassen: Meldet sich ein Kunde 3 Tage nach den Listen nicht, bekommt er eine kurze Mail: ob noch Interesse besteht, ob Fragen offen sind.
- Fragen von Kunden beantwortet die KI. Kann sie eine Frage nicht sicher beantworten, benachrichtigt sie den Chef sofort und sichtbar (Benachrichtigung auf dem Bildschirm).

## Geheim, nie nach außen
- Kunden erfahren nie, dass die Ware von Avides kommt.
- Kunden sehen nie den Avides-Preis. Listen, Angebote und Rechnungen an Kunden enthalten nur unsere Preise.
- Mit Avides wird nur über handelshaus-angebote@web.de geschrieben. Mit Kunden nur über die Adresse von Retouren Großhandel. Die beiden Wege werden nie vermischt.

## Abläufe
Jeder Ablauf hat seine eigene Datei im Ordner `Ablaeufe/`.
- Ablaeufe/01-Anfrage-bis-Lieferung.md: vom Eintrag auf der Webseite bis zur gelieferten Palette

## Gestaltung
- Farben: Hauptfarbe «#…», neutrale Farbe «#…», Akzent «#…»
- Schriften: «…»
- Logo: hell «Datei», dunkel «Datei»
- Ton: Kunden werden immer mit „Sie“ angesprochen.

## Server
- Adresse der Software: https://app.«domain»
- Datenbank: Supabase, selbst gehostet, Version «…» (festgenagelt)
- Hintergrund-Abläufe: trigger.dev, selbst gehostet, Version «…» (festgenagelt)
- Das Befehlswerkzeug von trigger.dev hat immer genau die Version des Servers. Nie "latest".
- Beim Anheben: Server und die Pakete trigger.dev, @trigger.dev/sdk sowie @trigger.dev/build gemeinsam.
- Störungen und ihre Lösung: server/SERVER-BETRIEB.md

## Ablage und Abgleich
- Der Projektordner liegt in Dokumente. Dokumente wird mit iCloud oder OneDrive abgeglichen.
- Große Hilfsordner bleiben aus dem Abgleich heraus: node_modules, .next, dist, build, .venv, .turbo, .cache und ähnliche.
- Sobald so ein Ordner entsteht, richtet die KI das ein (zum Beispiel: Hilfsordner außerhalb von Dokumente ablegen und im Projekt nur darauf verweisen) und prüft danach, dass er nicht mehr abgeglichen wird.
- Installationsdateien (.exe) gehören nicht ins Projekt und nicht zu GitHub.

## Feste Regeln
1. Passwörter, Schlüssel und .env nie zu GitHub.
2. Alles, was nach außen geht, ist fünfmal geprüft und gegen die echten Daten gehalten.
3. Was etwas löscht oder Geld kostet, zeigt die KI vorher und wartet auf ein Ja.
   Ausnahme, vom Chef am 3. November 2026 so entschieden: Alle Mails im Verkaufsablauf (Listen, Nachfassen, Antworten, Anfragen an Avides, Angebote, Rechnungen) verschickt die KI ohne vorheriges Ja. Diese Regel geht für diesen Bereich dem Satz im Fundament vor („Nichts geht nach außen ohne das Ja des Chefs“). Die Fünffach-Prüfung gilt weiter für jede Mail. Geht etwas schief, meldet die KI es dem Chef sofort.
4. Fertig gebaut heißt veröffentlicht. Die KI veröffentlicht selbst und prüft danach, dass es wirklich läuft.
5. Werte und Strategie steuern innen. Sie scheinen nie nach außen durch.
6. Alles, was regelmäßig läuft, läuft auf dem Server. Nie auf dem Laptop.
