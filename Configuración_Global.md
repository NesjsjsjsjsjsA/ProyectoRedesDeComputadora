# Documentación GNS3

Se comparte las configuraciones hechas para cada maquina de cada nivel

## Nivel uno

### Configuracion R1

```
configure terminal
interface FastEthernet 0/0
no shutdown
exit

interface FastEthernet 0/0.10
encapsulation dot1Q 10
ip address 192.168.50.1 255.255.255.248
exit

interface FastEthernet 0/0.20
encapsulation dot1Q 20
ip address 192.168.50.9 255.255.255.248
exit

interface FastEthernet 0/0.30
encapsulation dot1Q 30
ip address 192.168.50.41 255.255.255.248
exit

interface FastEthernet 0/0.40
encapsulation dot1Q 40
ip address 192.168.50.81 255.255.255.252
exit

interface FastEthernet 0/0.50
encapsulation dot1Q 50
ip address 192.168.50.85 255.255.255.252
exit

interface FastEthernet 0/1
ip address 192.168.50.101 255.255.255.252
no shutdown
exit

router ospf 1
network 192.168.50.0 0.0.0.255 area 0
end

wr

show ip interface brief

show ip protocols

```

### Configuracion maquinas

1. PC-Ventas

```
ip 192.168.50.2 255.255.255.248 192.168.50.1
save
show ip
```

2. PC-C_Red

```
ip 192.168.50.10 255.255.255.248 192.168.50.9
save
show ip
```

3. PC-A_Clientes

```
ip 192.168.50.42 255.255.255.248 192.168.50.41
save
show ip
```

4. PC-Recepción

```
ip 192.168.50.82 255.255.255.252 192.168.50.81
save
show ip
```

5. PC-S_Espera

```
ip 192.168.50.86 255.255.255.252 192.168.50.85
save 
show ip
```


## Nivel dos

### Configuración router R2

```
configure terminal
interface FastEthernet 0/0
no shutdown
exit

interface FastEthernet 0/0.60
encapsulation dot1Q 60
ip address 192.168.50.17 255.255.255.248
exit

interface FastEthernet 0/0.70
encapsulation dot1Q 70
ip address 192.168.50.25 255.255.255.248
exit

interface FastEthernet 0/0.80
encapsulation dot1Q 80
ip address 192.168.50.49 255.255.255.248
exit

interface FastEthernet 0/0.90
encapsulation dot1Q 90
ip address 192.168.50.57 255.255.255.248
exit

interface FastEthernet 0/0.100
encapsulation dot1Q 100
ip address 192.168.50.89 255.255.255.252
exit

interface FastEthernet 0/0.110
encapsulation dot1Q 110
ip address 192.168.50.109 255.255.255.252
exit

interface FastEthernet 0/1
ip address 192.168.50.102 255.255.255.252
no shutdown
exit

interface FastEthernet1/0
ip address 192.168.50.105 255.255.255.252
no shutdown
exit

router ospf 1
network 192.168.50.0 0.0.0.255 area 0
end

wr

show ip protocols

show ip interface brief

```

### Configuración Maquinas

1. PC-Admin

```
ip 192.168.50.18 255.255.255.248 192.168.50.17
save
show ip
```

2. PC-C_Red

```
ip 192.168.50.26 255.255.255.248 192.168.50.25
save
show ip
```

3. PC-Contabilidad

```
ip 192.168.50.50 255.255.255.248 192.168.50.49
save
show ip
```

4. PC-Gerencia

```
ip 192.168.50.58 255.255.255.248 192.168.50.57
save
show ip
```

5. PC-S_Reuniones

```
ip 192.168.50.90 255.255.255.252 192.168.50.89
save
show ip
```

6. PC-RRHH

```
ip 192.168.50.110 255.255.255.252 192.168.50.109
save
show ip
```


## Nivel tres

### Configuración de router R3

```
configure terminal
interface FastEthernet 0/0
no shutdown
exit

interface FastEthernet 0/0.120
encapsulation dot1Q 120
ip address 192.168.50.33 255.255.255.248
exit

interface FastEthernet 0/0.130
encapsulation dot1Q 130
ip address 192.168.50.65 255.255.255.248
exit

interface FastEthernet 0/0.140
encapsulation dot1Q 140
ip address 192.168.50.73 255.255.255.248
exit

interface FastEthernet 0/0.150
encapsulation dot1Q 150
ip address 192.168.50.93 255.255.255.252
exit

interface FastEthernet 0/0.160
encapsulation dot1Q 160
ip address 192.168.50.97 255.255.255.252
exit

interface FastEthernet 0/1
ip address 192.168.50.106 255.255.255.252
no shutdown 
exit

router ospf 1
network 192.168.50.0 0.0.0.255 area 0
end

wr

show ip interface brief

show ip protocols

```

### Configuración de Maquinas

1. PC-GerenciaG

```
ip 192.168.50.34 255.255.255.248 192.168.50.33
save
show ip

```

2. PC-Servidores

```
ip 192.168.50.66 255.255.255.248 192.168.50.65
save 
show ip
```

3. PC-Soporte

```
ip 192.168.50.74 255.255.255.248 192.168.50.73
save
show ip
```

4. PC-Juntas

```
ip 192.168.50.94 255.255.255.252 192.168.50.93
save
show ip
```

5. PC-S_TI

```
ip 192.168.50.98 255.255.255.252 192.168.50.97
save
show ip
```

