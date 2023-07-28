# Automação residencial com Home Assistant

## Equipamentos utilizados
- 1 Raspberry PI 3 + cartão micro SD de 32 GB
- 4 Sonoff Basic R2
- 1  Sonoff Slampher
- 1 [Sonoff TH10 + sensor de temperatura ds18b20](https://pt.aliexpress.com/item/32865452363.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90ay59UfH) (para ligar no aquecedor e medir a temperatura do aquário)
- 1 [Broadlink RM4 PRO + sensor de temperatura/umidade HTS2](https://pt.aliexpress.com/item/1005001625163568.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w)
- 3 lâmpadas [Yeelight RGB](vhttps://pt.aliexpress.com/item/32885328641.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aGm32Rz) 
- 1 lâmpada [Philips/Xiaomi](https://pt.aliexpress.com/item/32853967773.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90awXatLR)
- 4 lâmpadas [Sonoff B05-B-A60](https://pt.aliexpress.com/item/1005002061178114.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) - comprei barato a lampada, mas tem alguns problemas: 1) não permite ligar em estado **desligado**. 2) Ao ligar a torneira elétrica, a lampada "enfraquece".
- 1 chromecast de 2ª geração (afinal, a TV do quarto não é smart)
- 1 Google Nest
- 1 [controlador RGB](https://pt.aliexpress.com/item/1005001800139865.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA&gatewayAdapt=glo2bra)
- 1 [sensor de temperatura/umidade](https://www.aliexpress.com/item/1005004592980757.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA)
- 1 [Smart TV LG 50" 4K 50UQ7950](https://www.google.com/search?client=firefox-b-d&q=++++Smart+TV+LG+50%22+4K+50UQ7950)
- 1 [Sound bar LG SP8A](https://www.google.com/search?q=lg+sp8a&client=firefox-b-d&sxsrf=AB5stBicd98WTvRjNufagQPddMQMXnos1Q%3A1690585440238&ei=YEnEZJaYDvHX5OUP5YaHgAc&oq=lg+sp&gs_lp=Egxnd3Mtd2l6LXNlcnAiBWxnIHNwKgIIATIEECMYJzIHECMYigUYJzIFEAAYgAQyBRAAGIAEMgcQABiKBRhDMgUQABiABDIHEAAYigUYQzIHEAAYigUYQzIHEAAYigUYQzIHEAAYigUYQ0iGHlCmCljlEXAEeAGQAQCYAa0DoAG0CqoBBzItNC4wLjG4AQPIAQD4AQHCAgoQABhHGNYEGLADwgIPECMYigUYJxidAhhGGPoBwgINEC4YigUYxwEY0QMYQ8ICCxAAGIAEGLEDGIMBwgILEC4YigUYsQMYgwHCAggQLhiABBixA8ICExAuGIoFGLEDGIMBGMcBGNEDGEPCAggQABiABBixA8ICIhAuGIoFGLEDGIMBGMcBGNEDGEMYlwUY3AQY3gQY4ATYAQHCAgwQIxiKBRgTGIAEGCfCAgoQABiKBRixAxhDwgILEAAYigUYsQMYgwHCAgsQLhiABBjHARivAeIDBBgAIEGIBgGQBgi6BgYIARABGBQ&sclient=gws-wiz-serp)
- 2 [Ar Condicionado LG S4NQ12JA31C](https://www.google.com/search?client=firefox-b-d&q=Ar+Condicionado+LG+S4NQ12JA31C)

## Componetes utilizados
Componentes instalados manualmente, dentro da pasta ``config\custom_components``
- [Sonoff Lan](https://github.com/AlexxIT/SonoffLAN) - Não precisa trocar o firmware dos Sonoffs 
- [MikrotikRouter](https://github.com/tomaae/homeassistant-mikrotik_router) - Permite obter informações de roteadores Mikrotik. **Não confundir com a integração nativa do Home Assistant**
- [smartthinq_sensors](https://github.com/ollo69/ha-smartthinq-sensors) - Permite controlar o ar condicionado LG através do wifi
## Cards Lovelave
- [button-card.js](https://github.com/custom-cards/button-card)
- [mini-graph-card-bundle.js](https://github.com/kalkih/mini-graph-card)
- [simple-weather-card-bundle.js](https://github.com/kalkih/simple-weather-card)
- [mini-media-player-bundle.js](https://github.com/kalkih/mini-media-player)

## Integrações utilizadas
- ``smartir`` permite controlar dispositivos via IR (ex: ar condicionado)
- ``generic_thermostat`` permite ler os dados de um sensor de temperatura e controlar um switch (conectado a um aquecedor)
- ``generic_hygrostat`` permite ler os dados de um sensor de umidade e controlar um switch (conectado a um umidificador de ar)

## Tutorias utilizados
- [Obtendo o tráfego da WAN do Roteador via SNMP](https://forum.homeassistantbrasil.com.br/t/obtendo-o-trafego-da-wan-do-roteador-via-snmp-tempo-real/92) 

## Interface em 28/07/2023
![Alt text](prints/interface1.png?raw=true "Title")

