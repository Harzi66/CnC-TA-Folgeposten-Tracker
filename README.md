# CnC-TA Folgeposten Tracker

Ein kleines Tampermonkey-Userscript für **Command & Conquer: Tiberium Alliances**, das neu erscheinende Folge Lager und Vorposten automatisch erkennt und übersichtlich auf der Weltkarte markiert.

Der Tracker zeigt die **10 neuesten Folgeposten** rund um die Hauptbasis an und informiert zusätzlich direkt im Spielchat, sobald ein neuer Folgeposten erkannt wurde.

---

## ✨ Funktionen

- 🗺️ Anzeige der **10 neuesten Folge Lager und Vorposten**
- 🔢 Nummerierung der Marker von **1–10**
- 🆕 Automatische Erkennung neu erschienener Folgeposten
- 💬 Chatmeldung bei einem neuen Folgeposten
- 📍 Koordinaten in der Chatmeldung sind **direkt anklickbar**
- 📊 Anzeige der **Levelhöhe**
- 🟡 Lager werden beim Level **gelb** hervorgehoben
- 🟢 Vorposten werden beim Level **grün** hervorgehoben
- 🎯 Berücksichtigt nur Folgeposten innerhalb der maximalen Angriffsdistanz
- ⚔️ Berücksichtigt Folgeposten bis maximal **eine Stufe unterhalb der Offensivstufe der Hauptbasis**
- 🔄 Prüfung auf neue Folgeposten etwa alle **2,5 Sekunden**
- 🖥️ Marker bleiben beim Verschieben und Zoomen der Weltkarte korrekt positioniert

---

## 🗺️ Weltkarten-Anzeige

Die neuesten Folgeposten werden direkt auf der Weltkarte mit nummerierten Markern dargestellt.

**1 = neuester Folgeposten**

**10 = zehnter Eintrag der aktuellen Liste**

![Weltkarten-Anzeige](Screenshot_1.png)

---

## 💬 Chat-Benachrichtigung

Wird ein neuer Folgeposten erkannt, erscheint automatisch eine Meldung im Systemchat.

Beispiele:

> Neues Lager bei 438:523 Level 39.56

> Neuer Vorposten bei 440:526 Level 41.20

Die Koordinaten können direkt angeklickt werden und zentrieren die Weltkarte automatisch auf den entsprechenden Standort.

Die Levelhöhe wird zur besseren Übersicht farblich hervorgehoben:

- 🟡 **Gelb = Lager**
- 🟢 **Grün = Vorposten**

![Chat-Benachrichtigung](Screenshot_2.png)

---

## 🔎 Welche Folgeposten werden angezeigt?

Der Tracker orientiert sich an der Hauptbasis des Spielers.

Dabei wird automatisch die eigene Stadt mit der höchsten Offensivstufe als Hauptbasis verwendet.

Anschließend werden Folgeposten innerhalb der maximalen Angriffsdistanz gesucht.

Standardmäßig werden Folgeposten berücksichtigt, deren Level höchstens **eine Stufe unter der Offensivstufe der Hauptbasis** liegt.

Beispiel:

| Hauptbasis | Angezeigte Folgeposten |
|---|---|
| Offensivstufe 40 | Level 39–40+ |
| Offensivstufe 50 | Level 49–50+ |
| Offensivstufe 60 | Level 59–60+ |

---

## 🆕 Erkennung neuer Folgeposten

Die Folgeposten werden anhand ihrer ID nach Aktualität sortiert.

Der höchste Wert wird dabei als der neueste Folgeposten behandelt.

Beim ersten Laden des Scripts wird der aktuell neueste Folgeposten einmal im Chat angezeigt.

Danach erfolgt eine Chatmeldung nur noch dann, wenn tatsächlich ein neuer Folgeposten erkannt wurde.

Dadurch wird der Chat nicht bei jeder Aktualisierung mit Meldungen gefüllt.

---

## ⚙️ Aktualisierung

Der Tracker prüft ungefähr alle **2,5 Sekunden**, ob sich bei den Folgeposten etwas geändert hat.

Die Position der vorhandenen Kartenmarker wird zusätzlich wesentlich häufiger aktualisiert, damit sie beim Bewegen und Zoomen der Weltkarte sauber an ihrer Position bleiben.

---

## 🛠️ Installation

### Voraussetzungen

Du benötigst einen Browser mit einem Userscript-Manager, zum Beispiel:

- Tampermonkey
- Violentmonkey

### Installation mit Tampermonkey

1. Tampermonkey im Browser installieren.
2. Die Userscript-Datei aus diesem Repository öffnen.
3. Das Script in Tampermonkey installieren.
4. Eine C&C-Tiberium-Alliances-Welt öffnen bzw. neu laden.
5. Der Tracker startet automatisch.

---

## 📁 Dateien

| Datei | Beschreibung |
|---|---|
| `CnC-TA _Folgeposten_Tracker.user.js` | Hauptscript |
| `Screenshot_1.png` | Beispiel der Weltkarten-Anzeige |
| `Screenshot_2.png` | Beispiel der Chat-Benachrichtigung |
| `README.md` | Dokumentation |

---

## ❤️ Hintergrund

Dieses Script basiert auf Erkenntnissen und Teilen der ursprünglichen CampTracker-Funktion aus:

**Shockr – Tiberium Alliances Tools**

Originalautor:

**leo7044**

Das Script wurde für den eigenständigen Einsatz als kleiner, spezialisierter **Folgeposten Tracker** angepasst und weiterentwickelt.

Der ursprüngliche Code und das Projekt sind hier zu finden:

https://github.com/leo7044/CnC_TA

---

## 👨‍💻 Autor

**Harzi**

Anpassung und Weiterentwicklung für C&C Tiberium Alliances.

---

## 📜 Hinweis

Dieses Userscript ist ein Community-Projekt für **Command & Conquer: Tiberium Alliances**.

Die Nutzung erfolgt auf eigene Verantwortung.
