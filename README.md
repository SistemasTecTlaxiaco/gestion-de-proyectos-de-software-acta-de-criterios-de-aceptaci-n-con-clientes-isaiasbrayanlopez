# Stellar Community Fund (SCF) – Requisitos y Criterios de Evaluación

## 1. Descripción General del Programa

El **Stellar Community Fund (SCF)** es un programa de subvenciones descentralizadas impulsado por la **Stellar Development Foundation (SDF)**. Su objetivo es financiar proyectos, desarrolladores y startups que agreguen valor significativo a la red **Stellar** y a su plataforma de contratos inteligentes **Soroban**.

---

## 2. Requisitos de Postulación Vigentes

| Requisito | Descripción |
|-----------|-------------|
| **Formulario de Interés** | Todo proyecto debe iniciar completando la solicitud previa en la plataforma oficial disponible en [https://communityfund.stellar.org](https://communityfund.stellar.org). Este formulario verifica elegibilidad técnica y alineación estratégica con la red Stellar. |
| **Integración Esencial de Stellar/Soroban** | El uso de contratos inteligentes en Rust/Soroban o de la red de pagos de Stellar debe ser medular. Se descartan soluciones donde la integración sea superficial o no justificada. |
| **Presupuesto Basado en Hitos en USD y XLM** | Los presupuestos se especifican en dólares estadounidenses pero se desembolsan _on-chain_ en Stellar Lumens (XLM). Los desembolsos se realizan tras la entrega y aprobación comunitaria de cada hito técnico, denominados **Milestones**. |
| **Cumplimiento y Verificación mediante KYC/KYB** | Es obligatorio completar al menos el ochenta por ciento del formulario y aprobar las verificaciones de identidad y cumplimiento legal internacionales. |

---

## 3. Criterios de Evaluación del SCF

| Criterio | Ponderación | Descripción |
|----------|-------------|-------------|
| **Ecosystem Value** | 30% | Evalúa la generación de utilidad real, nuevos usuarios o transacciones dentro de la red Stellar. |
| **Technical Feasibility** | 30% | Analiza la solidez arquitectónica del código WASM y Soroban, así como la viabilidad general del desarrollo propuesto. |
| **Team Capability** | 20% | Valora la experiencia comprobada del equipo en ingeniería blockchain y desarrollo de código abierto. |
| **Value for Money and Milestones** | 20% | Requiere una justificación transparente de costos por cada entregable del _backlog_. |

---

## 4. Fuentes Oficiales Consultadas

| Fuente | Enlace | Fecha de Consulta |
|--------|--------|-------------------|
| Plataforma oficial del SCF | [https://communityfund.stellar.org](https://communityfund.stellar.org) | 28 de agosto de 2026 |
| SCF Handbook | [https://github.com/stellar/scf-handbook](https://github.com/stellar/scf-handbook) | 28 de agosto de 2026 |

---

# Drips Protocol – Streaming de Fondos On-Chain

## 1. ¿Qué es el Streaming de Fondos On-Chain?

El **streaming de fondos on-chain** es un mecanismo financiero descentralizado mediante el cual el capital se transfiere de forma continua, calculada segundo a segundo, desde la billetera del emisor hacia el receptor a través de contratos inteligentes sin custodia.

A diferencia de los desembolsos periódicos tradicionales como los mensuales o trimestrales, el streaming elimina la necesidad de transferencias manuales recurrentes. El saldo del financiador decrece linealmente mientras el del desarrollador aumenta en tiempo real. Esto provee liquidez inmediata para el equipo de desarrollo y otorga al financiador la capacidad de pausar la emisión al instante si detecta un incumplimiento.

---

## 2. Requisitos para Recibir Fondos en Drips

| Requisito | Descripción |
|-----------|-------------|
| **Dirección EVM o Identidad de GitHub Vinculada** | El receptor debe contar con una billetera compatible con la máquina virtual de Ethereum o asociar criptográficamente la cuenta de GitHub del proyecto para reclamar fondos asignados. |
| **Liquidación por Ciclos o _Cycles_** | El protocolo organiza el tiempo en ciclos, siendo el más común el de una semana. Aunque el cálculo de tokens es continuo, los fondos quedan disponibles para su retiro efectivo, denominado _receivable balance_, al finalizar cada ciclo. |
| **Configuración de _Drip Lists_** | Para recibir distribuciones divididas o _splits_, la cuenta o repositorio debe estar incluida en las reglas activas del contrato inteligente. |

---

## 3. Límites y Restricciones Técnicas

| Restricción | Descripción |
|-------------|-------------|
| **Límite de receptores por _Drip List_** | Cada lista de transmisión puede distribuir fondos hacia un máximo de **200** direcciones o repositorios de forma directa. |
| **Agotamiento del Saldo del Emisor** | Si el saldo de la billetera del emisor llega a cero, el flujo se detiene de forma autónoma sin permitir saldos negativos. |
| **Compatibilidad ERC-20 Estándar** | El protocolo solo admite tokens que sigan el estándar ERC-20 básico. No soporta tokens con tarifas por transferencia conocidos como _fee-on-transfer_ ni tokens con rebases dinámicos. |

---

## 4. Fuente Técnica Consultada

| Fuente | Enlace | Fecha de Consulta |
|--------|--------|-------------------|
| Documentación técnica oficial de Drips Protocol | [https://docs.drips.network](https://docs.drips.network) | 28 de agosto de 2026 |

---

# Investigación Técnica – Fuentes Primarias en Inglés

Para garantizar el rigor técnico de este documento, se analizaron de manera directa tres fuentes primarias en inglés:

| Fuente | Descripción |
|--------|-------------|
| **Stellar Community Fund Handbook** | Publicado por la Stellar Development Foundation en 2026. Se analizó en su versión original para estudiar las reglas de elegibilidad de los _Build Awards_ y los requisitos de verificación de hitos. |
| **Drips Protocol v2 Architecture and Smart Contracts** | Publicado por Drips Network en 2026. Se realizó una revisión técnica de los contratos inteligentes en Solidity para comprender el cálculo de tasas por segundo y la amortización de ciclos. |
| **Soroban Smart Contracts** | Publicado por Stellar Developers en 2026. Se estudió el funcionamiento de las interfaces de contratos inteligentes WASM en Rust y su interacción con tokens de la red Stellar. |

---

# Estructura del Repositorio y Documentación

A continuación se detalla la organización de los documentos que componen este repositorio:

| Archivo | Descripción |
|---------|-------------|
| `README.md` | Índice principal, mapa de archivos y matriz de contribuciones de los integrantes. |
| `FINANCIAMIENTO.md` | Análisis completo de requisitos y evaluación del SCF. |
| `DRIPS_PROTOCOL.md` | Desglose técnico de Drips Protocol y streaming _on-chain_. |
| `BACKLOG.md` | Mapeo de fases de desarrollo a los tramos financieros del SCF. |
| `HUECO_HONESTO.md` | Declaración transparente de brechas y cronograma de cierre. |
| `LICENSE` | Licencia abierta MIT que permite el uso y distribución sin restricciones. |

---

# Backlog por Fases Ligado al Financiamiento On-Chain

La solicitud de subvención ante el SCF asciende a un total de **cincuenta mil dólares estadounidenses (USD 50,000)** , que serán desembolsados en **XLM**, y se desglosa en tres tramos financieros vinculados al _backlog_:

| Fase | Descripción | Monto | Justificación |
|------|-------------|-------|---------------|
| **Fase 1: Soroban Smart Contracts Core** | Desarrollo de los contratos de custodia y lógica central en Rust y Soroban con cobertura de pruebas unitarias superior al 90%. | USD 15,000 | Constituye la base crítica de seguridad y lógica de negocio sin la cual no se pueden administrar activos. |
| **Fase 2: Interoperabilidad con Drips y dApp Frontend** | Construcción de los adaptadores de Drips Protocol, interfaz web en React y Next.js, y soporte para Freighter Wallet. | USD 20,000 | Representa el esfuerzo principal de ingeniería de interfaz y conexión entre protocolos. |
| **Fase 3: Auditoría Externa, Pruebas de Carga y Mainnet** | Ejecución de auditoría de ciberseguridad por firma independiente, pruebas de carga con 1000 streams simultáneos y despliegue final en Mainnet. | USD 15,000 | Garantiza que el sistema sea resistente antes de recibir capital del público. |

---

# Declaración de Requisitos Pendientes – El Hueco Honesto

## Brecha Identificada

El proyecto actualmente no cuenta con:
- Una auditoría externa de seguridad independiente realizada por una firma de ciberseguridad sobre los contratos Soroban WASM.
- La conclusión de los experimentos de carga masiva con más de 1000 streams activos en Testnet.

---

## Plan de Mitigación en Tres Pasos

| Paso | Fecha | Actividad |
|------|-------|-----------|
| **1** | 15 de septiembre de 2026 | Ejecución de _fuzzing_ interno intensivo mediante la herramienta `cargo-fuzz`. |
| **2** | 30 de septiembre de 2026 | Pruebas de simulación de estrés en Testnet con 1500 transacciones simultáneas. |
| **3** | 15 de octubre de 2026 | Obtención y publicación del reporte de auditoría externa con calificación de aprobación **PASS**. |

---

## Fecha Estimada de Cierre Completo

La fecha estimada para el cierre completo de todos los requisitos pendientes es el **15 de octubre de 2026**.

---

# Acta de Criterios de Aceptación con Clientes

Para garantizar la satisfacción del cliente y el cumplimiento riguroso de los entregables en cada fase del proyecto, se definen los siguientes criterios de aceptación:

| Criterio | Descripción | Método de Verificación |
|----------|-------------|------------------------|
| **Validación Funcional** | Todos los módulos desarrollados cumplen con las especificaciones técnicas acordadas. | Pruebas unitarias e integrales con cobertura superior al 90%. |
| **Transparencia en Entregas** | Desembolsos y reportes financieros alineados con los hitos aprobados en SCF. | Registro y trazabilidad pública en el explorador de la red Stellar. |
| **Seguridad del Código** | Contratos inteligentes libres de vulnerabilidades críticas o de severidad alta. | Reporte formal emitido por firma auditora externa independiente. |
| **Aprobación del Cliente** | Demostración satisfactoria de las funcionalidades al cliente previo al cierre del hito. | Acta de entrega y recepción firmada por los interesados clave. |

