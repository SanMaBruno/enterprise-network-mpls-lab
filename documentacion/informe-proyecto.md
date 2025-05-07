# Informe Técnico del Proyecto de Red Corporativa con Arquitectura Tipo MPLS

**Autor:** Bruno San Martín Navarro  
**Fecha:** Abril 2025  
**Repositorio:** [GitHub - enterprise-network-mpls-lab](https://github.com/SanMaBruno/enterprise-network-mpls-lab)

---

## 🎯 1. Objetivo General

Diseñar e implementar una red corporativa distribuida entre tres sedes, simulando una arquitectura tipo MPLS mediante enlaces backbone y segmentación por VLANs. El proyecto utiliza enrutamiento dinámico OSPF, encapsulación 802.1Q y documentación estructurada para garantizar escalabilidad, disponibilidad y facilidad de diagnóstico.

---

## 📐 2. Alcance

- Red multisede simulada con conectividad completa entre sedes A, B y C.
- Arquitectura de backbone estilo MPLS (sin etiquetado real) sobre OSPF.
- Segmentación por VLAN (TI, Contabilidad, RRHH).
- Enrutamiento dinámico interno con OSPF.
- Simulación y validación en Cisco Packet Tracer.
- Documentación profesional en Markdown y diagramas visuales.

---

## 🧱 3. Arquitectura de Red

- 3 routers Cisco 2911 en topología full-mesh.
- 3 switches Cisco 2960 con trunking y VLANs por departamento.
- 9 PCs distribuidos por función (3 por sede).
- Conexiones trunk entre routers y switches.
- Direccionamiento jerárquico por sede y VLAN.

---

## 🧭 4. Diagramas del Proyecto

- 🧩 Diagrama lógico: `documentacion/topologia-red-mpls.drawio`
- 📸 Imagen exportada: `documentacion/capturas/topologia-red-mpls.png`

---

## 📡 5. Protocolos y Servicios

| Protocolo | Uso                                       |
|-----------|--------------------------------------------|
| OSPF      | Enrutamiento entre routers (backbone)      |
| VLAN      | Segmentación lógica por áreas funcionales  |
| 802.1Q    | Encapsulación de subinterfaces (trunking)  |
| ICMP      | Validación de conectividad entre nodos     |

---

## ⚙️ 6. Equipamiento Simulado

- 3x Routers Cisco 2911
- 3x Switches Cisco 2960
- 9x PCs (TI, RRHH, Contabilidad por sede)
- Plataforma: Cisco Packet Tracer 8.x

---

## 🛠 7. Documentación Incluida

| Archivo                             | Descripción                                 |
|-------------------------------------|---------------------------------------------|
| procedimientos-configuracion.md     | Guía técnica paso a paso                    |
| pautas-mantenimiento.md             | Mantenimiento preventivo planificado        |
| plan-contingencia.md                | Respuesta ante fallos operativos            |
| configuraciones/*.txt               | Configuraciones por dispositivo (routers/switches) |
| diagnostico-fallas/*.md             | Casos de falla simulados y solución         |
| topologia-red-mpls.drawio/.png      | Diagrama visual y editable                  |
| red-mpls-empresarial.pkt            | Proyecto completo de simulación             |

---

## ✅ 8. Justificación Técnica

Se utilizó OSPF como protocolo de enrutamiento dinámico por su rápida convergencia y simplicidad en entornos empresariales internos. La estructura backbone simula una arquitectura MPLS para demostrar escalabilidad entre múltiples sedes. La segmentación por VLAN proporciona orden lógico, aislamiento de tráfico y base para políticas de seguridad. Todo el diseño respeta principios de modularidad, claridad y reutilización técnica.

---

## 📌 9. Conclusiones

Este laboratorio refleja una implementación profesional y estructurada de una red corporativa multi-sede, demostrando competencias clave en networking, documentación técnica y buenas prácticas de simulación. El proyecto está documentado, probado y organizado bajo estándares de ingeniería, ideal para roles en telecomunicaciones, infraestructura TI o soporte técnico avanzado.

---
