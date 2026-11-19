# Arquitectura Operativa Universal y Motor de Inteligencia Comercial (Framework G1–G7)

**Autor:** Jean Hernández (Arquitecto de Procesos)

**Estado del Proyecto:** Especificación Arquitectónica Unificada (Versión Consolidada sin Solapamientos) — Búsqueda de Colaboradores Técnicos / Desarrolladores para Construcción de MVP

**Licencia:** GPLv3 / CERN-OHL (Especificación y Arquitectura Abierta; compatible con implementaciones comerciales SaaS bajo esquema de núcleo abierto o dual)

---

## Propósito del Repositorio (Convocatoria de Desarrollo)

Este repositorio contiene los planos lógicos, contratos de datos, fórmulas deterministas y reglas de gobernanza de un **Motor de Decisión Guiado y Autónomo (Business OS)** diseñado para auditar, ordenar, blindar y escalar cualquier actividad económica eliminando el error operativo.

El diseño conceptual y la ingeniería de procesos están cerrados y unificados. **El objetivo actual de este repositorio es conectar con desarrolladores Full-Stack, arquitectos de software, ingenieros de datos o socios técnicos** interesados en traducir esta arquitectura determinista en una aplicación SaaS Multi-Tenant funcional desde su Etapa 1 (MVP: Puertas G1–G3 + Cierre Ejecutivo) hasta escala.

---

## 1. Principios Rectores y Doble Salida de Valor

A diferencia de los planes de negocio estáticos o plantillas que exigen cuestionarios interminables, este sistema opera bajo cuatro principios técnicos obligatorios:

- **Destilación de Datos (Cero Fricción):** Solicita al usuario únicamente la información mínima indispensable de arranque mediante captura reactiva en cascada, resolviendo la complejidad territorial, competitiva y económica en segundo plano.

- **Cero Datos Inventados y Manejo de Incertidumbre:** Ante cualquier dato faltante o respuesta `"No sé este dato aún"`, el motor nunca bloquea el flujo ni fabrica cifras; asigna referencias sectoriales marcadas explícitamente como `PROVISIONAL` o `ESTIMADO` y declara el índice de credibilidad de cada fuente externa (`HIGH`, `MEDIUM`, `APPROXIMATE`).

- **Navegación Modular Viva y Persistencia Continua:** Barra superior/inferior persistente con los 7 módulos (`G1` a `G7`) en estados visuales (`LOCKED`, `IN_PROGRESS`, `COMPLETED`, `PARTIAL`), panel de resumen acumulado en vivo y guardado automático continuo (`debounce 500ms`).

- **Doble Salida de Valor Simultánea:**
  1. **Salida Operativa (Business OS para Negocios):** Guía ejecutiva paso a paso descargable en PDF para fijar márgenes netos, optimizar turnos, controlar mermas, activar canales y escalar sin saturación.
  2. **Salida Analítica (Capa de Inteligencia Territorial y de Mercado):** Subproducto estrictamente agregado y despojado de identidad comercial (`tenant_id`) sobre dinámica zonal, densidad económica, fricciones competitivas y tendencias sectoriales.

---

## 2. Captura Reactiva en Cascada (Cero Fricción)

Para adaptar todo el motor de reglas sin abrumar al usuario, el flujo inicia en **Puerta G1** mediante una cadena de dependencias relacionales (`onChange` / `onSelect`):

1. **Estado Operativo (`operational_mode`):**
   - **Negocio Activo (`ACTIVE_BUSINESS`):** Opera con datos reales y habilita auditoría histórica en etapas posteriores.
   - **Proyecto Nuevo / Pre-Arranque (`PRE_LAUNCH`):** Bloquea métricas históricas inventadas (`operacion_dias == 0`), trabaja con metas/estimaciones y programa cortes de control.

