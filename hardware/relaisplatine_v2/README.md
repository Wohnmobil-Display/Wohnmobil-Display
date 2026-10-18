# Relaisplatine V2 – Bestückung und Aufbau

Optionale Erweiterung für die **Wasserpumpe**: Das Display schaltet damit die Pumpe und misst die Starterbatterie über die grüne Ader.
Platine **48 × 36 mm**, 2 Lagen, 1,6 mm. Es gibt nur noch diese Version (V2).

![Relaisplatine V2](relaisplatine_v2_oben.png)

## Dateien
| Datei | Inhalt |
|---|---|
| `relaisplatine_gerber.zip` | Fertigungsdaten (Gerber + Bohrdaten), beim Platinenhersteller hochladen |
| `relaisplatine_stueckliste.csv` | Stückliste mit LCSC-Nummern |

**Bestellung:** Gerber-ZIP hochladen, 2 Lagen, 1,6 mm, HASL bleifrei, **ohne Bestückung** (alle Teile sind bedrahtet und werden von Hand gelötet).
Kupfer 1 oz reicht, 2 oz ist besser, wenn die Pumpe mehr als 5 A zieht.

## Bauteile (alle bedrahtet)
| Pos. | Teil | Wert / Typ | LCSC | Hinweis |
|---|---|---|---|---|
| K1 | Relais | Panasonic **ALQ312** (nur Schließer, 10 A, Spule 720 Ω / 17 mA) | C425093 | zuletzt einlöten |
| D1 | Freilaufdiode | **1N4007** | C2985028 | **Ring (Kathode) zur Klemme „Starter“ (+)**, liegt parallel zur Relaisspule |
| J1 | Schraubklemme 2-polig, 5,08 mm | „Starter / Grün“ | C474881 | |
| J2 | Schraubklemme 2-polig, 5,08 mm | „Pumpe“ | C474881 | |
| J3 | Schraubklemme 2-polig, 5,08 mm | „Notschalter“ | C474881 | |

Phoenix-Contact-Original zu den Klemmen: **MKDS 1,5/2-5,08** (1729128).

## Bestückungsreihenfolge
1. **D1** (1N4007) einlöten, Ring zeigt zu J1 „Starter“.
2. **J1, J2, J3** (Klemmen) einlöten, Schraubseite zur Kante.
3. **K1** (ALQ312) einlöten (Pin 1 siehe Aufdruck).
4. Sichtprüfung auf Lötbrücken.

## Anschluss
| Klemme | Anschluss |
|---|---|
| **J1 Starter / Grün** | +Starterbatterie (EBL Block 3 Pin 8) und grüne Ader zur Steuerplatine |
| **J2 Pumpe** | Pumpenleitung (+): trennt das Relais, der Schließer (NO) schaltet die Pumpe |
| **J3 Notschalter** | optional: überbrückt das Relais, falls es einmal ausfällt |

Funktion: Relais an (das Display zieht die grüne Ader auf Masse) = Pumpe frei. Relais aus = Pumpe gesperrt, und die Steuerplatine misst die Starterbatterie.
Spulenanschluss am ALQ312: Pin 1 / 5, COM Pin 2, NO Pin 3.

## Prüfung
- Ohne angeschlossene Pumpe: 12 V an J1 „+“ und die grüne Ader kurz auf Masse legen → Relais klickt.
- Mit Pumpe: im Display unter *Setup → Wasserpumpe* die Relaisplatine einschalten und das Wasserhahn-Symbol bedienen.

## Gehäuse
3D-Druck: [`../../druck/relaisplatine_v2_unterschale.stl`](../../druck/relaisplatine_v2_unterschale.stl) und [`../../druck/relaisplatine_v2_deckel.stl`](../../druck/relaisplatine_v2_deckel.stl), Maße siehe [Gehäusezeichnung](../../druck/zeichnungen/gehaeuse_zeichnung_v2.png).
