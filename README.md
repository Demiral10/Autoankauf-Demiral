# Autoankauf Demiral

Website für Automobile Demiral – Autoankauf in Essen und NRW (PKW, LKW, Transporter).

## Inhalt

- `index.html` – komplette Startseite (HTML, CSS und JavaScript in einer Datei, keine externen Abhängigkeiten)

## Lokal ansehen

Die Datei `index.html` einfach im Browser öffnen, oder einen lokalen Server starten:

```bash
python3 -m http.server 8000
# danach http://localhost:8000 aufrufen
```

## Veröffentlichen mit GitHub Pages

1. Im Repository auf **Settings → Pages** gehen
2. Unter *Build and deployment* als Source **Deploy from a branch** wählen
3. Branch auf `main` (Ordner `/root`) setzen und speichern

## Rechtstexte

- `impressum.html` – Anbieterkennzeichnung nach § 5 DDG
- `datenschutz.html` – Datenschutzerklärung nach Art. 13 DSGVO

Die Datenschutzerklärung beschreibt den tatsächlichen Stand der Seite: keine Cookies,
kein Tracking, Formularversand nur über WhatsApp-Link oder `mailto`, Fotos bleiben lokal,
Google Maps lädt erst nach Klick. Wird an der Seite etwas davon geändert, muss der Text
mitgezogen werden.

## Link-Vorschaubild

`og-image.png` (1200 × 630) wird von `og:image` und `twitter:image` referenziert und
erscheint, wenn der Link per WhatsApp, Facebook oder E-Mail geteilt wird.

## Noch offen

Die Startseite verlinkt auf sechs Stadt-Seiten, die noch nicht im Repository liegen:

- `autoankauf-essen.html`, `autoankauf-bochum.html`, `autoankauf-bottrop.html`,
  `autoankauf-duisburg.html`, `autoankauf-gelsenkirchen.html`, `autoankauf-oberhausen.html`

Ebenfalls referenziert, aber noch nicht vorhanden: `sitemap.xml`, `robots.txt`.

## Domain

Die Seite ist auf `https://www.autoankauf-demiral.de` ausgelegt – Canonical-Tag,
Open-Graph-URLs und strukturierte Daten verweisen bereits auf diese Domain.
