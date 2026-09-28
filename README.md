# AgriStopa — natívne Android obaly

Toto **nie je** samotná aplikácia AgriStopa. Sú to dva malé natívne obaly,
ktoré na telefóne zobrazujú AgriStopu zo servera a pridávajú to, čo
prehliadač na Androide nedokáže — nahrávanie GPS, ktoré systém nesmie uspať.

Samotná aplikácia sa vyvíja v Lovable (repozitár `plow-and-plan`).
Tu sa nikdy neupravuje obsah aplikácie — len obal.

## Dve aplikácie

| Súbor | Pre koho | Otvára | Identifikátor |
|---|---|---|---|
| `AgriStopa.apk` | vodiči | kabínu (`/m`) | `sk.agristopa.kabina` |
| `AgriStopa-Vedenie.apk` | vedenie, mechanizátor, ekonóm | prihlásenie (`/auth`) | `sk.agristopa.vedenie` |

Majú rôzne identifikátory, takže sa dajú mať v telefóne obe naraz.

## Odkazy na stiahnutie (trvalé)

- Vodiči: `https://github.com/tomasnemeth/agristopa-app/releases/latest/download/AgriStopa.apk`
- Vedenie: `https://github.com/tomasnemeth/agristopa-app/releases/latest/download/AgriStopa-Vedenie.apk`

Pri každej zmene v tomto repozitári GitHub zostaví obe aplikácie sám
(záložka **Actions**) a nahrá ich na tie isté odkazy.

## Nastavenia

Adresy sú v `config/kabina.json` a `config/vedenie.json` v poli `server.url`.
Keď raz prejdeme na vlastnú doménu, mení sa len tam.

## Známe obmedzenie

Pri prvom spustení (a po reštarte aplikácie) potrebuje telefón internet,
aby sa AgriStopa načítala. Po načítaní funguje aj bez signálu — záznamy
sa ukladajú do fronty a odošlú sa, keď je signál.
