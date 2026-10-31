# Luna branding (`luna-branding`)

> [Polski](README.pl.md) · [English](README.en.md) · [Deutsch](README.de.md)

Wspólne zasoby graficzne środowiska Luna: pastelowy zestaw ikon **Luna-Icons**,
logo trzech warstw projektu oraz tapety. Pakiet `luna-branding` instaluje je
w standardowych katalogach freedesktop, więc te same ikony widzi powłoka,
Ustawienia, Pliki i ekran logowania.

## Zawartość

| Ścieżka | Rola |
| --- | --- |
| `icons/Luna-Icons/` | motyw ikon freedesktop: 16–512 px PNG + SVG, kategorie apps/places/actions/devices/status/emblems/mimetypes/categories, `index.theme` |
| `branding/luna.svg` | ikona środowiska i sesji (półksiężyc) |
| `branding/libluna.svg` | logo toolkitu (pastelowe warstwy) |
| `branding/selene.svg` | logo kompozytora (nachodzące okna) |
| `branding/hicolor/` | wygenerowane PNG logo (16–512 px) dla programów bez SVG |
| `branding/luna.png` | 256 px do `/usr/share/pixmaps` |
| `wallpapers/luna-desktop.png` | domyślna tapeta Luny (także ekranu logowania) |
| `wallpapers/paganlinux.png` | tapeta dzienna PaganOS |
| `wallpapers/pagannoc.png` | tapeta nocna PaganOS |

## Instalacja

Pakiet `luna-branding` (PaganOS) instaluje:

```
/usr/share/icons/Luna-Icons/
/usr/share/icons/hicolor/scalable/apps/{luna,libluna,selene}.svg
/usr/share/icons/hicolor/<N>x<N>/apps/{luna,libluna,selene}.png
/usr/share/pixmaps/luna.png
/usr/share/wallpapers/luna/luna-desktop.png
/usr/share/wallpapers/paganlinux/{paganlinux,pagannoc}.png
```

Po instalacji warto odświeżyć cache ikon:

```sh
gtk-update-icon-cache -q -t -f /usr/share/icons/Luna-Icons
gtk-update-icon-cache -q -t -f /usr/share/icons/hicolor
```

## Zasady

- Wszystkie ikony są pastelowe i mają wspólną paletę (lawenda, błękit, mięta,
  żółty) — dzięki temu panel, Ustawienia i ekran logowania wyglądają spójnie.
- Zestaw nie zawiera reklam ani zdalnych zasobów; nic nie jest pobierane
  w runtime.
- Ikony aplikacji, które nie należą do środowiska, pochodzą z motywu
  `Luna-Icons` (nazwy freedesktop, np. `system-file-manager`).

Licencja: MPL-2.0.
