# Настройка протокола STP

## Команды настройки

### Switch 1
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch1
switch1(config)> spanning-tree mode pvst
switch1(config)> spanning-tree vlan 1 root primary
switch1(config)> end
switch1> wr
```

### Switch 2
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch2
switch2(config)> spanning-tree mode pvst
switch2(config)> spanning-tree vlan 1 root secondary
switch2(config)> end
switch2> wr
```

### Switch 3
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch3
switch3(config)> spanning-tree mode pvst
switch3(config)> end
switch3> wr
```

версия с измененной стоимостью
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch3
switch3(config)> spanning-tree mode pvst
switch3(config)> interface Gi0/0
switch3(config-if)> spanning-tree cost 10
switch3(config-if)> exit
switch3(config)> interface Gi0/1
switch3(config-if)> spanning-tree cost 10
switch3(config-if)> exit
switch3(config)> end
switch3> wr
```

### Switch 4
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch4
switch4(config)> spanning-tree mode pvst
switch4(config)> end
> wr
```

### Switch 5
```shell
vIOS-L2> enable
vIOS-L2> config terminal
vIOS-L2(config)> hostname switch5
switch5(config)> spanning-tree mode pvst
switch5(config)> end
switch5> wr
```

### pc 1
```shell
PC1> ip 10.0.0.11/24
PC1> save config
```

### pc 2
```shell
PC2> ip 10.0.0.12/24
PC2> save config
```

### pc 3
```shell
PC3> ip 10.0.0.13/24
PC3> save config
```

### pc 4
```shell
PC4> ip 10.0.0.14/24
PC4> save config
```

### pc 5
```shell
PC5> ip 10.0.0.15/24
PC5> save config
```

### pc 6
```shell
PC6> ip 10.0.0.16/24
PC6> save config
```

## Топология сети
![topology](images/lab2_topology1.png)
![topology](images/lab2_topology2.png)

## STP пакеты
### Swtich 1 eth 0 <-> switch 2 eth 0
![link sw 1 eth0 sw2 eth0](images/link_sw1_eth0_sw2_eth0.png)

### Swtich 1 eth 1 <-> switch 2 eth 1
![link sw 1 eth1 sw2 eth1](images/link_sw1_eth1_sw2_eth1.png)

### Swtich 1 eth 2 <-> switch 3 eth 0
![link sw 1 eth2 sw3 eth0](images/link_sw1_eth2_sw3_eth0.png)

### Swtich 1 eth 3 <-> switch 3 eth 1
![link sw 1 eth3 sw3 eth1](images/link_sw1_eth3_sw3_eth1.png)

### Swtich 1 eth 4 <-> switch 4 eth 0
![link sw 1 eth4 sw4 eth0](images/link_sw1_eth4_sw4_eth0.png)

### Swtich 1 eth 5 <-> switch 4 eth 1
![link sw 1 eth5 sw4 eth1](images/link_sw1_eth5_sw4_eth1.png)

### Swtich 1 eth 6 <-> switch 5 eth 0
![link sw 1 eth6 sw5 eth0](images/link_sw1_eth6_sw5_eth0.png)

### Swtich 1 eth 7 <-> switch 5 eth 1
![link sw 1 eth7 sw5 eth7](images/link_sw1_eth7_sw5_eth1.png)

## Проверка доступности
### pc 1
![pc1 ping](images/pc1_ping.png)

### pc 2
![pc2 ping](images/pc2_ping.png)

### pc 3
![pc3 ping](images/pc3_ping.png)

### pc 4
![pc4 ping](images/pc4_ping.png)

### pc 5
![pc5 ping](images/pc5_ping.png)

### pc 6
![pc6 ping](images/pc6_ping.png)
