# Automação residencial com Home Assistant
O Home Assistant é uma plataforma de automação residencial open source. O processo de automação residencial é algo que nunca tem fim, pois sempre há novos dispositivos, integrações e ideias para serem exploradas.
Por isso, este projeto está em constante evolução e dificilmente estará "pronto". Toda a configuração, integrações e experiências que tive estão documentadas aqui, servindo tanto como registro pessoal quanto como referência para quem deseja implementar algo semelhante.
## Equipamentos utilizados
- 4 Sonoff Basic R2
- 6 Sonoff Mini R4 Extreme
- 5 interruptores Tuya - Apesar de serem mais baratos e mais completos que os da Sonoff, dão mais problemas e dois já queimaram
- 1 Sonoff TH10 + sensor de temperatura ds18b20
- 1 [Broadlink RM4 PRO + sensor de temperatura/umidade HTS2](https://pt.aliexpress.com/item/1005001625163568.html?gatewayAdapt=glo2bra&spm=a2g0o.9042311.0.0.2742b90aP3fL4w)
- 3 lâmpadas Yeelight RGB 
- 2 luminárias de embutir Ekasa
- 2 Google Nest 2ª geração
- 4 controladores RGB Magic Home: Tem integração nativa e funcionam em modo LAN, sem depender da nuvem
- 3 Réguas inteligentes "Tuya"
- 1 sensor de temperatura/umidade: Inicialmente comprei um que usava 3 pilhas, depois troquei por outro que tem um IR junto. Apesar de não conseguir usar o IR, as mediçãoes de temperatura são mais precisas, pois as atualizaçãoes não ocorrem a cada 5 minutos
- 2 [sensor de temperatura/umidade](https://pt.aliexpress.com/item/1005005883460491.html?spm=a2g0o.order_list.order_list_main.31.5d05caa4Ee7QZP&gatewayAdapt=glo2bra)
- 2 [sensor de abertura de portas](https://pt.aliexpress.com/item/1005005880697254.html?spm=a2g0o.order_list.order_list_main.26.5d05caa4Ee7QZP&gatewayAdapt=glo2bra). Depois que passei a usar sensores Zigbee, não usaria sensores com pilha/wifi, pois descarregam rápido (em torno de 30 dias)
- 2 [sensores medidor de energia](https://pt.aliexpress.com/item/1005005873738695.html?spm=a2g0o.order_list.order_list_main.21.5d05caa4Ee7QZP&gatewayAdapt=glo2bra): Usados para medir o consumo/retorno de energia elétrica à rede e a produção solar
- 2 Smart TV LG
- 1 Sound bar LG SP8A
- 3 Ar Condicionado LG
- 1 Lavadora LG V2 (sou fã da LG)
- 1 Motor de portão AGL trino 300 
- 1 [Mikrotik C52iG](https://mikrotik.com/product/hap_ax2) - Roteador principal
- 1 [Mikrotik 952Ui](https://mikrotik.com/product/RB952Ui-5ac2nD) - Apenas faz as funções de access point e switch
- 1 [Repetidor TP RE200](https://mikrotik.com/product/RB952Ui-5ac2nD) - Usado apenas para repedir o sinal sinal da rede de IoT
- 1 [Sonoff zigbee dongle-e](https://pt.aliexpress.com/item/1005007089589385.html?src=google&pdp_npi=4%40dis!BRL!236.76!108.93!!!!!%40!12000039362722962!ppc!!!&snps=y&snpsid=1&src=google&albch=shopping&acnt=752-015-9270&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=_oDeeeiG&gclsrc=aw.ds&&albagn=888888&&ds_e_adid=775659227243&ds_e_matchtype=search&ds_e_device=c&ds_e_network=g&ds_e_product_group_id=2446396853741&ds_e_product_id=pt1005007089589385&ds_e_product_merchant_id=5551326180&ds_e_product_country=BR&ds_e_product_language=pt&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=23055122380&albag=188614690929&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=23055122380&gbraid=0AAAAA_eFwRCSqJmM80e5fuNzbksRWQ9sW&gclid=Cj0KCQiA5abIBhCaARIsAM3-zFWsq2ifidBfff3zMJRmjCmWn5ayvrvQNS0cpPlyOj65iQUicTl6JcMaAmiYEALw_wcB): Tive MUITO trabalho para configurar. A versão E é mais nova, portanto, não era 100% compatível com o Home Assistant. Foi necessário atualizar o firmware e segui o tutorial disponível [aqui](https://www.youtube.com/watch?v=x1QeNPi6tK8). Isso deu possibilidade de adicionar alguns dispositivos zigbee na rede, sendo eles:
- 1 [Sonoff Mini R4 Extreme Zigbee](https://www.aliexpress.com/p/tesla-landing/index.html?scenario=c_ppc_item_bridge&productId=1005005402936930&_immersiveMode=true&withMainCard=true&src=google&aff_platform=true&isdl=y&src=google&albch=shopping&acnt=615-992-9880&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=_oFgTQeV&gclsrc=aw.ds&&albagn=888888&&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=pt1005005402936930&ds_e_product_merchant_id=107718315&ds_e_product_country=BR&ds_e_product_language=pt&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=22561659993&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=22571595037&gbraid=0AAAAA_TvRHqLcYn0kEukFSOB4EqpVM79a&gclid=Cj0KCQiA5abIBhCaARIsAM3-zFV3RiFW-mBBBHzb1Gxo4c0W17PhC99aAEqjFakm5qLVoMikBOwOBPwaAvz8EALw_wcB)
- 1 PIR Zigbee

## Equipamentos INutilizados
Ao longo do tempo, alguns equipamentos foram sendo trocados, pois não eram mais necessários ou por não terem sido as melhores compras. São eles:
- 1 Raspberry PI 3 + cartão micro SD de 32 GB - Com a aposentadoria do meu laptop velho, passei a usar ele através de uma VM, permitindo ter mais serviços implantados
- 1 chromecast de 2ª geração (afinal, agora as duas televisões são smart) 
- 1  Sonoff Slampher. Coloquei um interruptor sonoff zigbee sem neutro.
- 1 lâmpada Philips/Xiaomi - Obs: essa lampada comprei em 2017
- 4 lâmpadas Sonoff B05-B-A60 - comprei barato a lampada, mas não recomendo, pois tem alguns problemas: 1) não permite ligar em estado **desligado**. 2) Ao ligar a torneira elétrica, a lampada "enfraquece" e 3) não permite o controle local.

## Componetes utilizados
Componentes instalados manualmente, dentro da pasta ``config\custom_components``. Atualmente estou com o [HACS](https://www.hacs.xyz/) instalado, mas isso não é necessário.
- [localtuya](https://github.com/rospogrigio/localtuya) - Permite controlar os dispositivos compatíveis com o app Tuya sem trocar o firmware, mas não funciona com todos os dispositivos 
- [MikrotikRouter](https://github.com/tomaae/homeassistant-mikrotik_router) - Permite obter informações de roteadores Mikrotik. **Não confundir com a integração nativa do Home Assistant**
- [smartthinq_sensors](https://github.com/ollo69/ha-smartthinq-sensors) - Permite controlar o ar condicionado e a máquina da lavar da LG. Agora já existe a intregração nativa LG Thinq, mas elas não trazem exatamente as mesmas informações. **Ambas dependem de internet**.
- [Sonoff Lan](https://github.com/AlexxIT/SonoffLAN) - Permite controlar os Sonoffs no modo LAN sem trocar o firmware 
## Cards Lovelave
- [button-card.js](https://github.com/custom-cards/button-card)
- [mini-graph-card-bundle.js](https://github.com/kalkih/mini-graph-card)
- [mini-media-player](https://github.com/kalkih/mini-media-player)
- [mushroom.js](https://github.com/piitaya/lovelace-mushroom)
- [simple-weather-card-bundle.js](https://github.com/kalkih/simple-weather-card)

## Tutoriais utilizados
- [Obtendo o tráfego da WAN do Roteador via SNMP](https://forum.homeassistantbrasil.com.br/t/obtendo-o-trafego-da-wan-do-roteador-via-snmp-tempo-real/92). Observação: foi necessário encontrar os OIDs corretos das interfaces, pois varia de acordo com cada modelo. 
- [Integrando o OpenWRT ao Home Assistant](https://jonbrito.dev/articles/openwrt-mqtt-ha)

## Interface em 04/11/2025
![Alt text](prints/Captura de tela 2025-11-04 150727.png?raw=true "Interface principal")

