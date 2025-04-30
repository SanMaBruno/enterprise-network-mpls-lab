# Informe Técnico del Proyecto de Red MPLS Corporativa

**Autor:** Bruno San Martín Navarro  
**Fecha:** Abril 2025  
**Repositorio:** [GitHub - enterprise-network-mpls-lab](https://github.com/SanMaBruno/enterprise-network-mpls-lab)

---

## 🎯 1. Objetivo General

Diseñar e implementar una red corporativa distribuida entre tres sedes, basada en tecnología MPLS, segmentada por VLANs y gestionada mediante protocolos de enrutamiento dinámico (OSPF y BGP), asegurando escalabilidad, disponibilidad y documentación profesional para su mantenimiento y diagnóstico.

---

## 📐 2. Alcance

- 3 sedes geográficamente distribuidas.
- Backbone MPLS simulado entre routers principales.
- Segmentación por VLAN (Finanzas, RRHH, IT).
- Enrutamiento interno OSPF y externo BGP.
- Simulación completa en Cisco Packet Tracer.
- Documentación técnica profesional y automatizada.

---

## 🧱 3. Arquitectura de Red

- **Routers Cisco 2901** conectados por enlaces MPLS.
- **Switches Cisco 2960** con VLANs por área funcional.
- PCs segmentados por VLAN en cada sede.
- Trunks entre routers y switches.
- Direccionamiento jerárquico por sede y función.

---

## 🧭 4. Diagramas del Proyecto

- 📊 [Topología Lógica](../diagramas/topologia-logica.png)
- 🧩 [Topología Física](../diagramas/topologia-fisica.png)

---

## 📡 5. Protocolos y Servicios

| Protocolo | Uso                                 |
|-----------|--------------------------------------|
| MPLS      | Transporte entre sedes (Backbone)   |
| OSPF      | Enrutamiento interno por sede       |
| BGP       | Enrutamiento entre sedes            |
| VLAN      | Segmentación lógica por departamentos |

---

## ⚙️ 6. Equipamiento Simulado

- 3x Cisco 2901 (routers)
- 3x Cisco 2960 (switches L2)
- 6x PCs
- Plataforma: Cisco Packet Tracer

---

## 🛠 7. Documentación Incluida

| Archivo                             | Descripción                                 |
|-------------------------------------|---------------------------------------------|
| procedimientos-configuracion.md     | Guía técnica paso a paso                    |
| pautas-mantenimiento.md             | Mantenimiento preventivo planificado        |
| plan-contingencia.md                | Respuesta ante fallos operativos            |
| configuraciones/*.txt               | Configuraciones reales por equipo           |
| diagnostico-fallas/*.md             | Casos de falla simulados y solución         |

---

## ✅ 8. Justificación Técnica

Se eligió MPLS por su capacidad de segmentar servicios, soportar múltiples protocolos y escalar fácilmente a nivel corporativo. OSPF fue seleccionado por su eficiencia en entornos internos y convergencia rápida, mientras que BGP permite controlar el enrutamiento entre dominios administrativos. La segmentación por VLAN garantiza orden y seguridad a nivel de capa 2.

---

## 📌 9. Conclusiones

Este laboratorio demuestra competencias técnicas avanzadas en diseño, implementación y documentación de redes, posicionando al autor como un candidato ideal para roles de ingeniería de redes en entornos de misión crítica. La estandarización en nombres, estructura y documentación refuerza una visión orientada a buenas prácticas y trabajo en equipo.

