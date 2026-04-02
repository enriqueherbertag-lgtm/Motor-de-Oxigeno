# Motor de Oxígeno

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

Sistema de propulsión que extrae oxígeno del aire ambiente, lo concentra y lo quema con combustible en una turbina, generando energía mecánica sin emisiones de NOx. Diseñado para operar en atmósferas convencionales, entornos pobres en oxígeno (alta montaña, submarinos) o incluso en Marte, integrado con torres ShieldAir.

## ¿Qué es?

El Motor de Oxígeno es un concepto de propulsión basado en la separación activa del oxígeno del aire. A diferencia de un motor de combustión interna convencional, que diluye el oxígeno con nitrógeno (reduciendo eficiencia y generando NOx), este sistema:

1. **Captura aire ambiente**.
2. **Separa oxígeno puro** mediante membranas de grafeno o zeolitas.
3. **Inyecta combustible** (hidrógeno, metano, sintético).
4. **Quema en cámara cerrada** a alta temperatura y presión.
5. **Expande los gases** en una turbina para generar energía mecánica.
6. **Expulsa vapor de agua y CO₂**, o los recircula si se busca cero emisiones.

El principio es similar al de un cohete, pero el oxidante no se almacena en tanques, sino que se extrae del entorno en tiempo real.

## Arquitectura general


[AIRE AMBIENTE]
│
▼
┌─────────────────┐
│ CAPTURA │ Entrada de aire, filtrado de partículas
└────────┬────────┘
▼
┌─────────────────┐
│ SEPARADOR O₂ │ Membranas de grafeno / zeolitas. Produce O₂ puro.
└────────┬────────┘ (el resto (N₂, CO₂) se expulsa o se usa en otras funciones)
▼
┌─────────────────┐
│ COMBUSTIÓN │ Cámara donde se inyecta combustible y se quema con O₂.
└────────┬────────┘ Temperatura > 2000°C (controlada).
▼
┌─────────────────┐
│ TURBINA │ Los gases de combustión expanden, mueven un rotor.
└────────┬────────┘ Genera energía mecánica (eje rotativo).
▼
┌─────────────────┐
│ ESCAPE │ Gases residuales (H₂O, CO₂) se expulsan o capturan.
└─────────────────┘


## Ventajas sobre motores convencionales

| Característica | Motor convencional | Motor de Oxígeno |
|----------------|--------------------|------------------|
| Oxidante | Aire ambiente (21% O₂, 79% N₂) | O₂ puro (separado del aire) |
| Eficiencia térmica | Limitada por dilución con N₂ | Mayor, al quemar con O₂ puro |
| Emisiones NOx | Altas (por la reacción N₂ + O₂ a alta T) | Cero (no hay N₂ en la combustión) |
| Funcionamiento en atmósferas pobres | No | Sí (si hay fuente de O₂ o CO₂) |
| Adaptación a Marte | No | Sí (con ShieldAir-Mars) |

## Integración con ShieldAir

El Motor de Oxígeno puede recibir su O₂ directamente de:

- **ShieldAir-Urban**: en ciudades, usando la torre para extraer oxígeno del smog.
- **ShieldAir-Mars**: en Marte, usando CO₂ atmosférico para producir O₂ y luego quemarlo con hidrógeno.

Esto convierte a ShieldAir en el *combustible* de un sistema de propulsión, no solo en un purificador o generador.

## Aplicaciones

| Ámbito | Uso |
|--------|-----|
| **Terrestre** | Motores de combustión limpia para vehículos pesados, generación eléctrica sin NOx. |
| **Submarinos** | Propulsión independiente de aire exterior, usando oxígeno producido a bordo. |
| **Alta montaña / desierto** | Funcionamiento donde el aire es pobre en O₂. |
| **Espacio / Marte** | Propulsión para etapas de ascenso, usando O₂ producido in situ (ISRU). |
| **Sistemas cerrados** | Bases autónomas que queman residuos o hidrógeno con oxígeno reciclado. |

## Estado del proyecto

| Componente | Estado |
|------------|--------|
| Concepto | Definido |
| Flujo de aire | Esquematizado |
| Separación de O₂ | Basado en tecnología existente (membranas, zeolitas) |
| Cámara de combustión | En fase conceptual |
| Turbina | Pendiente de diseño |
| Integración con ShieldAir | Definida |
| Prototipo | Pendiente |

## Próximos pasos

1. Selección de tecnología de separación de O₂ (membranas de grafeno vs. zeolitas).
2. Diseño de la cámara de combustión con O₂ puro (control de temperatura, materiales).
3. Simulación de flujo y eficiencia térmica.
4. Integración con ShieldAir-Urban para pruebas en banco.
5. Adaptación a ShieldAir-Mars para pruebas en atmósfera simulada.

## Proyectos relacionados

- **ShieldAir-Urban** — torre de captura y purificación de aire.
- **ShieldAir-Mars** — torre de producción de O₂ desde CO₂ atmosférico.
- **Goliat-Orbital** — sistema orbital autónomo (comparte principios de separación de gases).
- **CORPUS** — sistemas de energía y metabolismo artificial.

## Licencia

Copyright © 2026 Enrique Aguayo. Todos los derechos reservados.

Este proyecto está protegido por derechos de autor.

**PERMITIDO:**
- Uso no comercial con fines educativos o de investigación.
- Distribución sin modificación, siempre que se mantenga esta licencia y se dé crédito al autor.

**PROHIBIDO sin autorización expresa por escrito:**
- Uso comercial (incluyendo, pero no limitado a: ofrecerlo como servicio, SaaS, suscripción, integración en productos que generen ingresos, o cualquier uso que genere beneficio económico directo o indirecto).
- Modificación para entornos de producción.
- Distribución de versiones modificadas sin autorización.

Para licencias comerciales, soporte técnico, pilotos empresariales o consultas:
Contacto: **eaguayo@migst.cl**

Cualquier uso fuera de los términos permitidos requiere permiso previo del autor.

Las consultas comerciales son bienvenidas y se responderán en un plazo máximo de 7 días hábiles.

## Autor

**Enrique Aguayo H.**  
Mackiber Labs  
Contacto: eaguayo@migst.cl  
ORCID: 0009-0004-4615-6825  
GitHub: [@enriqueherbertag-lgtm](https://github.com/enriqueherbertag-lgtm)

Documentación asistida por **Ana (DeepSeek)** , IA para investigación y optimización técnica.

