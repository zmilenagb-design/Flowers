
# Proyecto Flowers 🌸

## Descripción del Proyecto
Este proyecto es una solución tecnológica para la gestión de un catálogo floral, desarrollada como parte de la formación técnica.

# Patrones de Diseño Aplicados
**Repository Pattern:** Implementado para separar la lógica de acceso a datos (Azure SQL) de la lógica de negocio, facilitando el mantenimiento.
**Singleton: Utilizado** para gestionar la instancia única de conexión con Azure Blob Storage, optimizando el uso de recursos.

# Principios SOLID
**S** (Single Responsibility): Cada módulo tiene una función única; por ejemplo, la clase `ImageLoader` se encarga exclusivamente de la comunicación con el storage.
**O** (Open/Closed):** El sistema permite agregar nuevos tipos de flores o categorías mediante configuración sin alterar el código base.
**D** (Dependency Inversion):** Los componentes de alto nivel dependen de abstracciones, no de implementaciones concretas de la base de datos.

# Diagrama de los Tiers de la arquitectura
El diseño del sistema se encuentra documentado en la carpeta de activos del proyecto.

Diagrama de los Tiers (![arquitectura01 png](https://github.com/user-attachments/assets/dcc09749-a404-4a7e-9e7c-e441b40a3cd3)
)

# CI/CD (Integración y Despliegue Continuo)
Se utiliza **GitHub Actions** para garantizar la calidad del software:
-**Build:** Compilación automática tras cada commit.
- **Deploy:** Despliegue automático hacia **Azure App Service** al fusionar cambios en la rama principal.

# Arquitectura del Sistema

La aplicación está organizada en tres niveles:

### Presentation Tier
- Navegador Web
- Aplicación React

### Application Tier
- Hooks personalizados
- Servicios de acceso a datos

### Data Tier
- Microsoft Azure Blob Storage

# Diagrama de los Layers
El diseño del sistema se encuentra documentado en la carpeta de activos del proyecto.

Diagrama de los Layers(![arquitectura02 png](https://github.com/user-attachments/assets/2bff06de-8974-4439-aa4d-d960c76b465d)
)

# Arquitectura del Sistema
La aplicación está organizada siguiendo Arquitectura Limpia, separando responsabilidades para mantener el código organizado y fácil de mantener.

## Presentacion layers
- Manejan la estructura de las páginas de la aplicación.
- Organizan y combinan los componentes de la interfaz.

## Components (Interfaz)
- Elementos reutilizables de la interfaz como botones, formularios o tarjetas.
- Solo manejan la presentación visual.

## Hooks (Lógica de aplicación)
- Contienen la lógica de estado y comportamiento de la aplicación.
- Conectan los componentes con los servicios.

## Services (Acceso a datos)
- Se encargan de la comunicación con APIs o bases de datos.
- Manejan integraciones externas.

# Patrones de Diseño Aplicados

En esta arquitectura se pueden usar varios patrones de diseño, por ejemplo:
- **Patrón Component:** Permite crear elementos reutilizables de interfaz.
- **Patrón Service Layer:** Separa la lógica de acceso a datos en los servicios.
- **Patrón Hook o Custom Hook:** Permite reutilizar lógica dentro de la aplicación.
- **Patrón Modular:** Divide el sistema en partes independientes para facilitar mantenimiento.

# Principios SOLID

**Responsabilidad única:** cada capa tiene una función específica.
**Abierto/Cerrado:** el sistema puede ampliarse sin modificar el código existente.
**Inversión de dependencias:** las capas superiores dependen de abstracciones y no de implementaciones directas.
