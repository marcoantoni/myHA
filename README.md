# Automação residencial com Home Assistant

## Equipamentos utilizados
- 1 Raspberry PI 3 + cartão micro SD de 32 GB
- 4 Sonoff Basic R2
- 1  Sonoff Slampher
- 1 [Sonoff TH10 + sensor de temperatura ds18b20](https://pt.aliexpress.com/item/32865452363.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90ay59UfH) (para ligar no aquecedor e medir a temperatura do aquário)
- 1 [Broadlink RM4 PRO + sensor de temperatura/umidade HTS2](https://pt.aliexpress.com/item/1005001625163568.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w)
- 1 [Broadlink RM4c Mini](https://pt.aliexpress.com/item/33032400979.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) **(atenção que esse modelo não suporta o sensor HTS2)**
- 1 lâmpada [Yeelight RGB](vhttps://pt.aliexpress.com/item/32885328641.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aGm32Rz) 
- 1 lâmpada [Philips/Xiaomi](https://pt.aliexpress.com/item/32853967773.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90awXatLR)
- 4 lâmpadas [Sonoff B05-B-A60](https://pt.aliexpress.com/item/1005002061178114.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) - comprei barato a lampada, mas tem alguns problemas: 1) não permite ligar em estado **desligado**. 2) Ao ligar a torneira elétrica, a lampada "enfraquece".
- 1 chromecast de 2ª geração (afinal, a TV não é smart)
- 1 Google Nest
- 1 [controlador RGB](https://pt.aliexpress.com/item/1005001800139865.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA&gatewayAdapt=glo2bra)
- 1 [sensor de temperatura/umidade](https://www.aliexpress.com/item/1005004592980757.html?spm=a2g0o.order_list.0.0.555ccaa42PfbkA)

## Componetes utilizados
Componentes instalados manualmente, dentro da pasta ``config\custom_components``
- [Sonoff Lan](https://github.com/AlexxIT/SonoffLAN) - Não precisa trocar o firmware dos Sonoffs 
- [SmartIR](https://github.com/smartHomeHub/SmartIR) - Permite controlar dispositivos, como ar condicionado via IR
- [WebRTC](https://github.com/AlexxIT/WebRTC) - Zera o delay para visualização das câmeras via RTSP
- [MikrotikRouter](https://github.com/tomaae/homeassistant-mikrotik_router) - Permite obter informações de roteadores Mikrotik. **Não confundir com a integração nativa do Home Assistant**
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

## Interface em 29/01/2022
![Alt text](print30-01-22.png?raw=true "Title")

