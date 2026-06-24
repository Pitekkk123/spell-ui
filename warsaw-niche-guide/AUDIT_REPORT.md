# 🔎 AUDIT REPORT — WARSZAWA NICHE GUIDE : by Bilu

**Data audytu:** 2026-06-24T14:44:21.684Z  ·  **Miasto:** Warszawa, Polska  ·  **Próg modułu:** 5 obiektów

Raport bramki QA (subagent **S7**) dla mapy wygenerowanej topologią A0–A19 + S1–S7.

## 1. Podsumowanie

| Metryka | Wartość |
|---|---|
| Obiekty łącznie | **92** |
| Z modułów badawczych (agenci) | 91 |
| Anchor kuratorski (backfill) | 1 |
| Z oceną Google | 49 (53%) |
| Bez oceny → flaga MISSING | 43 (47%) |
| Ze ≥2 źródłami | 91 (99%) |
| Z 1 źródłem (flaga JEDNO_ZRODLO) | 1 (1%) |
| Bez źródła (UNVERIFIED) | 0 (0%) |
| Realne zdjęcie ładowane w runtime (Wikipedia, landmarki) | 26 |
| Miniatura satelitarna ESRI (gwarantowany fallback) | 92 (wszystkie) |
| **KILL** (geo poza bbox / brak istnienia) | 1 |
| Odrzucone przez audytorów modułowych | 1 |

## 2. Bramka SHIP

Reguła §7: jeśli **>5%** obiektów ma status UNVERIFIED (0 źródeł) → zwrot do A0.

- UNVERIFIED: **0/92 = 0.0%**
- Wynik bramki: ✅ **PASS — publikacja**

## 3. Moduły (18 — stały slot/kolor/ikona §4)

| # | Moduł | Slot | Obiekty | Agenci | Anchor | Status |
|---|---|---|---|---|---|---|
| 1 | 🍜 Restauracje | `restaurant` | **6** | 6 | 0 | ✅ OK |
| 2 | 👨‍🍳 Warsztaty | `workshop` | **5** | 5 | 0 | ✅ OK |
| 3 | 🎰 Hazard & Adrenalina | `hazard` | **5** | 5 | 0 | ✅ OK |
| 4 | 📷 Street Photo | `street` | **5** | 5 | 0 | ✅ OK |
| 5 | 🏛 Architektura | `architecture` | **6** | 6 | 0 | ✅ OK |
| 6 | ✂️ Niszowe | `niche` | **5** | 5 | 0 | ✅ OK |
| 7 | ♠️ Adult / Sztuka | `adult` | **4** | 4 | 0 | ⚠️ UNDERFILLED |
| 8 | 🌿 Parki & Natura | `parks` | **5** | 5 | 0 | ✅ OK |
| 9 | ☕ Kawa Specialty | `coffee` | **6** | 6 | 0 | ✅ OK |
| 10 | 🔪 Noże & Stal | `knives` | **5** | 5 | 0 | ✅ OK |
| 11 | 🚲 Rowery Custom | `cycling` | **6** | 6 | 0 | ✅ OK |
| 12 | 🎵 Winyle | `vinyl` | **5** | 6 | 0 | ✅ OK |
| 13 | ⌚ Zegarki | `watches` | **4** | 5 | 0 | ⚠️ UNDERFILLED |
| 14 | 📸 Aparaty Analog | `cameras` | **5** | 5 | 0 | ✅ OK |
| 15 | 💀 Urbex & Mrok | `urbex` | **5** | 4 | 1 | ✅ OK |
| 16 | 🔊 Hi-Fi & Jazz | `audio` | **5** | 5 | 0 | ✅ OK |
| 17 | 🕹️ Retro Arcade | `arcade` | **4** | 4 | 0 | ⚠️ UNDERFILLED |
| 18 | 🗼 Panoramy | `panorama` | **6** | 6 | 0 | ✅ OK |

### Moduły poniżej progu / bez desygnatu
- `adult` — 4 obiektów (UNDERFILLED). Warszawa konserwatywna; mało scen burleski/performance o profilu archiwalno-estetycznym.
- `watches` — 4 obiektów (UNDERFILLED). Ograniczona liczba zweryfikowanych desygnatów w Warszawie.
- `arcade` — 4 obiektów (UNDERFILLED). Ograniczona liczba zweryfikowanych desygnatów w Warszawie.

## 4. KILL-e (odrzucone obiekty)

| Obiekt | Slot | Powód |
|---|---|---|
| Spichlerz Twierdzy Modlin (ruiny Banku Polskiego) | `urbex` | geo poza bbox (52.4311,20.6598) |

### Odrzucone przez audytorów modułowych (faza VERIFY)

