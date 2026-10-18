# Wohnmobil-Display – dein Wohnmobil immer im Blick

**Alles wird überwacht – und du bekommst eine Nachricht aufs Handy, wenn etwas nicht stimmt.**

Ein 7-Zoll-Touchdisplay, das rund um die Uhr auf dein Wohnmobil aufpasst:

- 🔋 **Spannung und Ladezustand** von Starter- und Aufbau-Batterie, jede einzelne Zelle des JK-BMS
- ☀️ **Solarertrag** vom Victron-Laderegler, heute und die letzten 7 Tage
- 💧 **Frisch- und Abwasser** – Warnung, bevor der Tank leer bzw. voll ist
- 🔥 **Gasflaschen** in Prozent – Warnung, bevor das Gas ausgeht
- 🌡️ **Temperaturen** innen, außen und im Kühlschrank – Warnung bei zu warm oder zu kalt
- 🚨 **Alarmanlage** mit Tür-, Fenster- und Bewegungsmeldern, **Rauch- und Gasmelder** rund um die Uhr
- 📱 **Push-Nachrichten per Telegram** für jede Warnung – du entscheidest, worüber du informiert werden willst
- 🗓️ **Tagesbericht per Telegram:** einmal am Tag zur Wunschzeit alle wichtigen Werte aufs Handy – Batterien, Tanks, Gas, Solar, Temperaturen, Alarm (ab dem nächsten Update)
- 📡 **Sensor offline oder Batterie schwach?** Auch das meldet das Display

