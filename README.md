# AgriStopa — natívny Android obal

Toto **nie je** samotná aplikácia AgriStopa. Je to malý natívny obal,
ktorý na telefóne zobrazuje AgriStopu z adresy
`https://plow-and-plan.lovable.app` a navyše pridáva to, čo prehliadač
na Androide nedokáže:

- **nahrávanie GPS, ktoré systém nesmie uspať** (trvalé upozornenie v lište),
- beží ďalej pri zamknutom telefóne aj počas hovoru.

Samotná aplikácia sa naďalej vyvíja v Lovable (repozitár `plow-and-plan`).
Tu sa nikdy neupravuje obsah aplikácie — len obal.

## Ako vznikne APK

Pri každej zmene v tomto repozitári ho GitHub zostaví sám
(záložka **Actions** → beh **Zostav Android APK** → dole **AgriStopa-APK**).
APK sa stiahne ako ZIP, rozbalí a nainštaluje priamo do telefónu.

## Nastavenia

Adresa aplikácie je v `capacitor.config.json` v poli `server.url`.
Keď raz prejdeme na vlastnú doménu, mení sa len tento jeden riadok.

## Známe obmedzenie

Pri **úplne prvom spustení** (a po reštarte aplikácie) potrebuje telefón
internet, aby sa AgriStopa načítala. Po načítaní už funguje aj bez signálu
— záznamy sa ukladajú do fronty a odošlú sa, keď je signál.
