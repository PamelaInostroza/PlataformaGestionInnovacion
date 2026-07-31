# Plataforma modular de gestión de innovación

> Caso de estudio y propuesta de producto

![Estado](https://img.shields.io/badge/estado-caso_de_estudio-334155)
![Producto](https://img.shields.io/badge/producto-configurable-0f766e)
![Stack](https://img.shields.io/badge/stack-Next.js_%7C_Django_%7C_PostgreSQL-2563eb)

## Navegación

- [Resumen](#resumen)
- [En palabras simples](#en-palabras-simples)
- [Recorrido visual](#recorrido-visual)
  - [Acceso a la solución](#1-acceso-a-la-solución)
  - [Ingreso y administración de datos](#2-ingreso-y-administración-de-datos)
  - [Consulta y analítica](#3-consulta-y-analítica)
  - [Herramientas especializadas](#4-herramientas-especializadas)
- [Problema que resuelve](#problema-que-resuelve)
- [Arquitectura del producto](#arquitectura-del-producto)
- [Componentes](#componentes)
- [Capacidades demostradas](#capacidades-demostradas)
- [Personalización](#personalización)
- [Modelo de implementación](#modelo-de-implementación)
- [Modalidades](#modalidades)
- [Tecnologías](#tecnologías)
- [Estado y documentación](#estado)
- [Autoría y créditos](#autoría-y-créditos)

## Resumen

Plataforma integral para centralizar el ingreso, administración, seguimiento y visualización de proyectos, tecnologías, investigadores, instituciones e indicadores.

La solución combina dos componentes:

1. Un **sistema transaccional de ingreso y administración de datos**, orientado a reemplazar planillas y organizar la fuente institucional de información.
2. Un **portal web de consulta, seguimiento y analítica**, con catálogos relacionados, indicadores, herramientas operativas y acceso diferenciado.

El producto puede adaptarse al modelo de información, procesos, permisos, indicadores e identidad visual de cada organización.

## En palabras simples

La plataforma permite ingresar y ordenar la información de una organización en un solo lugar. Después convierte esos datos en fichas, indicadores, reportes y herramientas de seguimiento.

Cada cliente puede adaptar los formularios, permisos, procesos, indicadores y apariencia a sus propias necesidades.

![Flujo funcional del producto](images/flujo-producto.svg)

## Recorrido visual

Las siguientes capturas muestran una implementación institucional real. Se seleccionaron vistas sin registros personales visibles; los datos agregados corresponden a la interfaz demostrada y no constituyen una base de datos distribuida con este repositorio.

### 1. Acceso a la solución

![Portada del portal de innovación](images/01-portada.png)

El portal organiza el acceso al portafolio, los indicadores y las herramientas operativas.

### 2. Ingreso y administración de datos

![Selección de formularios del sistema de ingreso](images/02-formularios-demo.png)

El sistema de administración separa la información por dominios: investigadores, instituciones, equipo, proyectos, tecnologías y materias legales.

![Formulario estructurado para ingresar un proyecto](images/03-ingreso-datos-demo.png)

Los formularios incorporan secciones, campos obligatorios, relaciones con catálogos y controles de completitud.

### 3. Consulta y analítica

![Dashboard público del portafolio](images/05-dashboardpublico.png)

El portal transforma la información administrada en indicadores, distribuciones y resúmenes ejecutivos.

![Dashboard de análisis por áreas estratégicas](images/05-dashboardarea-demo.png)

La vista interna profundiza el análisis por ejes de trabajo, periodos e indicadores operativos.

![Listado anonimizado de proyectos](images/07-listado-demo.png)

Los listados permiten filtrar, seleccionar columnas y exportar información, manteniendo una navegación directa hacia las fichas relacionadas.

#### Ficha de proyecto

![Ficha demostrativa de un proyecto](images/08-ficha-proyecto-demo.png)

Reúne antecedentes, participantes, financiamiento, reuniones, documentos y entidades relacionadas.

#### Ficha de tecnología

![Ficha demostrativa de una tecnología](images/08-ficha-tecnologia-demo.png)

Organiza clasificación, nivel de madurez, propiedad intelectual, proyectos, investigadores e instituciones asociadas.

#### Ficha de investigador

![Ficha demostrativa de un investigador](images/08-ficha-investigador-demo.png)

Resume proyectos, tecnologías, actividad pública, propiedad intelectual y evolución anual del portafolio asociado.

#### Ficha de institución

![Ficha demostrativa de una institución](images/08-ficha-institucion-demo.png)

Permite visualizar en un solo lugar los proyectos y tecnologías relacionados con una organización.

Todas las fichas anteriores utilizan identidades y nombres ficticios preparados exclusivamente para esta demostración.

![Indicadores por áreas estratégicas](images/06-areas-estrategicas-demo.png)

Las áreas pueden consultar métricas y resultados relacionados con sus propios procesos.

### 4. Herramientas especializadas

![Menú de herramientas especializadas](images/11-herramientas-demo.png)

La solución integra herramientas operativas dentro de la misma experiencia.

![Plan de Desarrollo Tecnológico](images/09-gestorPDT-demo.png)

El gestor PDT permite organizar entregables y avances desde investigación y propiedad intelectual hasta mercado, calidad, escalamiento y financiamiento.

![Matriz de niveles de preparación para la innovación](images/09-gestorXRL-demo.png)

La matriz XRL reúne dimensiones comerciales, tecnológicas, de negocio, propiedad intelectual, equipo y financiamiento.

![Formulario demostrativo de declaración de invención](images/10-formulario-di-demo.png)

El módulo de declaración de invención organiza propuestas, responsables, revisión y estado. Los nombres y proyectos de esta imagen son ficticios.

## Problema que resuelve

Las organizaciones que gestionan innovación suelen mantener sus proyectos, tecnologías, investigadores, indicadores y procesos en planillas separadas. Esto produce duplicidad, errores de digitación, relaciones difíciles de mantener y poca trazabilidad.

La plataforma convierte esas fuentes dispersas en un sistema conectado:

- estructura el ingreso de información;
- valida reglas y relaciones;
- centraliza los datos maestros;
- entrega vistas apropiadas para cada perfil;
- automatiza reportes y actualizaciones;
- facilita el seguimiento y la toma de decisiones.

## Arquitectura del producto

![Arquitectura del producto](images/arquitectura-producto.svg)

La separación entre administración y publicación permite adaptar ambos componentes de forma independiente y aplicar controles diferentes a usuarios internos, investigadores, administradores y público general.

## Componentes

### Sistema de ingreso y administración

- Formularios estructurados por dominio.
- Creación, edición y consulta de registros.
- Catálogos maestros y relaciones entre entidades.
- Validación de campos y reglas de negocio.
- Importación masiva desde Excel.
- Administración de usuarios y permisos.
- Auditoría y trazabilidad de cambios.
- Exportación mediante contratos de datos estables.
- Migración progresiva desde procesos basados en planillas.

### Portal, seguimiento y analítica

- Portafolios de proyectos y tecnologías.
- Catálogos de investigadores e instituciones.
- Fichas relacionadas y filtros por periodo.
- Dashboards, indicadores, metas y tendencias.
- Seguimiento de madurez tecnológica TRL, PDT e IRL.
- Gestión de propiedad intelectual y documentos.
- Formularios para incubadora y declaraciones de invención.
- Reportes y fichas exportables.
- Notificaciones y herramientas operativas.
- API para integraciones y asistentes externos.

## Capacidades demostradas

- Arquitectura full stack con Next.js, React, TypeScript y Django.
- Modelamiento y transformación de información institucional.
- Integración con PostgreSQL/Supabase.
- Automatización de importaciones, respaldos y sincronizaciones.
- Validación preventiva de calidad e integridad de datos.
- Autenticación y autorización según perfiles.
- Dashboards, visualizaciones y generación de reportes.
- Diseño de APIs e integraciones server-side.
- Documentación de arquitectura, seguridad y operación.

## Personalización

| Área | Ejemplos de adaptación |
|---|---|
| Identidad visual | Marca, colores, tipografía, dominio e idioma |
| Modelo de datos | Entidades, campos, catálogos y relaciones |
| Formularios | Secciones, validaciones y flujos de aprobación |
| Perfiles | Roles, permisos y alcance por unidad |
| Indicadores | Fórmulas, metas, periodos y visualizaciones |
| Procesos | Etapas, estados, responsables y notificaciones |
| Integraciones | ERP, CRM, SSO, correo, API y bases existentes |
| Reportes | PDF, Excel, fichas y formatos institucionales |
| Infraestructura | Nube administrada o infraestructura del cliente |

Más detalles en [Personalización](docs/PERSONALIZACION.md).

## Modelo de implementación

1. **Diagnóstico:** procesos, fuentes, usuarios y necesidades.
2. **Configuración base:** infraestructura, marca, perfiles y dominios.
3. **Migración:** limpieza, homologación y carga inicial.
4. **Adaptación:** formularios, reglas, indicadores y reportes.
5. **Validación:** pruebas funcionales, permisos y aceptación.
6. **Puesta en marcha:** capacitación, monitoreo y soporte.

## Modalidades

- **Implementación base:** configuración, identidad visual y puesta en marcha.
- **Adaptación institucional:** modelo de datos, formularios, roles e indicadores.
- **Desarrollo especializado:** módulos e integraciones a medida.
- **Continuidad operacional:** soporte, respaldo, monitoreo y evolución.

## Tecnologías

- Next.js, React y TypeScript.
- Django y Python.
- PostgreSQL y Supabase.
- Tailwind CSS.
- Procesamiento de Excel, CSV y archivos tabulares.
- Generación de PDF y notificaciones por correo.
- Despliegue en servicios cloud.

## Estado

Este repositorio presenta un caso de estudio y una propuesta de producto. No contiene el código, datos, marcas, credenciales ni documentación confidencial de la implementación institucional original.

Para convertir la experiencia en un producto distribuible se propone desacoplar las reglas específicas del cliente, crear una configuración por organización y utilizar exclusivamente datos demostrativos.

Consulta:

- [Arquitectura](docs/ARQUITECTURA.md)
- [Módulos](docs/MODULOS.md)
- [Personalización](docs/PERSONALIZACION.md)
- [Seguridad y privacidad](docs/SEGURIDAD-Y-PRIVACIDAD.md)
- [Roadmap de producto](docs/ROADMAP.md)
- [Guía para preparar capturas](images/README.md)
- [Aviso de uso](AVISO-DE-USO.md)

## Autoría y créditos

La implementación institucional fue un trabajo colaborativo. El detalle de responsabilidades, diseño, base inicial y aportes funcionales se encuentra en [Créditos y contribuciones](CREDITOS.md).

Datos de contacto y redes profesionales disponibles en el perfil de GitHub desde el cual se publica este repositorio.

## Aviso de autoría y propiedad

Caso de estudio y documentación de presentación.

Las marcas, datos, diseños, documentos y componentes pertenecientes a terceros no forman parte de este repositorio. La disponibilidad comercial de una implementación debe quedar sujeta a la revisión de los derechos sobre el código y a los acuerdos contractuales correspondientes.

Las capturas se incluyen únicamente para documentar la experiencia y las capacidades de la solución. La marca institucional visible pertenece a su respectivo titular y no forma parte del producto comercial propuesto.
