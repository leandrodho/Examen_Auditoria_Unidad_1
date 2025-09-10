# Informe de Auditoría de Sistemas - Examen de la Unidad I

**Nombres y apellidos:** Leandro Hurtado Ortiz  
**Fecha:** 10/09/2025  
**URL GitHub:** [https://github.com/leandrodho/Examen_Auditoria_Unidad_1](https://github.com/leandrodho/Examen_Auditoria_Unidad_1)

---

## 1. Proyecto de Auditoría de Riesgos

### Login

**Evidencia:**  
![Login](img/login1.png)

![Login2](img/login2.png)

**Descripción:**  
El inicio de sesión ficticio se implementó mediante un componente en React (`Login.jsx`) y un servicio de autenticación (`LoginService.js`) que valida credenciales predefinidas (usuario: **admin**, contraseña: **123456**).  
Al iniciar sesión correctamente, se guarda un token simulado en `localStorage` para mantener la sesión activa y se muestra la interfaz principal del sistema. Este mecanismo no utiliza base de datos real, sino que emula la autenticación únicamente con datos en memoria del navegador.

---

### Motor de Inteligencia Artificial

**Evidencia:**  
![Motor IA](img/motorIA.png)

**Descripción:**  
El motor de IA se implementó en el backend (`app.py`) usando Flask. Se crearon los endpoints **/analizar-riesgos** y **/sugerir-tratamiento**, que reciben datos del activo y devuelven riesgos, impactos y posibles tratamientos.  
La lógica utiliza un modelo local de lenguaje y expresiones regulares para procesar la respuesta y enviarla en formato JSON al frontend.

---

## 2. Hallazgos

![Agregar nuevo activo](img/agregaractivo.png)

### Activo 1: Servidor de base de datos

**Evidencia:**  
![Servidor de base de datos](img/activo1.png)

**Condición:**  
Se identificó el riesgo de pérdida del servidor de base de datos, lo que implica la posibilidad de perder información valiosa relacionada con las operaciones críticas del banco.  

**Recomendación:**  
Aplicar políticas de seguridad específicas para bases de datos, incluyendo cifrado en reposo y en tránsito, autenticación multifactor para administradores, controles de acceso basados en roles, así como respaldos automáticos y monitoreo continuo de logs.  

**Riesgo:** Alta  

---

### Activo 2: VPN Corporativa

**Evidencia:**  
![VPN Corporativa](img/activo2.png)

**Condición:**  
Se identificó riesgo de pérdida de la VPN corporativa, lo que podría ocasionar la interrupción del acceso remoto seguro y la exposición de información sensible en tránsito.  

**Recomendación:**  
Fortalecer la seguridad de la VPN implementando cifrado robusto (IKEv2/IPsec o WireGuard), habilitar autenticación multifactor, limitar accesos por roles y registrar todas las conexiones para detectar anomalías.  

**Riesgo:** Alta  

---

### Activo 3: Firewall Perimetral

**Evidencia:**  
![Firewall Perimetral](img/activo3.png)

**Condición:**  
Se identificó riesgo de pérdida o fallo del firewall perimetral, lo que expone la red corporativa a posibles accesos no autorizados y tráfico malicioso.  

**Recomendación:**  
Implementar un firewall perimetral de nueva generación, reforzar las políticas de filtrado, aplicar controles de acceso físico y lógico, y monitorear continuamente los eventos de red.  

**Riesgo:** Media  

---

### Activo 4: Registros de Auditoría

**Evidencia:**  
![Registros de Auditoría](img/activo4.png)

**Condición:**  
Se identificó riesgo de pérdida de registros de auditoría, lo que compromete la trazabilidad de eventos de seguridad y dificulta la detección de incidentes o accesos indebidos.  

**Recomendación:**  
Asegurar que los registros se almacenen de forma centralizada, con acceso restringido y en sistemas inmutables; habilitar copias de seguridad automáticas y aplicar monitoreo continuo de accesos a los logs.  

**Riesgo:** Medio  

---

### Activo 5: Aplicación Web de Banca

**Evidencia:**  
![Aplicación Web de Banca](img/activo5.png)

**Condición:**  
Se identificó riesgo de pérdida de la aplicación web de banca, lo que podría ocasionar la indisponibilidad del servicio para los clientes y la exposición de datos financieros sensibles.  

**Recomendación:**  
Implementar desarrollo seguro siguiendo los lineamientos de OWASP, habilitar pruebas de penetración periódicas, monitorear accesos en tiempo real y aplicar medidas de alta disponibilidad (balanceadores de carga, redundancia).  

**Riesgo:** Alta  

---

## Anexo 1: Activos de información

*(Se conserva la lista completa de los activos del examen como referencia)*

---

