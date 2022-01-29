# Automação residencial com Home Assistant

## Equipamentos utilizados
- 1 Raspberry PI 3 + cartão micro SD de 32 BG
- 4 Sonoff Basic R2
- 1  Slampher
- 1 [Sonoff TH10 + sensor de temperatura ds18b20](https://pt.aliexpress.com/item/32865452363.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90ay59UfH) (para ligar no aquecedor e medir a temperatura do aquário)
- 1 [Broadlink RM4 PRO + sensor de temperatura/umidade HTS2](https://pt.aliexpress.com/item/1005001625163568.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w)
- 1 [Broadlink RM4c Mini](https://pt.aliexpress.com/item/33032400979.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) **(atenção que esse modelo não suporta o sensor HTS2)**
- 1 lâmpada [Yeelight RGB](vhttps://pt.aliexpress.com/item/32885328641.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aGm32Rz) 
- 1 lâmpada [Philips/Xiaomi](https://pt.aliexpress.com/item/32853967773.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90awXatLR)
- 4 lâmpadas [RGB Sonoff B05-B-A60](https://pt.aliexpress.com/item/1005002061178114.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w) - comprei barato a lampada, mas tem alguns problemas: 1) não permite ligar em estado **desligado**. 2) Ao ligar a torneira elétrica, a lampada "enfraquece".
- 1 chromecast de 2ª geração (afinal, a TV não é smart)

## Componetes utilizados
Componentes instalados manualmente, dentro da pasta ``config\custom_components``
- [Sonoff Lan](https://github.com/AlexxIT/SonoffLAN) - Não precisa trocar o firmware dos Sonoffs
- [SmartIR](https://github.com/smartHomeHub/SmartIR) - 

## Cards Lovelave
- [button-card.js](https://github.com/custom-cards/button-card)
- [mini-graph-card-bundle.js](https://github.com/kalkih/mini-graph-card)
- [simple-weather-card-bundle.js](https://github.com/kalkih/simple-weather-card)

## Integrações utilizadas
- ``smartir`` permite controlar dispositivos via IR (ex: ar condicionado)
- ``generic_thermostat`` permite ler os dados de um sensor de temperatura e ligar/controlar um switch (conectado a um aquecedor)
- ``generic_hygrostat`` permite ler os dados de um sensor de umidade e ligar/controlar um switch (conectado a um umidificador de ar)


## Tutorias utilizados
- [Obtendo o tráfego da WAN do Roteador via SNMP](https://forum.homeassistantbrasil.com.br/t/obtendo-o-trafego-da-wan-do-roteador-via-snmp-tempo-real/92) 

## Interface em 29/01/2022
![Alt text](print.png?raw=true "Title")

