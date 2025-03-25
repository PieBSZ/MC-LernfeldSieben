<!--
author: Benjamin Pietke
email: pietke@bszbautzen.de
comment: Lernfeld 7 - Mechatronik: Dieser Online-Kurs dient zur Unterstützung im Lernfeld-Unterricht am BSZ Bautzen.
logo: ./bilder/logo-lf7.png
icon: ./bilder/icon-bsz.png
classroom: enable
-->

# Mechatronische Teilsysteme

## Einführung

## Sensorik

## Baugruppen eines Netzteils

### Transformator

### Gleichrichter

#### Halbleiterbauelemente

### Glättung

### Stabilisierung

## Steuer- und Regelungstechnik

Herzlich willkommen im Abschnitt zu Regelungstechnik! 🎓

In der Ausbildung zum Mechatroniker ist dieses Thema unerlässlich, da es euch grundlegende Prinzipien zur Steuerung und Regelung komplexer Systeme vermittelt.

Ihr lernt, wie Systeme automatisch reguliert werden, um Istwerte und Sollwerte richtig abzustimmen. 📏 Dabei spielt die Erfassung von Daten durch Sensoren und die Verarbeitung dieser Informationen zur Anpassung von Steuerungen eine zentrale Rolle. 🎛️

Ein wichtiger Aspekt ist das Verständnis von Regelkreisen und deren Komponenten. Ihr erfahrt, wie diese in verschiedenen Anwendungen, wie Industrieanlagen und Automatisierungssystemen, eingesetzt werden. 🔧 Zudem werdet ihr praktische Übungen durchführen, um euer theoretisches Wissen anzuwenden und zu vertiefen. 💻🔍

Die Kenntnisse in der Regelungstechnik sind entscheidend für eure berufliche Entwicklung und für die Effizienz moderner technischer Systeme. 🌍 Seid bereit, spannende Themen zu erkunden und euer Wissen zu erweitern! Viel Spaß beim Lernen! 📚✨

![GIVE ME CONTROL!](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExOW96dnl1b2g4b2RvZHF0anhuaTVoZmdkOTk3dG1sanpwajdhMnRxMyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/YO3icZKE2G8OoGHWC9/giphy.gif "viaGIPHY")

### Steuern vs. Regeln

Für ein erstes Verständnis zum Thema Regelungstechnik ist es wichtig, den technischen Unterschied zwischen "steuern" und "regeln" zu verinnerlichen.

![Steuern vs. Regeln](bilder/steuern-regeln.png)

Lesen Sie die beiden Definition nach DIN IEC 60050-351:

**Steuerung**

*"Das Steuern, die Steuerung, ist ein Vorgang in einem System, bei dem eine oder mehrere Größen als Eingangsgrößen, andere Größen als Ausgangs- bzw. Steuergrößen aufgrund der dem System eigentümlichen Gesetzmäßigkeiten beeinflussen.*

*Kennzeichen für das Steuern ist entweder der offene Wirkungsweg oder ein zeitweise geschlossener Wirkungsweg, bei dem die durch die Eingangsgrößen beeinflussten Ausgangsgrößen nicht fortlaufend und nicht wieder über dieselben Eingangsgrößen auf sich selbst wirken."*

**Regelung**

*"Die Regelung bzw. das Regeln ist ein Vorgang, bei dem fortlaufend eine Größe, die Regelgröße, erfasst, mit einer anderen Größe, der Führungsgröße, verglichen und im Sinne einer Angleichung an die Führungsgröße beeinflusst wird.*

*Kennzeichen für das Regeln ist der geschlossene Wirkungsablauf, bei dem die Regelgröße im Wirkungsweg des Regelkreises fortlaufend sich selbst beeinflusst."*

**📝 AUFGABE**

Erläutern Sie anhand der folgenden Beispiele den Unterschied zwischen "Steuern" und "Regeln":

- Geschwindigkeit eines Autos
- Navigation per Maps
- Backofen in der Küche

**📝 AUFGABE**

Grenzen Sie die Begriffe "Steuerung" und "Regelung" mit Ihren eigenen Worten gegeneinander ab.

### Blockschaltbild

Eine Regelung wird meist schematisch als **Blockschaltbild** anhand der Struktur eines **Regelkreises** dargestellt.

**📝 AUFGABE**

Übernehmen Sie das Blockschaltbild und ergänzen Sie die Begriffe für die einzelnen Elemente. Nutzen Sie die Informationen in Ihrem Tabellenbuch!

![Schema Regelkreis](bilder/schema-regelkreis.png)

``` ascii
+------------+   +---------+   +--------+
|            |   |         |   |        |
| Leerer     +-->| Platz-  +-->| halter |
|            |   |         |   |        |
+------------+   +---------+   +--------+
```

Ergänzen Sie die Bedeutung der verschiedenen Kenngrößen eines Regelkreises und tragen Sie diese an der passenden Stelle im Blockschaltbild ein.

| Kenngröße | Bedeutung        |
|-----------|------------------|
| x         |  |
| w         |  |
| e         |  |
| z         |  |
| y         |  |
| r         |  |

**✅ KONTROLLE**

