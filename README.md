# Kulturarv
Her kan du finde en zip-fil for hver kommune som har data hos Kulturarvsstyrelsen omkring bevaringsværdige bygninger

## Metode
Jeg har hentet view_bygning_fredningstatus_lav, view_bygning_fredningstatus_med, view_bygning_fredningstatus_hoej fra kulturarv.dk WFS

Derefter har jeg tilføjet bygningens koordinater fra BBR-bygninger, så punktet er flyttet fra adresse-punktet til bygnings-punktet

Så har jeg hentet GeoDanmark Bygninger fra WFS hvis BBR-UUID findes i GeoDanmark, dvs. hvis der står 0 i gdk_id, betyder det ikke at bygningen ikke findes, men bare at bygningen ikke er geokodet.

## Output
I zip-filen ligger der to shp-filer, kulturarv_xxx.shp og kulturarv_xxx_mangler_i_bbr.shp
### Kulturarv_xxx.shp
Denne fil indeholder alle bevaringsværdige bygninger som har et tilsvarende UUID i BBR, men ikke nødvendigvis i GeoDanmark

### Mangler i BBR
Denne fil indeholder de bevaringsværdige bygninger som ikke har en UUID i BBR
