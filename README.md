## Gestion Piscine avec un esp32  

### Fonctions Principales :      
 
 - pression filtre à sable
 - temperature eau piscine
 - contact pompe de filtration (commande du contacteur de puissance)
 - ph
 - capteur circulation eau oui/non
 - led de status + ecran

### Liste des composants :

- [un pcb diy multi-roles](https://github.com/NicoDupont/PCB/tree/main/multi-role)
- [detecteur de debit d'eau F3/4](https://www.amazon.fr/dp/B0B3RL9H4V?psc=1&ref=ppx_yo2ov_dt_b_product_details)
- [capteur de pression analogique 0=>30PSI](https://www.amazon.fr/Capteur-Pression-Walfront-0-5-4-5V-Transmetteur/dp/B07KJXNCJ3/ref=sr_1_1_sspa?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1KLC8P4V7IX1C&keywords=pression+0-30psi&qid=1686149428&s=hi&sprefix=pression+0-30psi%2Cdiy%2C120&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1&smid=A2ITG3U79VPZKX)
- [2x contact magnetique ouverture de porte](https://www.amazon.fr/gp/product/B00PZMG980/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- [sonde ph](https://www.aliexpress.com/item/32995322213.html?spm=a2g0o.order_list.order_list_main.66.58601802quQO2y)
- prises en charge pour pvc pression 50mm
- [puits de sonde ds18b20](https://www.amazon.fr/dp/B07DXFWV6B?psc=1&ref=ppx_yo2ov_dt_b_product_details)
- [isolateur i2c dfrobot pour le capteur PH](https://www.dfrobot.com/product-1778.html) 

### Montage :

![boitier](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/elec1.jpg?raw=true)
![boitier](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/elec2.jpg?raw=true)
![isolateur+ads1115](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/isolateur.jpg?raw=true)
![isolateur+ads1115](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/ph.jpg?raw=true)

### Calibrer la sonde PH avec les solutions PH :

 - video youtube : https://www.youtube.com/watch?v=tHYt3oUGYbw

### HomeAssistant panneau piscine :

![links](https://github.com/NicoDupont/esp_gestion_piscine/blob/main/img/ha.png?raw=true)

#### Evolutions possibles mais pas prevues pour le moment :  
 - Sonde orp
 - Remplissage auto niveau avec vanne motorisée / electrovanne, flotteur  , debimetre
 - Gestion Hivernage
 - Gestion ph+ ou ph- avec une pompe péristaltique
 - Gestion chlore avec une pompe péristaltique