Lösen Sie die LearningApp [Blockschaltbild Regelkreis](https://learningapps.org/watch?v=ptu8z0cwa19).
[qr-code](https://learningapps.org/watch?v=ptu8z0cwa19)

### Regelungsarten

Der Vergleicher vergleicht die zwei am Reglereingang anstehenden Signale. Das sind die Rückführgröße **r** (die zu regelnde Größe) und die Führungsgröße **w** (Sollwert). Je nach Art der Führungsgröße w wird in der Regelungstechnik eine Regelung in drei verschiedene Arten eingeteilt.

1. **Festwertregelung**: Unter Festwertregelung versteht man eine Regelungsart, bei der der Sollwert w einer Regelung konstant gehalten werden soll.

2. **Folgeregelung**: Unter Folgeregelung versteht man eine Regelung, bei der der Sollwert w einer veränderlichen Führungsgröße folgt.

3. **Zeitplanregelung**: Bei einer Zeitplanregelung wird der Sollwert w von einer Zeitschaltuhr oder von einem Programm geändert.

**📝 AUFGABE**

Ordnen Sie die Beispiele einer Regelungsart zu und begründen Sie Ihre Entscheidung.

- Geschwindigkeitsregelung von PKWs
- Temperaturregelung in Wohngebäuden
- Positionsregelung des Maschinenschlittens einer Drehmaschine
- Abstandsregelung eines Laserschneidwerkzeugs
- Druckregelung in einem Kompressor

Finden Sie je zwei weitere Praxisbeispiele pro Regelungsart.


### Wichtige Begriffe und Elemente eines Regelkreises

#### Regelstrecke

In einem Regelkreis wird die zu regelnde Anlage als *Regelstrecke* bezeichnet. Sie liegt zwischen dem Stellglied und dem Messglied.

Bei **Regelstrecken mit Ausgleich** nimmt die Ausgangsgröße x der Strecke nach einer Veränderung der Eingangsgröße y innerhalb einer bestimmten Zeit wieder einen neuen *Beharrungszustand* ein. Diese Strecken werden als **P-Strecken** (Proportional-Strecken) bezeichnet.

![Messie Wohnzimmer](bilder/messie.png "Bildrechte:https://www.kreisbote.de/lokales/schongau/muell-soweit-auge-reicht-7379971.html")

**Click for more garbage** --> [Messie richtet Chaos in Peitinger Wohnung an](https://www.kreisbote.de/lokales/schongau/messie-verwuestet-peitinger-wohnung-voellig-mehrere-faelle-jaehrlich-7379977.html)

#### Stellsprung und Sprungantwort

Wird am Eingang der Strecke die Stellgröße y sehr schnell um einen bestimmten Wert $ \Delta $ y oder um den ganzen Stellbereich Y verändert (*Stellsprung*), so kann sich der neue Wert der Strecke (*Sprungantwort*) sofort oder nach einer bestimmten Zeit einstellen.

#### Zeitverhalten und Ordnungszahl

Von entscheidender Bedeutung für die Charakterisierung einer Regelstrecke ist ihr *Zeitverhalten*, das heißt der Verlauf der Regelgröße x über der Zeit t bei Änderung der Stellgröße y. Man unterscheidet zwischen verzögerungsfreien Strecken und Strecken mit Anlaufzeit.

Üblicherweise sind in Regelstrecken Verzögerungsglieder (Energiespeicher) enthalten, die den Prozess der Regelung beeinflussen.

Eine verzögerungsfreie Strecke (*Strecke 0. Ordnung* oder *$ PT_0 $-Strecke*) besitzt keine Energiespeicher und reagiert unmittelbar auf eine Änderung der Führungsgröße.

Folgt die Regelgröße x einer Stellgrößenänderung y nur verzögert, so handelt es sich um eine Strecke mit Anlaufzeit. Befindet sich nur ein Energiespeicher in dieser Strecke, so spricht man von einer *Strecke 1. Ordnung* oder *$ PT_1 $-Strecke*. Strecken mit mehreren Energiespeichern werden als *Strecke n. Ordnung* oder *$ PT_n $-Strecke* zusammengefasst.

**📝 AUFGABE**

In der Regelungstechnik wird für eine bessere Übersichtlichkeit das Verhalten der Strecke bei einem Stellsprung (oder einer Störung) als Blockschaltbild angegeben.

Zeichnen Sie für die genannten Strecken ($ PT_0 $, $ PT_0-T_t $, $ PT_1 $, $ PT_1-T_t $, $ PT_n $) das zugehörige Blockschaltbild. Für Infos zur *Totzeit $ T_t $* lesen Sie zunächst den nächsten Abschnitt.

Geben Sie für jede Strecke zwei Beispiele an.

#### Totzeit

Unter der Totzeit $ T_t $ einer Regelstrecke versteht man die Zeit, die vergeht, bis sich eine Änderung der Stellgröße beginnt am Messort auszuwirken. Umso größer die Totzeit ist, desto schwieriger ist die Regelbarkeit einer Strecke.

**📝 AUFGABE**

Geben Sie Hinweise, die beim Entwurf eines Regelkreises beachtet werden müssen, damit die Totzeit möglichst klein ist.

#### Übergangsfunktion eines Regelkreises

![Übergangsfunktion](bilder/kennwerte-uebergangsfunktion.png "Bildrechte: https://upload.wikimedia.org/wikipedia/commons/b/b4/Kennwerte_%C3%9Cbergangsfunktion.png")





### Verhalten einer *guten* Regelung

**📝 AUFGABE**

Betrachten wir nochmal das Beispiel vom Abschnitt **Steuern vs. Regeln**. Nennen Sie verschiedene Kriterien, die Sie zur Beurteilung einer *guten* Regelung bewerten würden:

- Geschwindigkeit eines Autos
- Navigation per Maps
- Backofen in der Küche