2. **Modalidad Física (`modality_type`):**
   - **Puesto en Calle / Ambulante (`STREET_STALL`):** Oculta renta de local comercial y activa permisos de vía pública y flujo peatonal.
   - **Local Fijo / Changarro (`FIXED_LOCAL`):** Evalúa flujo peatonal, visibilidad a pie de banqueta, estaciones físicas y renta.
   - **Servicio Móvil / A Domicilio (`MOBILE_SERVICE`):** Activa radios de cobertura en km, tiempos de traslado y densidad de demanda por zona.
   - **Operación Multi-Sede (`MULTI_SITE`):** Activa requisición dinámica de personal, turnos múltiples y dimensionamiento multianual.

3. **Nodo de Giro y Taxonomía Dinámica (`industry_node`):**
   - Al elegir un giro (o registrar uno personalizado), el sistema consulta el grafo de dependencias y pre-carga en tiempo real: insumos/materiales, equipamiento, pasos operativos estándar y criterios de filtrado para proveedores zonales.

---

## 3. Arquitectura Central: Los 5 Activos Interdependientes

Todo negocio pierde rentabilidad cuando sus áreas operan aisladas (por ejemplo, lanzar pauta pagada sin validar capacidad efectiva o margen neto). El motor acopla cinco bloques estructurales:

| Grupo de Activo | Componentes Parametrizados | Función Sistémica |
| :--- | :--- | :--- |
| **1. Oferta** | Servicios, productos, paquetes, variaciones de insumos y promociones. | Estandarizar costos directos unitarios, tiempos reales de ejecución y márgenes netos. |
| **2. Capacidad** | Personal, horas-hombre, estaciones físicas o unidades móviles, inventario y horarios. | Detectar el cuello de botella real y subordinar la demanda a la capacidad efectiva. |
| **3. Evidencia** | Portafolio visual, casos de éxito, reseñas verificables y metadatos de permisos. | Sustituir promesas genéricas por activos probatorios clasificados y legalmente auditables. |
| **4. Mercado** | Clientes recurrentes, prospectos, competencia directa/indirecta, proveedores y tendencias. | Detectar oferta descartada, fricciones competitivas, insumos óptimos y patrones de recompra. |
| **5. Entorno** | Infraestructura laboral, vías de acceso, transporte, nodos generadores y flujos horarios. | Capturar demanda contextual mediante cronomarketing basado en movilidad real por franja. |

### Flujo Maestro de Ejecución

`G1 (Contexto y Capacidad Base)` -> `G2 (Territorio y Cronología)` -> `G3 (Economía y Techo CAC)` -> `G4 (Operación Diaria, Evidencia y Captación)` -> `G5 (Atención, Mermas y Auditoría KPI)` -> `G6 (Despliegue Piloto y Validación)` -> `G7 (Plan Maestro, Estrés y Ciclo Quincenal)`

---

## 4. Gobernanza de Implementación: Las 7 Puertas de Decisión (G1–G7)

El sistema prohíbe avanzar a la automatización, pauta o escalamiento si los cimientos operativos y financieros no están validados mediante compuertas secuenciales con contratos de salida tipados:

