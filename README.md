# Automação residencial com Home Assistant

## Equipamentos utilizados
- 1 Raspberry PI 3 + cartão micro SD de 32 GB 
- 4 Sonoff Basic R2
- 6 Sonoff Mini R4 Extreme
- 1  Sonoff Slampher
- 1 Sonoff TH10 + sensor de temperatura ds18b20] (para ligar no aquecedor e medir a temperatura do aquário)
- 1 [Broadlink RM4 PRO + sensor de temperatura/umidade HTS2](https://pt.aliexpress.com/item/1005001625163568.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w)
- 3 lâmpadas [Yeelight RGB](https://pt.aliexpress.com/item/32885328641.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aGm32Rz) 
- 1 lâmpada [Philips/Xiaomi](https://pt.aliexpress.com/item/32853967773.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90awXatLR) - Obs: essa não está em uso,
- 4 lâmpadas [Sonoff B05-B-A60](https://pt.aliexpress.com/item/1005002061178114.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) - comprei barato a lampada, mas não recomendo, pois tem alguns problemas: 1) não permite ligar em estado **desligado**. 2) Ao ligar a torneira elétrica, a lampada "enfraquece" e 3) não permite o controle local. Obs: não estou mais usando essas lampadas
- 1 chromecast de 2ª geração (afinal, a TV do quarto não é smart) - 
- 1 Google Nest 2ª geração
- 1 [controlador RGB](https://pt.aliexpress.com/item/1005001800139865.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA&gatewayAdapt=glo2bra)
- 1 [Régua inteligente](https://pt.aliexpress.com/item/1005006381172584.html?src=google&src=google&albch=shopping&acnt=768-202-3196&slnk=&plac=&mtctp=&albbt=Google_7_shopping&isSmbAutoCall=false&needSmbHouyi=false&albcp=17355674356&albag=&trgt=&crea=pt1005006381172584&netw=x&device=c&albpg=&albpd=pt1005006381172584&gad_source=1&gclid=Cj0KCQjwgJyyBhCGARIsAK8LVLM0P9oeS1uW3-LGFv__bEAilEBUQPfPkYD9fdCY5MOez6eXvMw4YPsaArKBEALw_wcB&gclsrc=aw.ds&aff_fcid=a64e164450e342c3bc92172ecf0e1a2e-1715983676269-00096-UneMJZVf&aff_fsk=UneMJZVf&aff_platform=aaf&sk=UneMJZVf&aff_trace_key=a64e164450e342c3bc92172ecf0e1a2e-1715983676269-00096-UneMJZVf&terminal_id=f2727c40bb8440afb6bb715e795e2166&afSmartRedirect=y)
- 1 [sensor de temperatura/umidade](https://www.aliexpress.com/item/1005004592980757.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA)
- 3 [sensor de temperatura/umidade](https://pt.aliexpress.com/item/1005005883460491.html?spm=a2g0o.order_list.order_list_main.31.5d05caa4Ee7QZP&gatewayAdapt=glo2bra)
- 2 [sensor de abertura de portas](https://pt.aliexpress.com/item/1005005880697254.html?spm=a2g0o.order_list.order_list_main.26.5d05caa4Ee7QZP&gatewayAdapt=glo2bra)
- 1 [sensor medidor de energia](https://pt.aliexpress.com/item/1005005873738695.html?spm=a2g0o.order_list.order_list_main.21.5d05caa4Ee7QZP&gatewayAdapt=glo2bra)
- 1 Smart TV LG 50" 4K 50UQ7950
- 1 Sound bar LG SP8A
- 2 Ar Condicionado LG S4NQ12JA31C
- 1 Lavadora LG V2
- 1 Motor de portão AGL trino 300 

## Componetes utilizados
Componentes instalados manualmente, dentro da pasta ``config\custom_components``
- [localtuya](https://github.com/rospogrigio/localtuya) - Permite controlar os dispositivos compatíveis com o app Tuya sem trocar o firmware, mas não funciona com todos os dispositivos 
- [MikrotikRouter](https://github.com/tomaae/homeassistant-mikrotik_router) - Permite obter informações de roteadores Mikrotik. **Não confundir com a integração nativa do Home Assistant**
- [smartthinq_sensors](https://github.com/ollo69/ha-smartthinq-sensors) - Permite controlar o ar condicionado e a máquina da lavar da LG
- [Sonoff Lan](https://github.com/AlexxIT/SonoffLAN) - Permite controlar os Sonoffs sem trocar o firmware 
## Cards Lovelave
- [button-card.js](https://github.com/custom-cards/button-card)
- [mini-graph-card-bundle.js](https://github.com/kalkih/mini-graph-card)
- [mini-media-player](https://github.com/kalkih/mini-media-player)
- [mushroom.js](https://github.com/piitaya/lovelace-mushroom)

## Integrações utilizadas
- ``generic_thermostat`` permite ler os dados de um sensor de temperatura e controlar um switch (conectado a um aquecedor)
- ``generic_hygrostat`` permite ler os dados de um sensor de umidade e controlar um switch (conectado a um umidificador de ar)

## Tutorias utilizados
- [Obtendo o tráfego da WAN do Roteador via SNMP](https://forum.homeassistantbrasil.com.br/t/obtendo-o-trafego-da-wan-do-roteador-via-snmp-tempo-real/92). Observação: foi necessário encontrar os OIDs corretos das interfaces, pois varia de acordo com cada modelo. 

## Interface em 17/05/2024
![Alt text](prints/Firefox_Screenshot_2024-05-18T00-33-45.738Z.png?raw=true "Title")