| Moduł | Obiekt | Powód |
|---|---|---|
| `street` | Hala Gwardii | Obiekt zamkniety i wchodzi w wieloletnia rewitalizacje - nie dziala jako opisany food-market. Hala gastronomiczna (zarzadzana wczesniej prze |

## 5. Obiekty z flagą MISSING (brak oceny)

- CookUp Studio Kulinarne (`workshop`)
- Sushi Akademia (`workshop`)
- Polish Your Cooking (`workshop`)
- Hala COS Torwar (`hazard`)
- Osiedle Za Żelazną Bramą (`street`)
- Pałac Kultury i Nauki (taras widokowy, 30. piętro) (`architecture`)
- ZODIAK Warszawski Pawilon Architektury (`architecture`)
- Pawilon Cepelii (dawny pawilon handlowy, ob. Empik Marszałkowska) (`architecture`)
- Plac Konstytucji (Marszałkowska Dzielnica Mieszkaniowa, MDM) (`architecture`)
- Dworzec Warszawa Centralna im. Stanisława Moniuszki (`architecture`)
- Biblioteka Uniwersytecka w Warszawie (BUW) i ogród na dachu (`architecture`)
- Muzeum Historii Medycyny Warszawskiego Uniwersytetu Medycznego (`niche`)
- Galeria Grafiki i Plakatu (`niche`)
- Muzeum Drukarstwa (oddział Muzeum Warszawy) (`niche`)
- Klub Komediowy (scena Rakieta) (`adult`)
- Rezerwat przyrody Las Kabacki im. Stefana Starzyńskiego (`parks`)
- Park Skaryszewski im. Ignacego Jana Paderewskiego (`parks`)
- Zespół pałacowo-parkowy w Natolinie (Park Natoliński, rezerwat Las Natoliński) (`parks`)
- Rezerwat przyrody Las Bielański (`parks`)
- Pracownia Kłosy (`knives`)
- Kuźnia Barona (`knives`)
- JapońskieNoże.pl (salon Corazziego) (`knives`)
- A-NÓŻ (`knives`)
- Ostry-Sklep (`knives`)
- True Love Cycles (`cycling`)
- MOKO Frameworks (`cycling`)
- GRUBANUTA.PL (`vinyl`)
- Wrzeciono Czasu (`watches`)
- Syncret Jewellery / Jubiler (Warszawa) (`watches`)
- FOTO XERO - pracownia fotograficzna i laboratorium analogowe (`cameras`)
- Fort IX Sadyba (Czerniaków) – Muzeum Polskiej Techniki Wojskowej (`urbex`)
- Muzeum X Pawilonu Cytadeli Warszawskiej (`urbex`)
- Schron przeciwatomowy Huty ArcelorMittal Warszawa (Stanowisko Dowodzenia Obrony Cywilnej) (`urbex`)
- Fort Bema (Fort P / Parysów) (`urbex`)
- B-SIDE (`audio`)
- Ministerstwo Dźwięku (`audio`)
- Interaktywne Muzeum "Tiger Score" (`arcade`)
- Warsaw Arcade Museum - Muzeum Gier Wideo (`arcade`)
- Kopiec Powstania Warszawskiego (Park Akcji "Burza") (`panorama`)
- Górka Szczęśliwicka – taras widokowy (`panorama`)
- Ogród na dachu Biblioteki Uniwersytetu Warszawskiego (BUW) (`panorama`)
- Kładka Magdaleny Abakanowicz (most pieszo-rowerowy na Wiśle) (`panorama`)
- Taras widokowy na skarpie przy Zamku Ujazdowskim (`panorama`)

## 6. Noty rzetelności (zero halucynacji §1)

- **Istnienie:** potwierdzane przez roj badawczy (web search + oficjalne strony) i audytorów modułowych; obiekty bez dowodu są usuwane, nie zmyślane. Współrzędne poza ramką miasta (`52.05–52.40, 20.80–21.30`) → KILL.
- **Oceny dzień/weekend:** Google nie publikuje ocen w podziale na dni — przełącznik Tydzień/Weekend różnicuje realnie **godziny otwarcia**, natomiast wartość gwiazdek to rzeczywista agregacja (jednakowa w obu trybach, chyba że źródło wskaże inaczej). Nie wprowadzono sztucznej pseudo-precyzji ocen.
- **Miniatury / zdjęcia:** każda pinezka ma natychmiast deterministyczny kafel satelitarny ESRI liczony z `la/lo` (gwarantowany, nigdy pusty). Dla 26 rozpoznawalnych landmarków front w tle dociąga realne zdjęcie z Wikipedii (`pageimages`, na maszynie użytkownika — build jest za egress-proxy blokującym Wikimedia) i podmienia kafel po załadowaniu; przy błędzie zostaje satelita. Przycisk „📸 Zdjęcia" otwiera **Google Grafikę** dla każdego miejsca (link, bez niestabilnego hotlinkowania — Google Images nie ma API miniatur).
- **Anchor kuratorski (`ANCHOR_KURATORSKI`):** 1 obiekt dodany z wiedzy kuratorskiej (backfill modułu urbex) dla pewnego pokrycia; oznaczony i opatrzony źródłem.
- **Linie metra:** zweryfikowane jako M1 czerwona / M2 zielona (WebSearch); dokładny hex wg standardowych wartości operatora (Wikipedia i mapa-metro zwracały 403 przez egress proxy).

---

## 7. Rozszerzenie hipsterskie — v2 (2026-06-24)

**Powód:** feedback — wersja v1 zawierała zbyt wiele miejsc mainstreamowych/turystycznych (np. taras PKiN, ogród Kopernika ~55 tys. opinii, Hala Bakalarska ~10,9 tys.), niezgodnych z założeniem „niszowe / poza szlakiem". v2 **dokłada** 50 miejsc hipstersko-lokalnych (nie usuwa v1) i kompresuje opisy.

### 7.1 Podsumowanie v2

| Metryka | Wartość |
|---|---|
| Obiekty łącznie | **142** (92 v1 + **50** nowych) |
| Nowe moduły | **7** (winebar, vintage, gallery, craft, club, bakery, concept) |
| Rozszerzone moduły v1 | 5 (coffee +5, vinyl +3, workshop +4, restaurant +4, niche +5) |
| Nowe obiekty ze ≥1 źródłem | **50/50 (100%)** |
| Nowe obiekty z oceną Google | 28/50 — pozostałe 22 → `rt=null` (zero zmyślonych ocen) |
| Współrzędne | wyprowadzone z potwierdzonych adresów ulicznych (geokodery zablokowane przez proxy 403); część `GEO_APPROX` |
| Kompresja opisów (92 v1) | 46 564 → 16 121 znaków (**−65%**); nowe 50 ~174 zn.; wszystkie ≤216 zn., ≤2 zdania |

### 7.2 Nowe moduły (7)

| Moduł | Slot | Obiekty | Przykłady |
|---|---|---|---|
| 🍷 Wino Naturalne | `winebar` | 4 | Rausz (Wilcza 27), Źródło (Targowa 81), Nowina (+ muzeum korkociągów) |
| 🧥 Vintage & Second-hand | `vintage` | 4 | Matrioszka, Nostalgia (koszulki piłkarskie), Kamizelka (Saska Kępa) |
| 🖼 Galerie Niezależne | `gallery` | 5 | Raster, lokal_30, Wschód, Propaganda, Piktogram (WGW) |
| 🍺 Craft Beer | `craft` | 4 | Cześć (Grzybowska 2), Same Krafty, Beer Station Praga |
| 🎧 Kluby & Rave | `club` | 4 | Chmury, Skład Butelek, Jasna 1, A.D.A. Puławska |
| 🥐 Piekarnie Rzemieślnicze | `bakery` | 4 | BAKEN, QUASĄ, DEJ, Aromat (Puławska) |
| 🪴 Concept & Design | `concept` | 4 | NAP (Mysia 3), Pan tu nie stał, Plant Concept, Locum |

### 7.3 Metoda i rzetelność (zero halucynacji)

- **12 agentów badawczych** (po kategorii) weryfikowało istnienie i bieżące działanie przez **WebSearch** z wieloźródłowym potwierdzeniem (oficjalne strony / IG / agregatory). `WebFetch` oraz geokodery (Nominatim/Photon) zwracały **403** (anti-bot serwisów + egress-proxy) — stąd współrzędne wyprowadzano z potwierdzonych adresów (poziom ulicy/budynku), wszystkie w ramce `52.05–52.40, 20.80–21.30`.
- **Twarda poprzeczka niszowości:** wykluczano miejsca turystyczno-mainstreamowe i z **>1500 opinii Google** (preferencja <800). Bez potwierdzenia źródłem — pomijano (nie zmyślano).
- **Odrzucone (przykłady, dla przejrzystości):**
  - *zamknięte:* Pogłos (XII 2024), Chmielarnia, Tarabuk, MiTo;
  - *zbyt mainstream (>1500 opinii):* Cuda na Kiju (3956), Arigator Ramen (6040), Mezze (4173), Jabeerwocky (2666), Kufle i Kapsle (2638);
  - *niepotwierdzone:* Kafarnaum, Fuel Cafe, Cudawa, Brand Books Café.
- **Nadmiar ponad limit 50 (4 obiekty, ważne — nie zniknęły przez błąd, lecz przez cap):** Winylowa, Blisko Bar, Bar Tung Anh, Szafa na Sztuki — zweryfikowane, ale odcięte przy domknięciu do 50 (najniższy wynik jakości: brak oceny / poza dzielnicami priorytetowymi).
- **Niezależny spot-check orkiestratora:** ręcznie potwierdzono przez WebSearch próbkę — Rausz (Wilcza 27, rausz.me), Nowina (Nowogrodzka 4 + muzeum korkociągów Cybulskich), Muzant (Warecka 4/6, antykwariat od 1989), Trzy Kruki (pl. Hallera 8, Good Coffee Micro Roasters) — wszystkie realne pod podanym adresem.

### 7.4 Bramka SHIP v2

- Nowe obiekty UNVERIFIED (0 źródeł): **0/50 = 0.0%** → ✅ **PASS**
- Uwaga jakości: współrzędne `GEO_APPROX` (poziom ulicy) — akceptowalne dla pinezek mapy; oceny brakujące jawnie `null`, bez pseudo-precyzji.
