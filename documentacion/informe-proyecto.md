# Informe Técnico del Proyecto de Red MPLS Corporativa

## 1. Objetivo General
Diseñar e implementar una red corporativa distribuida que asegure alta disponibilidad, segmentación lógica, escalabilidad y capacidad de diagnóstico, conectando 3 sedes mediante una arquitectura basada en MPLS y protocolos de enrutamiento dinámico.

## 2. Alcance del Proyecto
- 3 sedes conectadas con MPLS
- Segmentación por VLAN (Finanzas, RRHH, IT)
- Protocolos: OSPF (intra-sede), BGP (inter-sede)
- Simulación en Cisco Packet Tracer
- Documentación completa y estandarizada

## 3. Descripción de la Arquitectura
- Backbone MPLS con enlaces entre routers Cisco 2901
- VLANs implementadas sobre switches Cisco 2960
- Enlaces trunk entre routers y switches
- IPs por subred funcional y direccionamiento jerárquico

## 4. Diagramas de Red
- [Topología lógica](../diagramas/topologia-logica.png)
- [Topología física](../diagramas/topologia-fisica.png)

## 5. Protocolos Utilizados
- **MPLS**: Backbone multisede
- **OSPF**: Routing interno por sede
- **BGP**: Anuncio y convergencia entre sedes

## 6. Justificación Técnica
> Se eligió MPLS por su capacidad para segmentar tráfico por etiquetas y soportar políticas QoS y VRF.  
> OSPF fue seleccionado por su eficiencia intra-área.  
> BGP facilita el control de enrutamiento entre sedes.

## 7. Equipamiento Simulado
- 3x Cisco 2901 (routers)
- 3x Cisco 2960 (switches L2)
- 6 PCs (por VLAN)

## 8. Herramientas Utilizadas
- Cisco Packet Tracer
- Draw.io
- PlantUML
- GitHub
- Markdown

## 9. Autor
**Bruno San Martín Navarro**  
[LinkedIn](https://www.linkedin.com/in/SanMaBruno/) | [GitHub](https://github.com/SanMabruno)

