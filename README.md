# CargoPay Authorization System

## Descripción del Proyecto

El **CargoPay Authorization System** es una solución robusta y escalable para la autorización y gestión de pagos. Desarrollado con .NET Core, este sistema está diseñado para manejar transacciones financieras de manera eficiente, segura y adaptable a diferentes industrias, como comercio electrónico, fintech, y gestión empresarial.

## Características Principales

- **Gestión de Tarjetas:**
  - Creación de tarjetas virtuales con un saldo inicial configurable.
  - Consultas de saldo en tiempo real.
  - Procesamiento de pagos con cálculo automático de tarifas dinámicas.

- **Manejo de Transacciones:**
  - Sistema de tarifas dinámicas actualizadas automáticamente cada hora, proporcionadas por el servicio Universal Fees Exchange (UFE).
  - Optimizado para manejar altos volúmenes de transacciones.

- **Seguridad y Escalabilidad:**
  - Autenticación mediante JSON Web Tokens (JWT) para garantizar la seguridad de las transacciones.
  - Arquitectura modular basada en MVC, adaptable a sistemas empresariales existentes.

- **Documentación Interactiva:**
  - Integración con Swagger para documentar y probar los endpoints de la API.

## Aplicaciones Prácticas

Este sistema puede ser integrado en diversas industrias, tales como:
- **Comercio Electrónico:** Gestión de pagos en plataformas de tiendas en línea.
- **Fintech:** Procesamiento de transacciones y manejo de tarjetas virtuales.
- **Empresas:** Automatización de la gestión de pagos internos y externos.

## Tecnologías Utilizadas

- **Backend:**
  - .NET Core
  - Entity Framework Core
  - SQL Server

- **Patrones de Diseño:**
  - Modelo Vista Controlador (MVC)
  - Inyección de Dependencias
  - Servicios en segundo plano para tareas automatizadas (e.g., actualización de tarifas).

- **Seguridad:**
  - Autenticación mediante JWT.
  - Middleware personalizado para manejo centralizado de excepciones.

- **Documentación:**
  - Swagger para la descripción y prueba de endpoints de la API.

## Endpoints Principales

1. **Crear Tarjeta**
   - **URL:** `/api/Card`
   - **Método:** `POST`
   - **Descripción:** Genera una tarjeta virtual con un saldo inicial configurable.

2. **Procesar Pago**
   - **URL:** `/api/Card/{id}/pay`
   - **Método:** `POST`
   - **Descripción:** Procesa un pago utilizando una tarjeta virtual existente.

3. **Consultar Saldo**
   - **URL:** `/api/Card/{id}/balance`
   - **Método:** `GET`
   - **Descripción:** Consulta el saldo disponible en una tarjeta.

## Cómo Configurar y Ejecutar el Proyecto

### Requisitos Previos
1. Instalar **.NET Core SDK**.
2. Tener configurado **SQL Server**.
3. Instalar las herramientas de **Entity Framework Core**.

### Pasos de Configuración
1. Clona el repositorio:
   ```bash
   git clone https://github.com/ingenieraLesly/CargoPayAuthorizationSystem.git
   ```
2. Configura la conexión a la base de datos en el archivo `appsettings.json`.
3. Ejecuta los scripts de configuración de base de datos incluidos en `SETUP.md`.
4. Aplica las migraciones de la base de datos:
   ```bash
   dotnet ef database update
   ```
5. Ejecuta la aplicación:
   ```bash
   dotnet run
   ```

### Despliegue en Producción
El sistema es compatible con servicios en la nube como **Azure**, **AWS** o **Heroku**, y puede configurarse para procesar pagos de forma remota.

## Mejoras Futuras

1. Ampliar la compatibilidad con múltiples monedas y métodos de pago.
2. Optimizar el manejo de grandes volúmenes de transacciones para entornos con alta concurrencia.
3. Crear un sistema de notificaciones para informar a los usuarios sobre actualizaciones de saldo y transacciones.

## Autor

**Lesly Paola Aguilar Rincón**  
Desarrolladora de Software  
[GitHub](https://github.com/ingenieraLesly) | [LinkedIn](https://www.linkedin.com/in/lesly-flytric/)  