Es ersetzt das originale Schaudt-Bedienteil **LT 100** und nutzt dessen **vorhandene Stecker und Kabel**.
Für die dauerhafte Nutzung ist ein einmaliger **Freischaltcode** nötig (siehe [Freischalten](#3-freischalten)).
Es ist ein **privates Hobbyprojekt**; Einbau und Nutzung erfolgen **auf eigene Verantwortung** (siehe [Hinweis](#hinweis-haftung-und-eigenverantwortung)).

![Startseite](bilder/startseite.png)

**Inhalt:** [Funktionen](#funktionen) · [Bedienung](#bedienung) · [Hardware](#hardware) · [Einkaufsliste](#einkaufsliste) ·
[Installation](#1-installation) · [Erster Start](#2-erster-start) · [Freischalten](#3-freischalten) · [Updates](#4-updates)

## Funktionen

| Bereich | Was das Display kann |
|---|---|
| **Batterien** | Motor- und Aufbau-Batterie, JK-BMS mit allen 12 Zellen, Temperaturen und Ladezustand (Bluetooth) |
| **Solar** | Victron-MPPT-Laderegler: Leistung, Tagesertrag, Verlauf der letzten 7 Tage (Bluetooth) |
| **Wasser** | Frischwasser über den Original-Geber oder die Votronic-Tankelektrode, Abwasser über die Original-Elektrodenstäbe |
| **Pumpe** | Wasserpumpe per Fingertipp ein/aus, automatisch gesperrt bei scharfer Alarmanlage |
| **Gas** | Zwei Gasflaschen mit Mopeka-Pro-Sensoren in Prozent (Bluetooth) |
| **Temperatur** | Innen (Wohn- und Schlafbereich), außen, Kühlschrank – über Zigbee-Sensoren oder fest verbaute Fühler |
| **Alarmanlage** | Bis zu 12 Zigbee-Sensoren (Tür/Fenster, Bewegung, Wasser), Nachtmodus, Verlassens-/Eingangszeit, PIN, Summer, Sirene |
| **Rauch / Gas** | Zigbee-Melder, rund um die Uhr überwacht |
| **Landstrom** | Anzeige, ob 230 V anliegen |
| **Push-Nachrichten** | Alarm, Grenzwerte, schwache Batterien, Sensor offline – per Telegram aufs Handy |
| **Tagesbericht** | täglich zur eingestellten Uhrzeit eine Zusammenfassung per Telegram, Inhalte frei wählbar (ab dem nächsten Update) |
| **Komfort** | Kachelnamen und Farben frei wählbar, Nachtabschaltung, Näherungssensor weckt das Display, Einstellen per Handy-Webseite |
| **Updates** | Neue Versionen per WLAN direkt am Display |

## Bedienung

Die komplette **[Bedienungsanleitung (PDF)](docs/Bedienungsanleitung.pdf)** zeigt jede Seite und jede Einstellung.

| **Startseite mit Beispielwerten** | **Innen: Detailseite mit zwei Sensoren** |
|---|---|
| ![Startseite](bilder/screenshots/dash.png) | ![Detailseite Innen](bilder/screenshots/detail0.png) |
| **Detailseite Außen** | **Detailseite Rauch/Gas** |
| ![Detailseite Außen](bilder/screenshots/detail1.png) | ![Detailseite Rauch/Gas](bilder/screenshots/detail3.png) |
| **Alarmanlage ein-/ausschalten** | **Victron / Solar mit 7-Tage-Verlauf** |
| ![PIN-Dialog](bilder/screenshots/alarmpin.png) | ![Victron](bilder/screenshots/victron.png) |
| **JK-BMS mit Zellspannungen** | **Zigbee-Geräte** |
| ![JK-BMS](bilder/screenshots/bms.png) | ![Zigbee](bilder/screenshots/zigbee.png) |

**Einstellungen (Setup):**

| Alarmanlage | Display |
|---|---|
| ![Setup Alarmanlage](bilder/screenshots/alarm.png) | ![Setup Display](bilder/screenshots/display.png) |
| **Nachtabschaltung** | **Allgemein** |
| ![Nachtabschaltung](bilder/screenshots/night.png) | ![Setup Allgemein](bilder/screenshots/allgemein.png) |
| **Wasserpumpe** | **Gasflaschen (Mopeka)** |
| ![Setup Wasserpumpe](bilder/screenshots/pump.png) | ![Setup Gasflaschen](bilder/screenshots/mopeka.png) |
| **Push-Nachrichten** | **Tagesbericht** |
| ![Setup Push](bilder/screenshots/push.png) | ![Tagesbericht](bilder/screenshots/tagesbericht.png) |
| **Victron-Laderegler** | **Farbauswahl Kachel** |
| ![Setup Victron](bilder/screenshots/victronsetup.png) | ![Farbauswahl](bilder/screenshots/tilecolors.png) |

*Alle Bilder mit Beispielwerten; Bot-Token, Chat-ID und Victron-Schlüssel sind im Bild ausgeblendet.*

- **Startseite:** 12 Kacheln, oben Uhrzeit, Landstrom, Störmeldungen, Wasserpumpe und Setup.
- **Rote Kachel:** ein eingestellter Grenzwert ist verletzt (z. B. Frischwasser fast leer).
- **Antippen** öffnet Detailseiten (Solar, BMS, Temperaturen) bzw. die PIN-Eingabe der Alarmanlage.
- **Setup:** keine Speichern-Taste – alles wird sofort gespeichert.

## Hardware

![Systemübersicht](bilder/systemuebersicht.svg)

Das System besteht aus dem **Display** und der **Steuerplatine** – beide sind nötig.
Die **Relaisplatine** für die Wasserpumpe ist eine Erweiterung, die man weglassen kann.

- **Display:** Waveshare ESP32-S3-Touch-LCD-7B (7 Zoll, 1024×600, WLAN, Bluetooth).
  Bluetooth-Geräte (Victron, Mopeka, JK-BMS) empfängt es direkt.
- **3D-Druckteile** im Ordner [`druck/`](druck/): **Rahmen für das Display** (ersetzt das LT 100 im vorhandenen Ausschnitt, mit oder ohne Näherungssensor), **Halter für Türkontakte** (Sensor und Magnet, verschiedene Sockelhöhen), **Gehäuse** für Steuer- und Relaisplatine und ein **Wassertank-Deckel für den Votronic-Tankfühler 5545** (Deckel in PETG mit 4 Wänden, Dichtungsring in TPU mit 3 Wänden – es geht auch der Original-Dichtring).

### Steuerplatine – notwendig

![Steuerplatine](bilder/steuerplatine.png)

Die Steuerplatine ist die Verbindung zwischen Display und Fahrzeug. Sie sitzt dort, wo vorher das LT 100 war,
und bekommt **die vorhandenen Original-Stecker** – es muss kein neues Kabel durchs Fahrzeug gezogen werden.
Auf ihr steckt das **ESP32-H2-Board**, das die Messwerte erfasst und das **Zigbee-Funknetz** betreibt.
Mit dem Display ist sie über **ein USB-Kabel** verbunden.

| Anschluss | Was angeschlossen wird |
|---|---|
| **ST1 – EBL** (Original-Stecker) | Stromversorgung 12 V, Hauptschalter **EIN/AUS**, 12-V-Kontrolle, **Landstrom** (230 V liegt an) |
| **ST2 – Frischwasser** (Original-Stecker) | Originaler Tankgeber (Stabsonde) **oder** Votronic-Tankfühler 5545 (Tankelektrode 15-50 K) – umschaltbar per Steckbrücken J12/J13 |
| **ST3 – Abwasser** (Original-Stecker) | Originale Elektrodenstäbe (25 / 50 / 75 / 100 %) |
| **Klemme GRÜN** | Freie grüne Ader im Panelkabel: misst die **Starterbatterie** und schaltet die Relaisplatine |
| **Klemme 5V DISPLAY** | Versorgt das Display – ein eigenes Netzteil ist nicht nötig |
| **Klemme SIRENE** | Alarmsirene (überwacht auf Kurzschluss und offene Leitung) |
| **Klemmen DS18B20** | Fest verbaute Temperaturfühler (z. B. innen, Kühlschrank) |
| **USB** | Verbindung zum Display |

Gemessen werden Starter- und Aufbau-Batterie, 12-V-Kontrolle und Landstrom.
**Ohne Steuerplatine** zeigt das Display nur die Bluetooth-Geräte – Tanks, Hauptschalter, Landstrom,
Pumpe und alle Zigbee-Sensoren (Alarmanlage, Rauchmelder, Temperaturen) funktionieren dann nicht.

**Frischwasser: Originalgeber oder Votronic-Tankelektrode** – die Steuerplatine hat dafür zwei Steckbrücken
J12/J13 neben ST2. **Beide immer auf dieselbe Seite** stecken, nur stromlos umstecken. Danach im Display unter
*Setup → Frischwasser → Geber* den passenden Geber wählen:

| Steckbrücken | ST2 Pin 1 | ST2 Pin 4 | ST2 Pin 5 | Geber |
|---|---|---|---|---|
| **rechts „ORIG“** (Standard) | Stab Voll | Stab ¼ | Basis | Originalgeber (Stabsonde des LT 100), Stufen 25 / 50 / 75 / 100 % |
| **links „VOT“** | +12 V (über selbstrückstellende Sicherung) | Signal 0–2,2 V | Masse | Votronic-Tankelektrode 15-50 K, stufenlos |

**Deckel für den Votronic-Tankfühler:** Für den Einbau des Fühlers gibt es einen **Wassertank-Deckel mit 37-mm-Bohrung** und einen
**Dichtungsring** zum Selbstdrucken. **Deckel, Griff und Bolzen gehören zusammen** ([Deckel](druck/wassertank_deckel_votronic_5545.stl),
[Griff](druck/wassertank_griff_votronic_5545.stl), [Bolzen](druck/wassertank_bolzen_votronic_5545.stl)), dazu der
[Dichtungsring](druck/wassertank_dichtring_tpu.stl). Den **Deckel in PETG mit 4 Wänden** drucken, den **Dichtungsring in TPU
mit 3 Wänden**. Zusatzinfo: Es kann auch der **Original-Dichtring** des Tanks weiterverwendet werden.

**So gehören die drei Teile zusammen:** Das Öffnen und Schließen des Tankdeckels braucht etwas Kraft. Deshalb gibt es zwei **Griffe**,
die als Hebel auf dem **Deckel** sitzen. Die **Bolzen** stecken Griff und Deckel zusammen, sorgen für eine saubere, passgenaue Verbindung
und verhindern, dass sich der Griff verdreht. Weil alles **in drei Einzelteilen** gedruckt wird, liegt jedes Teil sauber auf dem Druckbett
und die Teile lassen sich **ohne Stützmaterial** drucken.

**Fühler kürzen:** Der Votronic-Tankfühler lässt sich kürzen. Bei meinem Tank habe ich ihn auf **165 mm** eingekürzt, sodass das
untere Ende **mindestens 1 cm Abstand zum Tankboden** hat und nicht aufsetzt; danach wird unten wieder die **Endkappe** aufgesetzt. Die passende Länge
hängt von deinem Tank ab – vorher ausmessen. Nach dem Einbau im Display unter *Setup → Frischwasser* neu einmessen (Leer/Voll).

| 6-poliger Original-Stecker des Tankfühlers | Gedruckter Tankdeckel mit Dichtungsring |
|---|---|
| ![Tankfühler-Stecker](bilder/tankdeckel/tankfuehler_stecker_6polig.jpg) | ![Tankdeckel](bilder/tankdeckel/tankdeckel_votronic_gedruckt.jpg) |

![Tankdeckel von oben](bilder/tankdeckel/tankdeckel_votronic_oben.jpg)

**Fertiger Tankdeckel mit Votronic-Fühler:** Deckel, Griffe und Bolzen sind gedruckt, der Fühler (hier auf die Tanklänge gekürzt)
sitzt in der 37-mm-Bohrung, der Dichtring dichtet ihn ab, und am unteren Ende ist wieder die Endkappe aufgesetzt.

| Deckel mit eingebautem Fühler | Fühlerfuß von innen | Fühlerfuß mit Dichtring |
|---|---|---|
| ![Deckel mit Fühler](bilder/tankdeckel/tankdeckel_fuehler_montiert.jpg) | ![Fühlerfuß](bilder/tankdeckel/tankfuehler_fuss_von_innen.jpg) | ![Fühlerfuß mit Dichtring](bilder/tankdeckel/tankfuehler_fuss_mit_dichtring.jpg) |

| Deckel von unten (Bohrung 37 mm) | Deckel von oben mit den zwei Griffen |
|---|---|
| ![Deckel Unterseite](bilder/tankdeckel/tankdeckel_unterseite.jpg) | ![Deckel Oberseite](bilder/tankdeckel/tankdeckel_oberseite_griffe.jpg) |

![Deckel mit schwarzem TPU-Dichtring auf dem Tankstutzen](bilder/tankdeckel/tankdeckel_mit_tpu_dichtung.jpg)

Der Votronic-Tankfühler 5545 wird im Display eingemessen: bei leerem Tank **Leer = jetzt**, bei vollem Tank **Voll = jetzt** antippen.

**Votronic-Tankfühler am Original-Stecker anschließen** (Pin 1 = +12 V, Pin 4 = Signal, Pin 5 = Masse, Pin 2/3/6 bleiben frei):

![Votronic-Tankfühler am Stecker ST2](bilder/anschluss_frischwasser_votronic_v2.svg)

![Steckbrücken J12/J13: rechts Originalgeber, links Votronic](bilder/frischwasser_jumper_v2.png)

![Lage der Anschlüsse auf der Steuerplatine V2](bilder/steuerplatine_v2_uebersicht.png)

![Frischwasser-Anschluss an der Steuerplatine](bilder/anschluss_frischwasser_original_v2.svg)

#### Steuerplatine aus meinem Restbestand

Die Steuerplatine habe ich im Rahmen meines Hobbys für mich selbst entwickelt und bestellt. Da man bei der
Fertigung eine Mindestmenge abnehmen muss, sind **9 Stück** übrig. Einzelne Platinen gebe ich zum reinen
**Selbstkostenpreis von 30,68 € zuzüglich Versand** von Bastler zu Bastler ab.
(Der Preis ergibt sich aus den Gesamtkosten von 306,80 € für 10 Platinen – darin sind die Kosten einer früheren,
nicht mehr nutzbaren Kleinserie von 5 Platinen enthalten – geteilt durch 10. Es wird kein Gewinn erzielt.)
Die Platinen sind **fertig bestückt – nur das ESP32-H2-Board fehlt** (das steckt man selbst auf, siehe Einkaufsliste). Du kannst die Platine auch **selbst fertigen lassen**:
Die Fertigungsdaten (Gerber, Stückliste, Bestückung) liegen unter
[`hardware/steuerplatine_v2/`](hardware/steuerplatine_v2/) und lassen sich bei jedem Platinenfertiger (z. B. JLCPCB) hochladen –
oft schon ab 1 Stück, direkt nach Hause geliefert.

Interesse? Bitte ein **Issue** hier auf GitHub öffnen oder eine Mail an **wohnmobil.display@gmail.com** schreiben.

**Wichtig beim Einbau:** Vor dem Tausch unbedingt die entsprechende **Sicherung im Wohnmobil ziehen oder das
Bordnetz komplett stromlos schalten**. Beim Ab- und Anstecken kann ein Werkzeug sonst einen Kurzschluss am
Fahrzeugrahmen (Masse) verursachen. Danach die Original-Stecker von der alten Platine abziehen, auf die neue
Platine stecken und vor dem Einsetzen der Sicherung prüfen, dass alle Stecker fest und gerade sitzen.

**Haftungsausschluss:** Dies ist ein rein privater Gefälligkeitsdienst ohne Gewinnabsicht und kein kommerzielles
Angebot. Ich schließe jegliche Gewährleistung, Garantie, Sachmängelhaftung und ein Rückgaberecht komplett aus.
Einbau und Nutzung erfolgen **auf eigene Gefahr**. Für Schäden am Fahrzeug, an der Bordelektronik oder
Folgeschäden (z. B. durch Kurzschlüsse) wird keine Haftung übernommen.

### Relaisplatine für die Frischwasserpumpe – optional

![Relaisplatine](bilder/relaisplatine.png)

**Aufbau und Bestückung:** [Relaisplatine V2 – Bauteile, Reihenfolge, Anschluss](hardware/relaisplatine_v2/README.md) (Gerber-Dateien und Stückliste liegen dort).

Beim originalen LT 100 lässt sich die Wasserpumpe nicht schalten – hier schon:

- **Pumpe per Fingertipp ein/aus** über das Wasserhahn-Symbol oben auf der Startseite.
- **Automatisch aus, wenn die Alarmanlage scharf ist** – kein Wasser läuft unbemerkt, während du weg bist.
- **Anschluss für einen Notschalter**: überbrückt das Relais, falls einmal etwas nicht funktioniert – die Pumpe läuft dann wie früher.
- Die Platine wird am EBL in die Plus-Leitung der Pumpe eingesetzt und über die grüne Ader von der Steuerplatine geschaltet.

**Keine Relaisplatine?** Unter *Setup → Allgemein → Wasserpumpe (Relaisplatine)* ausschalten –
dann verschwinden das Wasserhahn-Symbol und alle Pumpen-Meldungen, alles andere läuft weiter.

**Die Original-Stecker werden einfach umgesteckt – kein neues Kabel durchs Fahrzeug:**

| LT 100 mit den Original-Steckern | Stecker abgezogen |
|---|---|
| ![LT 100 Platine](bilder/lt100_platine_stecker.jpg) | ![Stecker abgezogen](bilder/lt100_stecker_abgezogen.jpg) |

| Kabel zum EBL (ST1) | EBL 31, Block 3 „Instr.-Tafel“ |
|---|---|
| ![ST1](bilder/lt100_kabel_st1.jpg) | ![EBL 31](bilder/ebl31_block3.jpg) |

**Wichtig: Die grüne Ader muss durchverbunden werden.** Die freie grüne Ader im Panelkabel misst die **Spannung der
Motor-(Starter-)Batterie** und **schaltet die Wasserpumpe** (Relaisplatine). Am EBL (Block 3) ist sie das freie grüne
Aderende. Damit sie an der Steuerplatine ankommt, muss sie **unten im Schrank unter dem Kühlschrank durchverbunden
werden** (dort stecken die Stecker des Panelkabels) – z. B. mit einem Quetschverbinder und einer Zusatzleitung:

| Die grüne Ader am EBL | Im Schrank unter dem Kühlschrank durchverbinden |
|---|---|
| ![Grüne Ader am EBL](bilder/gruene_ader_ebl_ende.jpg) | ![Grüne Ader durchverbunden](bilder/gruene_ader_schrank_verbindung.jpg) |
| **Stecker des Panelkabels im Schrank** | **Übersicht mit Verbinder** |
| ![Stecker im Schrank](bilder/gruene_ader_schrank_stecker.jpg) | ![Übersicht im Schrank](bilder/gruene_ader_schrank_ueberblick.jpg) |

**12-V-Dauerspannung am EBL-Stecker Block 5 (Pin 3):** Den passenden **Crimpkontakt (Stift)** aus dem Steckverbinder-Set
(siehe Einkaufsliste) auf die Ader crimpen und in den freien Platz am Stecker stecken:

| EBL Block 5 – freie Plätze | Passender Crimpkontakt (Stift) |
|---|---|
| ![Block 5](bilder/ebl_block5_stecker.jpg) | ![Crimpkontakt](bilder/ebl_block5_crimpkontakt.jpg) |

Anschlüsse am Display:

![Anschlüsse am Display](bilder/anschluesse_display.svg)

**Summer und Näherungssensor** kommen direkt an das Display (Buchsen J8 und H1). Die Stecker mit Kabel
sind vorhanden – nur die beiden Bauteile an die Kabelenden anlöten:

![Summer und Näherungssensor am Display](bilder/anschluss_summer_sensor_display.svg)

**Der Näherungssensor ist optional.** Er macht das System nur komfortabler: das Display wird hell, sobald jemand davor
steht. Das Display funktioniert genauso **ohne Sensor** – dann weckt man es einfach per Fingertipp. Die Auswertung
lässt sich unter *Setup → Display → Näherungssensor* ausschalten. Für den Rahmen gibt es beide Varianten:
[Rahmen mit Näherungssensor](druck/display_rahmen_mit_sensor.stl) und
[Rahmen ohne Sensor](druck/display_rahmen_ohne_sensor.stl) (ohne Aussparung für den Sensor).

## Einkaufsliste

| Teil | Wofür | Link |
|---|---|---|
| Waveshare ESP32-S3-Touch-LCD-7B (7 Zoll, 1024×600) | Das Display | [Amazon\*](https://www.amazon.de/dp/B0FG354VCN?tag=wohnmobildisp-21) |
| ESP32-H2-DevKitM-1 (N4) | Zigbee und Steuerplatine | [Amazon\*](https://www.amazon.de/dp/B0D8XR48LF?tag=wohnmobildisp-21) |
| Votronic Tankfühler 5545 (Tankelektrode 15-50 K, 50 cm) | Frischwasser (optional, statt Original-Geber) – 3 Adern: +12 V, Masse, Signal; Steckbrücken J12/J13 auf „VOT“ | [Amazon\*](https://www.amazon.de/dp/B00IG69OOI/?tag=wohnmobil-21) |
| frient Smoke Alarm (Zigbee-Rauchmelder mit Sirene) | Rauchmelder, auch als Alarm-Sirene nutzbar | [Amazon\*](https://www.amazon.de/dp/B08WXV3G8P?tag=wohnmobildisp-21) |
| SONOFF SNZB-02B (Zigbee-Temperatur/Luftfeuchte) | Temperatur innen, außen, Kühlschrank | [Amazon\*](https://www.amazon.de/dp/B0H4QJQFKM?tag=wohnmobildisp-21) |
| SONOFF SNZB-04P (Zigbee-Tür-/Fensterkontakt) | Alarmanlage | [Amazon\*](https://www.amazon.de/dp/B0DD3SQYV9?tag=wohnmobildisp-21) |
| SONOFF SNZB-03P (Zigbee-Bewegungsmelder) | Alarmanlage | [Amazon\*](https://www.amazon.de/dp/B0C1GB4DVR?tag=wohnmobildisp-21) |
| Mopeka Pro (Ultraschallsensor mit Magnet) | Gasflaschen-Füllstand (optional) | [Amazon\*](https://www.amazon.de/dp/B0GCD1Q4HP?tag=wohnmobildisp-21) |
| VL53L0X-Näherungssensor (2 Stück) | Display wird hell, wenn jemand davor steht (optional) – getestet, funktioniert sofort | [Amazon\*](https://www.amazon.de/dp/B0FPQRKR9T?tag=wohnmobildisp-21) |
| Steckverbinder-Set 6-polig MATE-N-LOK (Kalitec KALI-1106, 6,35 mm, inkl. Crimpkontakte und Dichtungen, bis 19 A) | 12-V-Dauerspannung am EBL-Stecker Block 5 Pin 3 abgreifen (dort liegt auch der Wassertank-Anschluss): Crimpkontakt auf die Ader, in den freien Platz am EBL-Stecker einstecken | [Amazon\*](https://www.amazon.de/dp/B0DP58HVVM/?tag=wohnmobildisp-21) |
| USB-C-Datenkabel (240 W, Set: 1 m + 1 m + 1,5 m + 1,5 m) | Verbindung Display ↔ Steuerplatine und Anschluss am Computer – reines Ladekabel funktioniert nicht | [Amazon\*](https://www.amazon.de/dp/B0GX5WF5B9/?tag=wohnmobildisp-21) |
| Schrauben M3 × 8 mm (100 Stück, Edelstahl, Flachkopf, vollgewinde) | Montage | [Amazon\*](https://www.amazon.de/dp/B0FHGSGFY4/?tag=wohnmobildisp-21) |

\* Werbelink: Als Amazon-Partner verdiene ich an qualifizierten Verkäufen. Für dich ändert sich am Preis nichts.

## 1. Installation

Die Firmware wird direkt im Browser installiert – ohne Download und ohne Zusatzprogramm.

**Du brauchst:**
- ein USB-Datenkabel (ein reines Ladekabel funktioniert nicht),
- einen Computer mit **Google Chrome** oder **Microsoft Edge**,
- kein anderes Programm, das gerade auf den USB-Anschluss zugreift (z. B. Arduino IDE, serieller Monitor).

Es werden **zwei Geräte** installiert – beide auf derselben Installer-Seite, jedes mit eigenem Knopf:

| Gerät | Anschluss am Computer | Direkt zum Knopf |
|---|---|---|
| **① Display** (Waveshare 7 Zoll) | USB-C-Buchse **„UART1“** am Display (Schalter SW1 auf „UART1“) | **[Display installieren](https://wohnmobil-display.github.io/Wohnmobil-Display/#display)** |
| **② Steuerplatine** (ESP32-H2-Board) | Buchse **„USB“** am H2-Board (nicht „UART“), einmal **vor dem Einbau** | **[Steuerplatine installieren](https://wohnmobil-display.github.io/Wohnmobil-Display/#steuerplatine)** |

![Welche Buchse wofür – Display-Rückseite und H2-Board](bilder/buchsen_display_h2.svg)

![Display und Steuerplatine verbinden](bilder/anschluss_display_h2_usb.svg)

> **Wichtig – Jumper J5 am H2-Board:** Die kleine Steckbrücke (Jumper) muss auf den beiden Stiften **J5** stecken.
> Ohne sie bekommt der Chip keinen Strom – er wird am Computer nicht erkannt und läuft auch auf der Steuerplatine nicht.
> Liegt der Jumper lose in der Packung, einfach aufstecken.

**So geht's (für beide Geräte gleich):**
1. Link oben anklicken – die Installer-Seite öffnet sich beim passenden Knopf.
2. Gerät per USB anschließen und auf **Display installieren** bzw. **Steuerplatine installieren** klicken.
3. Im Fenster den Eintrag des Geräts wählen (z. B. „USB JTAG/serial debug unit“ oder „USB Single Serial“) und auf **Verbinden** klicken.
4. Installation bestätigen und warten, bis sie fertig ist. Kabel nicht abziehen, Browser nicht schließen.
5. Das Gerät startet danach von selbst neu. Falls nicht: kurz vom Strom trennen und wieder anschließen.

Die Steuerplatine muss nur **ein einziges Mal** so installiert werden. Spätere Updates spielt das Display
selbst über das USB-Kabel auf (siehe [Updates](#4-updates)).

> Wird kein Gerät angezeigt, probiere ein anderes Kabel oder einen anderen USB-Anschluss.
> Stecke das Gerät kurz ab und wieder an und wähle dann den neu erschienenen Eintrag.

## 2. Erster Start

Beim ersten Start zeigt das Display den Bildschirm **Freischaltung** mit zwei Werten:

- **Chip-ID**, z. B. `AA:BB:CC:DD:EE:FF`
- **Freigabecode**, z. B. `1234`

Darunter steht die fertige Zeile zum Freischalten, z. B.:

```
AA:BB:CC:DD:EE:FF 1234
```

Ohne Freischaltcode zeigt das Display nur diesen Freischalt-Bildschirm. Die Zeile notierst du dir und gibst sie beim Bezahlen an (siehe unten).

## 3. Freischalten

> **Ein privates Hobbyprojekt ohne Gewinnabsicht.** Das Wohnmobil-Display ist aus Freude am Basteln entstanden, in
> unzähligen Abenden und Wochenenden, für mein eigenes Wohnmobil – und weil ich es auch anderen Wohnmobilisten
> ermöglichen möchte. Es steckt viel Arbeit darin: Firmware, Platinen, Gehäuse, Anleitung und die laufende Pflege.
> Der Freischaltcode wird gegen einen **einmaligen Kostenbeitrag** abgegeben. Er hilft, Entwicklungsmaterial,
> Platinen-Prototypen, Server und Updates zu finanzieren – mir geht es nicht um Gewinn. Wenn dir das Projekt
> gefällt, freue ich mich über deinen Beitrag. Danke!

Für die dauerhafte Nutzung ist ein persönlicher, 6-stelliger **Freischaltcode** nötig. Du bekommst ihn gegen einen
einmaligen **Kostenbeitrag von 29 €** – er gilt für immer, auch nach Neustarts und Updates.

1. Öffne den PayPal-Link: **[paypal.com/ncp/payment/MHXFBPU9TVV2L](https://www.paypal.com/ncp/payment/MHXFBPU9TVV2L)**
2. Trage im Feld **„Chip-ID + Freigabecode“** die Zeile vom Display ein – genau so, wie sie dort steht:
   `AA:BB:CC:DD:EE:FF 1234`
3. Nach Eingang der Zahlung bekommst du den Freischaltcode per E-Mail, in der Regel **innerhalb von 24 Stunden**.
4. Gib den Code am Display ein und bestätige mit **OK**. Fertig – das Display ist dauerhaft freigeschaltet.

Bei einem freigeschalteten Display erreichst du die Seite jederzeit über **Setup → Allgemein → Freischaltung**.

> Feld beim Bezahlen vergessen? Schick die Zeile einfach an **wohnmobil.display@gmail.com**.
>
> Nach jeder dritten falschen Eingabe wird die Eingabe für einige Stunden gesperrt – den Code bitte genau übernehmen.

## 4. Updates

Freigeschaltete Displays holen neue Versionen selbst über WLAN – **für das Display und für die Steuerplatine**:
**Setup → Allgemein → Update → Installieren.**
Die Steuerplatine wird dabei über das USB-Kabel vom Display aus aktualisiert – nichts muss ausgebaut werden.
Deine Einstellungen bleiben dabei erhalten. Startet eine neue Version einmal nicht richtig,
kehrt das Display automatisch zur vorherigen Version zurück.

Was sich geändert hat, steht bei den [Versionen (Releases)](https://github.com/Wohnmobil-Display/Wohnmobil-Display/releases).

## Hilfe bei Verbindungsproblemen

- Nur Chrome oder Edge verwenden.
- Ein anderes USB-Kabel und einen anderen USB-Anschluss probieren.
- Alle Programme schließen, die den USB-Anschluss benutzen könnten.
- Display kurz abziehen und wieder anschließen, Installer-Seite neu laden.

## Manuelle Installation

Falls die Installer-Seite nicht funktioniert: Unter [Releases](https://github.com/Wohnmobil-Display/Wohnmobil-Display/releases)
liegen zwei Dateien, die mit einem eigenen Flash-Programm jeweils an **Adresse 0x0** geschrieben werden:
- `Wohnmobil-Display-FULL.bin` → Display
- `Steuerplatine-H2-FULL.bin` → Steuerplatine (ESP32-H2, Buchse „USB“)

Die Dateien ohne „FULL“ sind nur für Updates gedacht.

## Hinweis, Haftung und Eigenverantwortung

**Das Wohnmobil-Display ist ein privates Hobbyprojekt ohne Firma dahinter und ohne Gewinnabsicht.** Es steht in keiner
Verbindung zu Schaudt, Waveshare, Victron, Mopeka oder anderen Herstellern der unterstützten Geräte.

- **Selbstbau und Einbau auf eigene Verantwortung:** Wer die Platinen fertigen lässt, das Display installiert oder in
  sein Fahrzeug einbaut, tut das auf eigene Gefahr und ist selbst für die fachgerechte Ausführung verantwortlich
  (Absicherung, Verkabelung, Funktion, Versicherungs- und Zulassungsfragen).
- **Arbeiten an der Fahrzeugelektrik** nur mit entsprechenden Kenntnissen: vorher Sicherung ziehen bzw. das Bordnetz
  stromlos schalten, Landstrom trennen. Im Zweifel eine Fachwerkstatt fragen.
- **Keine Sicherheitseinrichtung:** Alarmanlage, Rauch-/Gaswarnung, Sirene, Pumpensperre und Füllstandsanzeigen sind
  ein Komfort für Bastler und **kein Ersatz** für geprüfte und zugelassene Geräte (z. B. Rauchmelder nach EN 14604,
  Gaswarner nach EN 50291).
- **Keine Garantie, kein Support-Anspruch:** Hardware, Firmware und Anleitung werden „wie besehen“ und ohne
  Gewähr für Funktion, Verfügbarkeit oder Fehlerfreiheit bereitgestellt.
- **Haftung:** Soweit gesetzlich zulässig ist meine Haftung ausgeschlossen. Gesetzlich zwingende Haftung (insbesondere
  bei Vorsatz, grober Fahrlässigkeit sowie bei Verletzung von Leben, Körper oder Gesundheit) bleibt unberührt.

Kontakt: **wohnmobil.display@gmail.com**
