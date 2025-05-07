# 🏢 Enterprise Network Lab - Arquitectura Tipo MPLS

Este proyecto representa el diseño e implementación de una arquitectura de red corporativa multi-sede, simulando una topología tipo MPLS sobre un entorno OSPF con segmentación lógica mediante VLANs. Se utiliza Cisco Packet Tracer para replicar el comportamiento de una red empresarial con alta disponibilidad, modularidad y escalabilidad.

> ⚠️ Nota: Dado que Cisco Packet Tracer no soporta MPLS real ni BGP, la arquitectura está orientada a simular su lógica mediante OSPF y una red backbone full-mesh entre routers.

---

## 🧩 Características Técnicas

- Enrutamiento dinámico con **OSPF** (entre routers)
- **Switching L2** con subinterfaces y VLANs por departamento (TI, RRHH, Contabilidad)
- Segmentación lógica con **encapsulación 802.1Q (dot1Q)**
- **Topología full-mesh** entre routers (backbone simulado tipo MPLS)
- **Configuración completa de red** con pruebas de conectividad
- **Documentación técnica** profesional en formato Markdown y diagramas .drawio

---
## 📂 Estructura del proyecto

```
enterprise-network-mpls-lab/
├── red-mpls-empresarial.pkt # Archivo principal de simulación (Cisco Packet Tracer)
├── README.md # Descripción general del proyecto
├── .gitignore # Exclusión de archivos del control de versiones
├── documentacion/ # Documentación técnica y diagramas
│ ├── topologia-red-mpls.drawio # Diagrama lógico de red
│ └── capturas/ # Evidencias de pruebas (pings, configuraciones, etc.)
├── configuraciones/ # Configuraciones de routers y switches (archivos .txt)
│ ├── routerA.txt
│ ├── routerB.txt
│ ├── routerC.txt
│ ├── switchA.txt
│ ├── switchB.txt
│ └── switchC.txt
├── diagnostico-fallas/ # Casos simulados de error y su resolución
│ ├── caso1.md
│ └── caso2.md
├── presupuesto/ # Estimación de costos y componentes (opcional)
│ └── costos-referenciales.xlsx
└── README.md                   # Descripción general del proyecto y objetivos
```


---

## ⚙️ Herramientas Utilizadas

- Cisco Packet Tracer 8.x
- Draw.io (diagrams.net)
- Git + GitHub
- VS Code (edición Markdown)
- Excel / LibreOffice / Numbers

---

## 🎯 Objetivo del Proyecto

Demostrar competencias avanzadas en diseño de redes empresariales, documentación estructurada y buenas prácticas de simulación técnica, orientadas a roles profesionales en telecomunicaciones, infraestructura TI y soporte técnico de nivel senior.

---
## 📸 Vista previa

📁 Diagrama visual de la topología (editable): [`topologia-red-empresarial-mpls.drawio`](documentacion/topologia-red-mpls.png)

🖼️ Imagen exportada para previsualización directa:

![Topología de red](documentacion/topologia-red-empresarial-mpls.png)