| Puerta | Nombre Oficial | Alcance Funcional Unificado | Objeto de Salida y Condición de Paso |
| :--- | :--- | :--- | :--- |
| **G1** | Diagnóstico en Cascada y Capacidad Base | Bifurcación (Activo vs. Pre-Arranque), modalidad física, nodo de giro con listas dependientes de insumos/procesos, capital y botón `"No sé este dato aún"`. | `Business_Context_Matrix` con estado, modalidad, insumos, capacidad diaria y costos base (reales o provisionales). |
| **G2** | Inteligencia Territorial y Cronología Viva | Anclaje micro-local, vías alimentadoras, nodos generadores, competencia directa, historial de cierres, cronología horaria y proveedores zonales. | `Territorial_Intelligence_Layer` con flujos horarios, vacíos competitivos, precios zonales y nivel de confianza declarado. |
| **G3** | Arquitectura Comercial y Economía Unitaria | Desambiguación financiera: costo directo real, tarifa recomendable frente a zona, punto de equilibrio, techo máximo de CAC y matriz de ofertas. | `Economic_Unit_Model` con margen protegido, techo de presupuesto de campaña y regla de bloqueo ante venta bajo costo. |
| **G4** | Operación Diaria, Evidencia y Captación | Requisición de equipo (con salto no bloqueante), días fuertes/flojos, blindaje de evidencia/permisos y plan de marketing por franja y nodo. | `Operations_and_Acquisition_Plan` con turnos, inventario de evidencia autorizada y tácticas ajustadas al tope de G3. |
| **G5** | Orquestación de Atención, Mermas y KPIs | Atención modular (Nivel 1 básico / Nivel 2 automatizado + escalado humano), trazabilidad de origen, control de mermas, alzas de insumos y KPIs. | `Audit_and_Traceability_State` (Modo Línea Base si `operacion_dias == 0` o Auditoría Real con semáforo de salud). |
| **G6** | Despliegue Piloto y Validación de Conversión | Ejecución acotada en campo por franjas y canales definidos, medición contra línea base (retención, intención, citas, ventas y CAC real) y ajuste de fugas. | `Pilot_Validation_Report` que acredita conversión dentro del techo de CAC permitido antes de autorizar escalamiento. |
| **G7** | Plan Maestro, Estrés y Ciclo Quincenal | Síntesis ejecutiva en lenguaje directo, activadores de solución alternativa, simulaciones de estrés (+20% a +100%), PDF descargable y bitácora cada 14 días. | `Master_Plan_Snapshot (vN)` ejecutable por fases y actualización de capa analítica territorial anonimizada. |

---

## 5. Fórmulas Deterministas del Motor Lógico (Backend)

Todas las métricas financieras y operativas del núcleo se calculan en servidor mediante fórmulas cerradas con redondeo a dos decimales:

| Variable / Indicador | Fórmula Determinista | Restricción / Regla de Borde |
| :--- | :--- | :--- |
| **Capacidad Efectiva Diaria (`C_ef`)** | `min(capacidad_declarada, (horas_operacion * 60) / ciclo_minutos_unidad)` | Si `ciclo_minutos_unidad == 0`, usar mediana del nodo de G1. |
| **Costo Unitario Total (`CTU`)** | `costo_directo_insumos + (gastos_fijos_mensuales / (C_ef * dias_habiles_mes))` | Si `modality_type == STREET_STALL`, renta comercial = `0`. |
| **Margen Neto Unitario (`MNU`)** | `precio_venta_elegido - CTU` | Si `MNU <= 0`, dispara alerta crítica y bloquea presupuesto de pauta. |
| **Punto de Equilibrio Diario (`PE_d`)** | `ceil((gastos_fijos_mensuales / dias_habiles_mes) / margen_contribucion_unitario)` | Alerta si `PE_d > C_ef` (capacidad instalada insuficiente). |
| **Techo Máximo de CAC (`CAC_max`)** | `MNU * factor_prudencia` (`0.35` en arranque; `0.50` con recompra comprobada) | El presupuesto semanal de captación nunca puede superar el `20%` del capital disponible en G1. |

---

## 6. Arquitectura de Resiliencia e Ingeniería Pre-Lanzamiento

Para garantizar estabilidad en producción y cero fricción para el usuario final, la implementación técnica resuelve cuatro restricciones críticas:

1. **Ingesta Externa Secuencial y Circuit Breakers (Puerta G2):**
   - Pipeline encadenado en secuencia estricta: `Ubicación` -> `Entorno` -> `Competencia` -> `Proveedores`.
   - Si una fuente externa (Google Maps/Places, OpenStreetMap, DENUE/INEGI o reseñas) falla o excede el timeout (`> 4s`), el flujo no se bloquea; asigna un respaldo controlado (por ejemplo, centroide de código postal o captura manual), degrada el índice de confianza (`APPROXIMATE`) y registra el código de error exacto en una **Consola de Diagnóstico Pre-Lanzamiento** (`diagnostic_logs`).

