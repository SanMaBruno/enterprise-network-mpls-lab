# 📘 Procedimientos de Configuración Técnica

**Proyecto:** Red Empresarial Multi-Sede con Segmentación VLAN y Backbone Tipo MPLS  
**Autor:** Bruno San Martín Navarro  
**Fecha:** Abril 2025

---

## 1️⃣ Configuración de Routers (Cisco 2911)

### 🔧 Router A

```
hostname RouterA
no ip domain-lookup

! Configuración de interfaces hacia otros routers
interface GigabitEthernet0/0
 ip address 10.0.0.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 10.0.1.1 255.255.255.0
 no shutdown

! Subinterfaces para VLANs (dot1Q)
interface GigabitEthernet0/2.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface GigabitEthernet0/2.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0

interface GigabitEthernet0/2.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
```

### 🔧 Router B
```
hostname RouterB
no ip domain-lookup

interface GigabitEthernet0/0
 ip address 10.0.0.2 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 10.0.2.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/2.10
 encapsulation dot1Q 10
 ip address 192.168.110.1 255.255.255.0

interface GigabitEthernet0/2.20
 encapsulation dot1Q 20
 ip address 192.168.120.1 255.255.255.0

interface GigabitEthernet0/2.30
 encapsulation dot1Q 30
 ip address 192.168.130.1 255.255.255.0
```

### 🔧 Router C

```
hostname RouterC
no ip domain-lookup

interface GigabitEthernet0/0
 ip address 10.0.2.2 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 10.0.1.2 255.255.255.0
 no shutdown

interface GigabitEthernet0/2.10
 encapsulation dot1Q 10
 ip address 192.168.210.1 255.255.255.0

interface GigabitEthernet0/2.20
 encapsulation dot1Q 20
 ip address 192.168.220.1 255.255.255.0

interface GigabitEthernet0/2.30
 encapsulation dot1Q 30
 ip address 192.168.230.1 255.255.255.0
```


### 2️⃣ Configuración de OSPF
### 🧠 En todos los routers

```

router ospf 1
 network 10.0.0.0 0.0.255.255 area 0
```

### 3️⃣ Configuración de Switches (Cisco 2960)
### 🧱 VLANs
```

vlan 10
 name TI
vlan 20
 name CONTABILIDAD
vlan 30
 name RRHH
```

🔌 Puertos de acceso
```

interface range FastEthernet0/1 - 3
 switchport mode access
 switchport access vlan 10

interface range FastEthernet0/4 - 6
 switchport mode access
 switchport access vlan 20

interface range FastEthernet0/7 - 9
 switchport mode access
 switchport access vlan 30
```


### 🌉 Puerto trunk hacia el router
```

interface FastEthernet0/24
 switchport mode trunk
```


### 4️⃣ Direccionamiento de PCs
```

Cada PC fue configurado manualmente con:

Sede	VLAN	IP Estática	Gateway
A	10	192.168.10.10	192.168.10.1
A	20	192.168.20.10	192.168.20.1
A	30	192.168.30.10	192.168.30.1
B	10	192.168.110.10	192.168.110.1
B	20	192.168.120.10	192.168.120.1
B	30	192.168.130.10	192.168.130.1
C	10	192.168.210.10	192.168.210.1
C	20	192.168.220.10	192.168.220.1
C	30	192.168.230.10	192.168.230.1
```

### ✅ Validaciones realizadas
```

Pings exitosos entre PCs de distintas sedes y VLANs.

Convergencia OSPF verificada con show ip ospf neighbor.

Rutas aprendidas vía OSPF vistas con show ip route.

Trunks confirmados con show interfaces trunk.

VLANs activas con show vlan brief.
```


