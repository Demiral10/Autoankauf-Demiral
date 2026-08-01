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

## Schriften

Inter und Inter Tight werden **lokal** ausgeliefert (`fonts/`, eingebunden über
`fonts.css`) – es besteht keine Verbindung zu Google Fonts. Das vermeidet die
Übermittlung der Besucher-IP an Google, die ohne Einwilligung datenschutzrechtlich
angreifbar ist (vgl. LG München I, Urteil vom 20.01.2022, 3 O 17493/20).

Es handelt sich um Variable Fonts mit der Gewichtsachse 100–900, je ein File pro
Familie und Subset (`latin`, `latin-ext`) – zusammen rund 262 KB. Beide Schriften
stehen unter der SIL Open Font License 1.1.

Sollen weitere Zeichensätze unterstützt werden (z. B. Kyrillisch oder Griechisch),
müssen die entsprechenden Subsets ergänzt werden.

## JavaScript-Bibliotheken

Ebenfalls lokal unter `js/` – kein CDN:

| Datei | Version | Zweck |
|---|---|---|
| `three.min.js` | r128 (0.128.0) | Partikel-Silhouette im Hero |
| `gsap.min.js` | 3.12.5 | Animationen |
| `ScrollTrigger.min.js` | 3.12.5 | Scroll-Reveals |

Alle drei werden mit `defer` geladen und blockieren das Rendering nicht.

**Beim Aktualisieren von three.js beachten:** Ab Version r150 gibt es kein
UMD-Bundle mehr, das ein globales `THREE` bereitstellt. Der Code in `index.html`
setzt genau das voraus. Ein Update auf eine neuere Version erfordert daher eine
Umstellung auf ES-Module.

## Datenübertragung an Dritte

Beim Aufruf der Seiten werden **keine** Daten an Dritte übertragen – alle Ressourcen
liegen im Repository. Die einzige externe Einbindung ist Google Maps, und die lädt
erst nach einem Klick auf die Schaltfläche im Kontaktbereich.

Wird das geändert (z. B. eine Bibliothek wieder per CDN eingebunden, Analytics
ergänzt oder der auskommentierte Formspree-Versand in `index.html` aktiviert),
muss die Datenschutzerklärung angepasst werden.

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