2. **Tolerancia a Saturación y Elasticidad de Carga (Puerta G7):**
   - **Margen de Maniobra (Headroom 3x):** Colas y trabajadores calibrados a **3x** el umbral crítico esperado para absorber simulaciones y picos reales de `+20%` a `+100%` sin latencia perceptible.
   - **Procesamiento Asíncrono:** Ejecución en segundo plano de barridos geoespaciales, cruces horarios y renderizado de PDF ejecutivos.

3. **Aislamiento Multi-Tenant y Privacidad Estricta:**
   - Separación total por `tenant_id` y `project_id` mediante *Row-Level Security (RLS)* en PostgreSQL para costos, márgenes, proveedores y clientes. La capa analítica territorial ingesta únicamente métricas agregadas y anonimizadas.

4. **Desacoplamiento Total entre Motor Lógico (Backend) e Interfaz (UI/UX):**
   - Toda la lógica de dependencias, cálculo de capacidad efectiva, umbrales de alerta (`merma > 5%` amarilla, `> 10%` roja; `alza de insumos > 8%`) y máquina de estados `G1–G7` reside en el servidor. El Frontend expone únicamente captura progresiva y tarjetas de acción clara.

---

## 7. Protocolo de Traducción por Perfil (Qué Se Necesita Construir)

| Interlocutor | Enfoque Principal | Entregables y Reglas del Sistema | Métrica de Éxito |
| :--- | :--- | :--- | :--- |
| **Programador / CTO** | Determinismo lógico, estabilidad y contratos de datos. | Diccionario de variables tipadas (`project_dossier`), fórmulas cerradas, máquina de estados `G1–G7`, aislamiento Multi-Tenant (RLS) y tuberías anonimizadas. | Cero ambigüedad en reglas, baja latencia y ausencia de fallos bloqueantes. |
| **Inversor / Socio** | Escalabilidad, defensibilidad y retorno financiero. | Modelo de doble monetización (Suscripción SaaS B2B + Licenciamiento de Inteligencia Territorial), *Moat* estructural de datos y validación con pilotos reales. | Relación LTV/CAC, retención quincenal de usuarios y margen bruto del software. |
| **Cliente / Operador** | Rentabilidad inmediata, simplicidad y control. | Configuración rápida según modalidad, guía operativa paso a paso en PDF sin tecnicismos, alertas de capacidad y blindaje total de privacidad. | Incremento de margen neto, reducción de merma y eliminación de cuellos de botella. |

---

## 8. Hoja de Ruta de Construcción (De Núcleo a Escala)

- **Etapa 1 — Núcleo Operativo (MVP: Puertas G1–G3 + Cierre Ejecutivo y Exportación PDF):** Implementación de la captura reactiva en cascada (`1A–1D`), pipeline geoespacial y cronología diaria (`2A–2C`), desambiguación financiera y techo de CAC (`3A–3B`), guardado automático (`autosave`) y generación de Plan de Arranque en PDF (`snapshot_v1`).

- **Etapa 2 — Operación Diaria, Evidencia, Atención Modular y Validación Piloto (Puertas G4–G6):** Requisición de equipo con salto no bloqueante (`4A–4C`), clasificación de evidencia con permisos auditables, atención modular Nivel 1/Nivel 2 con escalado humano, control de mermas/alzas de insumos (`5A–5C`) y despliegue piloto con validación en dos niveles (`6A–6B`).

- **Etapa 3 — Resiliencia Avanzada, Ciclo Quincenal e Inteligencia Territorial (Puerta G7 + Doble Salida):** Activación de disparadores de solución alternativa sin cambio de local (`7A`), simulaciones de estrés `+20%` a `+100%` con headroom `3x` (`7B`), bitácora de seguimiento cada 14 días (`7C`) y consolidación anonimizada de datos zonales para la capa analítica de mercado.

---

## Contacto y Colaboración

Si eres desarrollador Full-Stack, ingeniero de datos, arquitecto de software o buscas colaborar en la construcción técnica del MVP bajo esta especificación, abre un *Issue* en este repositorio o contacta directamente al autor a través de GitHub (`@jeanh0`).
