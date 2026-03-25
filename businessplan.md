# Businessplan

## Monatliche Kosten

| Position | EUR/Monat | Anmerkung |
|---|---|---|
| Hardware-Amortisation | 7.640 | 275k über 3 Jahre |
| Colocation | 2.375 | Rack, Strom, Kühlung, Netz |
| Geschäftsführung | 4.000 | Teilzeit, Anfang |
| DevOps / Admin | 2.000 | Teilzeit oder Mitglied |
| Steuerberater | 500 | Monatliche Buchhaltung + Jahresabschluss |
| Büro / Coworking | 500 | |
| Prüfungsverband | 170 | Pflicht bei eG |
| Versicherung, Misc | 300 | |
| Monitoring, Security | 200 | |
| Rücklage | 500 | Reparaturen, Unvorhergesehenes |
| **Gesamt** | **~19.000** | |

## Mitgliedschaften

| Mitgliedschaft | Preis | Inhalt |
|---|---|---|
| **Basis** | 19 EUR/Monat | API-Zugang zu gehosteten Modellen, Fair Use (1M Tokens/Tag) |
| **Power** | 59 EUR/Monat | Höheres Kontingent, 405B-Modelle, Priorität |
| **Startup** | 199 EUR/Monat | Dedizierte GPU-Stunden, Fine-Tuning, SLA |

Zum Vergleich: ChatGPT Plus kostet 20 EUR/Monat — ohne DSGVO, ohne eigene Infrastruktur, ohne Mitbestimmung.

## Break-even-Szenario

| Einnahmequelle | Annahme | EUR/Monat |
|---|---|---|
| 500 Basis-Mitglieder | 500 x 19 EUR | 9.500 |
| 150 Power-Mitglieder | 150 x 59 EUR | 8.850 |
| GPU-Stunden (2 GPUs, 70% Auslastung) | ~1.000h x 2 EUR | 2.000 |
| **Gesamt** | | **20.350** |

**Break-even bei ~650 Mitgliedern.**

## Wachstums-Szenario (nach 12 Monaten)

| Einnahmequelle | Annahme | EUR/Monat |
|---|---|---|
| 800 Basis-Mitglieder | 800 x 19 EUR | 15.200 |
| 200 Power-Mitglieder | 200 x 59 EUR | 11.800 |
| 50 Startup-Mitglieder | 50 x 199 EUR | 9.950 |
| GPU-Stunden | ~1.500h x 2 EUR | 3.000 |
| **Gesamt** | | **39.950** |

Überschuss: ~21.000 EUR/Monat — zweiter Node nach 13 Monaten selbst finanziert.

## Startfinanzierung

| Position | EUR |
|---|---|
| Hardware (8x H100 Server) | 275.000 |
| Setup, Colo-Einrichtung | 15.000 |
| Gründungskosten (Notar, Prüfungsverband, Satzung) | 10.000 |
| Steuerberater (Gründung + erstes Jahr) | 8.000 |
| Büro / Coworking (12 Monate) | 6.000 |
| Betriebspuffer (9 Monate bis Break-even) | 90.000 |
| Marketing / Community-Aufbau | 10.000 |
| **Gesamt** | **~414.000** |

## Finanzierungsmix

| Quelle | EUR | Anmerkung |
|---|---|---|
| Gründungsmitglieder (100 x 2.000 EUR) | 200.000 | Genossenschaftsanteil |
| GLS Bank / KfW Kredit | 150.000 | Zinsgünstig für eG |
| Fördermittel | 64.000 | Sovereign Tech Fund, BMWK, Land |
| **Gesamt** | **414.000** |

Der Gründungsanteil von 2.000 EUR ist vergleichbar mit Energiegenossenschaften (üblich: 500–5.000 EUR).

## Risiken

**Kriegen wir 650 Mitglieder in 9 Monaten?**

Dafür spricht:

- Der Markt ist da — jedes KI-nutzende Unternehmen in Deutschland hat das DSGVO-Problem
- 19 EUR/Monat ist unter ChatGPT Plus
- Die Story ist stark und zeitgemäß
- Energiegenossenschaften zeigen: Das Modell funktioniert

Dagegen spricht:

- Genossenschaft ist für manche Techies ungewohnt
- Open-Source-Modelle sind noch nicht auf GPT-4o-Level (aber der Abstand schrumpft schnell)
- 650 zahlende Mitglieder in 9 Monaten ist ambitioniert

## Skalierung: Wann GPU-Stunden konkurrenzfähig werden

Mit einem Node können wir im reinen GPU-Stunden-Modell nicht mit spezialisierten Anbietern konkurrieren:

| Anbieter | H100 EUR/GPU/Stunde |
|---|---|
| CoreWeave | 1,90–2,10 |
| Lambda Labs | 2,30–2,80 |
| AWS / GCP / Azure | 3,50–4,50 |
| **Wir (1 Node)** | **4,07** |

Der Grund: Fixkosten (GF, Büro, Verwaltung) verteilen sich auf nur 8 GPUs. Das ändert sich mit Skalierung:

| Nodes | GPUs | Fixkosten/Monat | Kosten/GPU-Stunde (80%) |
|---|---|---|---|
| 1 | 8 | 19.000 | 4,07 |
| 3 | 24 | 34.000 | 2,43 |
| 5 | 40 | 47.000 | 2,01 |
| 10 | 80 | 75.000 | 1,60 |

Jeder weitere Node kostet nur ~15.000 EUR/Monat (Hardware + Strom). Die Verwaltungskosten wachsen kaum. Ab 3 Nodes sind wir auf Lambda-Niveau, ab 5 schlagen wir sie.

### Strategie daraus

**Phase 1 (1 Node):** Mitgliedschaften tragen die Fixkosten. GPU-Stunden als Zusatz, nicht Hauptgeschäft. Startups kommen wegen DSGVO + Vertrauen, nicht wegen Preis.

**Phase 2 (3+ Nodes):** GPU-Stunden werden konkurrenzfähig (~2,40 EUR). Aktiver Vertrieb an Startups und Mittelstand.

**Phase 3 (Föderation, 10+ Nodes):** Mehrere lokale Genossenschaften, gemeinsame Verwaltung. Grenzkosten unter 2,00 EUR/GPU-Stunde. Echte Alternative zu den US-Anbietern.

## Zeitleiste

| Monat | Meilenstein |
|---|---|
| 0–3 | Gründungsteam, Satzung, Prüfungsverband |
| 3–6 | Gründung eG, Finanzierung gesichert |
| 6–9 | Hardware bestellt, Colo eingerichtet, Stack läuft |
| 9–12 | Erste Mitglieder, Community-Aufbau |
| 12–18 | Break-even, 650+ Mitglieder |
| 18–24 | Zweiter Node, Föderationsmodell starten |
