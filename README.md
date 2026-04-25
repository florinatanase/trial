# Manager Garanții Echipamente (MVP+)

Aplicație web simplă pentru urmărirea garanțiilor echipamentelor din casă, cu autentificare locală, notificări, export și sincronizare cloud opțională.

## Funcționalități
- **Autentificare locală** pe email + parolă (stocate local în browser).
- **Management garanții**: adăugare, listare, ștergere.
- **Calcul automat** dată expirare și status (activă / aproape expirată / expirată).
- **Notificări browser** (după acordul utilizatorului) pentru garanții cu <= 30 zile rămase.
- **Export CSV** pentru datele utilizatorului curent.
- **Export PDF** prin dialogul de print (`window.print`).
- **Sincronizare cloud opțională** via [JSONBin](https://jsonbin.io) (upload/download).

## Cum rulezi
Nu necesită build.

```bash
python3 -m http.server 8000
```
Apoi mergi la `http://localhost:8000`.

## Cum folosești rapid
1. Te autentifici (prima autentificare pe email creează cont local).
2. Adaugi echipamente și urmărești statusul garanțiilor.
3. Activezi notificările browser din secțiunea **Notificări**.
4. Exporți datele în CSV sau PDF.
5. (Opțional) configurezi `Bin ID` + `API Key` JSONBin și faci sync cloud.

## Observații de securitate
- Este un MVP: parolele sunt stocate local, necriptat.
- Pentru producție: recomandat backend dedicat, hash parole, JWT/OAuth, DB securizat.
