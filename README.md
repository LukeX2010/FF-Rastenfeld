# 🔥 FF Rastenfeld – Website

Blazor WebAssembly Website der Freiwilligen Feuerwehr Rastenfeld (NÖ).
Struktur angelehnt an **ffwaidhofen.at** – verbessert und modernisiert.

## Start

```bash
dotnet restore
dotnet run
# → https://localhost:5001
```

## Struktur

```
Pages/
  Index.razor              Startseite (Feed + Sidebar + Hero)
  Galerie.razor            Bildergalerie mit Lightbox
  Kontakt.razor            Kontaktformular
  Impressum.razor
  Datenschutz.razor
  Einsaetze/
    Einsaetze.razor        Einsatzliste mit Filterbar
    EinsatzDetail.razor    /einsaetze/{slug}
  News/
    News.razor             FF-News Übersicht
    NewsDetail.razor       /news/{slug}
    Ausbildung.razor
    AusbildungDetail.razor
    Feuerwehrjugend.razor
    FeuerwehrjugendDetail.razor
  Feuerwehr/
    Chronik.razor          Geschichte seit 1876
    Organisation.razor     Kommando + Mitgliederliste
    Feuerwehrhaus.razor    Infos zum Standort
  Fahrzeuge/
    Fahrzeuge.razor        Fahrzeugliste
    FahrzeugDetail.razor   /fahrzeuge/{id}

Components/
  NavMenu.razor     Header + Dropdown-Nav + Hamburger
  SiteFooter.razor  Footer
  Sidebar.razor     Wiederverwendbare Sidebar
  PostCard.razor    Beitragskarte (Einsatz/News/etc.)
  PageHero.razor    Seitenheader mit Breadcrumb

Services/DataService.cs   Alle Mock-Daten
Models/Models.cs          C# Datenmodelle
wwwroot/css/app.css       Komplettes Stylesheet
wwwroot/js/app.js         Scroll, Navbar, Loader
```

## Design-Konzept

| | ffwaidhofen.at | FF Rastenfeld |
|---|---|---|
| Layout | Feed + Sidebar | ✅ identisch |
| Nav | Dropdown-Menü | ✅ + Mobile Hamburger |
| Startseite | Direkt Blog-Feed | ✅ + verbesserter Hero |
| Beitragstypen | Einsätze/News/Ausbildung/Jugend | ✅ alle mit Detail-Routing |
| Fahrzeuge | Einzelseiten | ✅ /fahrzeuge/{id} |
| Sidebar | Suche, Kategorien, Links | ✅ als eigene Komponente |

## Kontaktdaten (real)

- Adresse: Rastenfeld 178, 3532 Rastenfeld, NÖ
- E-Mail: rastenfeld@feuerwehr.gv.at
- Notruf: 122
