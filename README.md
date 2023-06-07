## Gestion Piscine avec un esp32  

### Fonctions Principales :      
 
 - pression filtre à sable
 - temperature eau pisicine
 - contact pompe de filtration
 - ph
 - capteur circulation eau  

### Liste des composants :

Electronique :  
- 1x esp32u 
- 4x relais 5v (1x4) (alimenté en 5v, logique en 3.3v)
- 1x alim 12v2A
- 1x convertisseur dc 12v=>5v
- 1x convertisseur dc 5v=>3.3v (ams1117)
- 1x BME280 (3.3v)
- 2x DS18B20 (3.3v)
- 1x resistance 4.7 Kohm
- 2x résistance 10 kohm
- 1x PCF8575 (3.3v)
- 1x ADS1115 (5v) + 1x level shifter (i2c 5v<=>3.3v)
- 1x MLX90614 non-contact thermometer
- 1x ecran i2c ssd1306
- 1x [pzem-004t v3](https://www.aliexpress.com/item/1005005620371930.html?spm=a2g0o.order_list.order_list_main.29.58601802vbEUjW)
- 2x led verte basique
- 2x fusibles + 2x porte fusible
- pcb 2.54mm, jst, bornier, etc...

Autres :  
- [detecteur de debit d'eau F3/4](https://www.amazon.fr/dp/B0B3RL9H4V?psc=1&ref=ppx_yo2ov_dt_b_product_details)
- [capteur de pression analogique 0=>30PSI](https://www.amazon.fr/Capteur-Pression-Walfront-0-5-4-5V-Transmetteur/dp/B07KJXNCJ3/ref=sr_1_1_sspa?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1KLC8P4V7IX1C&keywords=pression+0-30psi&qid=1686149428&s=hi&sprefix=pression+0-30psi%2Cdiy%2C120&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1&smid=A2ITG3U79VPZKX)
- [2x contact magnetique ouverture de porte](https://www.amazon.fr/gp/product/B00PZMG980/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- [sonde ph](https://www.aliexpress.com/item/32995322213.html?spm=a2g0o.order_list.order_list_main.66.58601802quQO2y)
- prise charge pour pvc pression 50mm
- [puits de sonde ds18b20](https://www.amazon.fr/dp/B07DXFWV6B?psc=1&ref=ppx_yo2ov_dt_b_product_details)

### Cablage :

![links](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/shema.png?raw=true)

### Montage :

![board](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/pcbok.jpg?raw=true)
![boitier domotique](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/boxdomo.jpg?raw=true)
![boitier electrique](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/boxelec.jpg?raw=true)

### Calibrer la sonde PH avec les solutions PH :

 - préparer les solutions de tests et de l'eau distillé pour rincer la sonde

### HomeAssistant panneau piscine :

![links](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/hapiscine.png?raw=true)

#### Entités :

![links](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/entite.png?raw=true)

#### Evolutions possibles :  
 - Sonde orp
 - Remplissage auto niveau avec vanne motorisée, flotteur  , debimetre
 - Gestion Hivernage
 - Gestion ph+ ou ph- avec une pompe péristaltique
 - Gestion chlore avec une pompe péristaltique