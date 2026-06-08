# laboratorio-red-pyme-cloud
Diseño y documentación de una infraestructura de red segura para entornos híbridos"
# Red Híbrida Segura para PYME con Políticas BYOD

¡Bienvenido a mi repositorio de prácticas! En este laboratorio diseñé y documenté la infraestructura de red para una empresa ficticia (o un caso de estudio) de 25 usuarios que requiere conectar sus servidores locales con la nube de forma segura.

## 🎯 Objetivos del Laboratorio
* Diseñar una topología de red privada virtual (VPC) dividida en zonas seguras.
* Implementar políticas de control de acceso para dispositivos propios de los trabajadores (BYOD).
* Asegurar que el tráfico de datos crítico viaje encriptado.

## 🗺️ Topología de la Red
*(Aquí puedes arrastrar y soltar una imagen de tu diagrama de red hecho en Packet Tracer, Visio o Lucidchart)*

## 🛠️ Herramientas Utilizadas
* **Simulación:** Cisco Packet Tracer / AWS VPC (según lo que uses).
* **Seguridad:** Firewall perimetral, Listas de Control de Acceso (ACLs) y cifrado WPA3.
* **Gestión:** Consola de Administración para identidades de usuarios.

## 📝 Documentación del Paso a Paso

### 1. Segmentación de Redes
Se crearon tres subredes principales para evitar que un virus en la red de invitados afecte a los servidores:
* **Subred de Administración (VLAN 10):** Solo para personal de TI y servidores locales.
* **Subred de Empleados / BYOD (VLAN 20):** Con aislamiento de clientes para que los celulares de los trabajadores no se vean entre sí.
* **Subred de Invitados (VLAN 30):** Con acceso directo a Internet y bloqueo total hacia la red corporativa.

### 2. Políticas de Seguridad Aplicadas
* **Bloqueo de Puertos:** Se cerraron todos los puertos no esenciales en el Firewall, permitiendo únicamente tráfico seguro HTTPS (puerto 443) y VPN.
* **Auditoría:** Configuración de alertas automáticas en caso de que un dispositivo desconocido intente conectarse a la red de administración.

---
📬 **Contacto:** Si deseas conocer más detalles de este diseño o requieres una consultoría para tu infraestructura, puedes contactarme a través de mi perfil de LinkedIn o escribirme por aquí.
