# AUDIT EVIDENCE: E-001 - NETWORK SEGMENTATION BREACH

**Client:** NovaPay (Fintech)
**Date of Discovery:** January 29, 2026
**Auditor:** Felipe González Arcos
**Asset ID:** CORE-NW-VLAN-20 (Guest) / CORE-NW-CDE-50 (Production)

## 1. Technical Observation / Observación Técnica
During a standard network topology review and trace-route execution, a persistent logical route was identified between the Guest Wi-Fi segment and the Cardholder Data Environment (CDE).
(Durante una revisión estándar de la topología de red y ejecución de trace-route, se identificó una ruta lógica persistente entre el segmento Wi-Fi de Invitados y el Entorno de Datos de Tarjetas).

* **Source (Origen):** VLAN 20 (Guest) - 192.168.20.x
* **Destination (Destino):** Subnet 50 (CDE) - 10.0.50.x

## 2. Risk Impact / Impacto de Riesgo
**Threat Vector:** Lateral Movement.
An unauthorized user on the Guest network can perform network discovery and potential data exfiltration from the CDE, violating PCI DSS 4.0 isolation principles.
(Un usuario no autorizado en la red de invitados puede realizar descubrimiento de red y potencial filtración de datos desde el CDE, violando los principios de aislamiento de PCI DSS 4.0).

## 3. Compliance Status / Estado de Cumplimiento
**Status:** NON-COMPLIANT (Requirement 1.2.1)
