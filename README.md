# 🏥 PROCUMED - Proyecto Cubano de Medicina Digital
<div align="center">
<img src="images/official logo.png" alt="logo PROCUMED" width="250">
</div>

![Build](https://img.shields.io/badge/build-passing-green) [![License: MIT](https://img.shields.io/badge/license-MIT-70D69C)](https://opensource.org/licenses/MIT) 
[![Development Status](https://img.shields.io/badge/status-in%20development-yellow)](https://github.com/your-username/your-repo/labels/status%3A%20in%20development) 

> Transformando el sistema sanitario cubano mediante la digitalización y la interoperabilidad de datos clínicos.

---

## 📌 Descripción del Proyecto

**PROCUMED** es una iniciativa orientada a transformar el manejo de la información médica en Cuba mediante la integración de estándares internacionales como **HL7** y **FHIR**, adaptados al contexto nacional. El objetivo principal es establecer un ecosistema distribuido que conecte hospitales, laboratorios, farmacias y centros de salud, garantizando acceso seguro, estandarizado y soberano a los datos médicos.

Este proyecto representa un paso clave hacia un sistema sanitario más eficiente, seguro y adaptado a las demandas del siglo XXI.

---

## 🧾 Resumen

El **Proyecto Cubano de Medicina Digital (PROCUMED)** busca transformar el sistema sanitario cubano mediante la digitalización y la interoperabilidad de datos clínicos, abordando desafíos como la fragmentación de información, procesos manuales y la falta de integración entre instituciones. Utiliza estándares internacionales como HL7 y FHIR para crear un ecosistema distribuido que conecte hospitales, laboratorios, farmacias y centros de salud, garantizando acceso seguro y soberano a datos médicos.

El proyecto se estructura en seis etapas:

1. Implementación de un servidor FHIR nacional.
2. Adaptación del estándar a las necesidades cubanas (incluyendo recetas electrónicas vinculadas a la cédula de identidad).
3. Integración con sistemas antiguos (HL7 v2).
4. Desarrollo de un sistema clínico distribuido con servidores FHIR autónomos.
5. Pruebas piloto.
6. Plan de escalabilidad.

Para su ejecución, se eligieron tecnologías como **Clojure** (por su eficiencia en sistemas distribuidos y manejo de concurrencia) y **PostgreSQL** (por su capacidad para almacenar recursos FHIR en formato JSONB y sus funciones avanzadas de seguridad).

Los beneficios esperados incluyen reducción de errores médicos, optimización de recursos, mayor control en la dispensación de medicamentos regulados y alineación con tendencias globales en salud digital. Además, se busca eliminar procesos manuales, mejorar la continuidad asistencial y sentar las bases para innovaciones futuras como inteligencia artificial o blockchain.

---

## 🌐 Abstract

The Cuban Digital Medicine Project (**PROCUMED**) seeks to transform the Cuban healthcare system through the digitization and interoperability of clinical data, addressing challenges such as information fragmentation, manual processes and lack of integration between institutions. It uses international standards such as HL7 and FHIR to create a distributed ecosystem that connects hospitals, laboratories, pharmacies and health centers, guaranteeing secure and sovereign access to medical data.

The project is structured in six stages: implementation of a national FHIR server, adaptation of the standard to Cuban needs (including electronic prescriptions linked to the identity card), integration with old systems (HL7 v2), development of a distributed clinical system with autonomous FHIR servers, pilot tests and a scalability plan. Technologies such as Clojure (for its efficiency in distributed systems and concurrency management) and PostgreSQL (for its ability to store FHIR resources in JSONB format and its advanced security features) were chosen for its implementation.

The expected benefits include a reduction in medical errors, optimization of resources, greater control in the dispensing of regulated medications and alignment with global trends in digital health. In addition, it seeks to eliminate manual processes, improve continuity of care and lay the groundwork for future innovations such as artificial intelligence or blockchain.

PROCUMED represents a key step towards a healthcare system that is more efficient, safer and adapted to the demands of the 21st century.

---

## 📚 Palabras Clave / Keywords

- **Español**: Procesamiento de datos médicos; Sistemas de información sanitaria; Estándares HL7; FHIR.
- **English**: Medical data processing; Health information systems; HL7 standards; FHIR.

---

## 🧭 Introducción

La digitalización de los sistemas sanitarios se ha convertido en un pilar fundamental para mejorar la calidad, eficiencia y seguridad en la atención médica a nivel mundial. En Cuba, este proceso enfrenta desafíos significativos derivados de la fragmentación de la información clínica, la falta de interoperabilidad entre instituciones y la dependencia de procesos manuales que limitan la capacidad de respuesta del sistema ante emergencias sanitarias o cambios estructurales.

Estas limitaciones afectan tanto la continuidad asistencial como la planificación epidemiológica, generando oportunidades para la adopción de soluciones tecnológicas innovadoras.

Ante este escenario surge **PROCUMED**, una iniciativa orientada a transformar el manejo de la información médica mediante la integración de estándares internacionales reconocidos, como **HL7** y **FHIR**, y adaptados al contexto nacional.

El proyecto busca establecer una base técnica y operativa para la interoperabilidad entre hospitales, laboratorios, farmacias y centros de salud, garantizando el acceso seguro y estandarizado a datos clínicos sin comprometer la soberanía de los mismos.

---

## 🛠️ Métodos o Metodología Computacional

### Exploración de Soluciones Existentes: XAVIA HIS

Durante el proceso de investigación nos encontramos con un sistema relacionado con algunos de los objetivos fijados por PROCUMED. Su nombre es **XAVIA HIS** (*Hospital Information System*) y su evolución e implementación están lideradas actualmente por el Centro de Informática Médica (CESIM).

XAVIA HIS representa un esfuerzo valioso en la digitalización del sistema sanitario cubano, pero presenta limitaciones técnicas y funcionales que restringen su utilidad a nivel nacional:

- Arquitectura centralizada incompatible con la interoperabilidad entre instituciones.
- Uso del estándar HL7 CDA, orientado a documentos clínicos estáticos.
- No permite acceso remoto a datos médicos por parte de pacientes o profesionales fuera del entorno hospitalario.
- Falta de estrategias claras de seguridad ni protocolos de autenticación avanzada.

---

## 🧬 El Mejor Estándar para el Intercambio de Datos Médicos: FHIR

**FHIR** (*Fast Healthcare Interoperability Resources*) es un estándar de interoperabilidad para el intercambio de información de salud digital, y es el núcleo del Proyecto Cubano de Medicina Digital.

Se seleccionó **FHIR** por:

- Capacidad para garantizar interoperabilidad efectiva.
- APIs RESTful y formatos modernos (JSON/XML).
- Enfoque modular basado en recursos reutilizables.
- Adopción masiva en proyectos globales como Google Cloud Healthcare API, Apple Health y European Health Data Space.

---

## 📅 Etapas del Proyecto

### Etapa 1: Implementación de un Servidor FHIR Nacional

- Establecimiento de un servidor FHIR base adaptado al contexto cubano.
- Herramientas: HAPI FHIR Server u OpenFHIR.
- Recursos básicos: `Patient`, `MedicationRequest`, `ServiceRequest`.
- Integración del número de cédula como identificador único.

### Etapa 2: Adaptación del Estándar a la Realidad Sanitaria Cubana

- Definición de perfiles FHIR locales.
- Validación cruzada de recetas electrónicas vinculadas a medicamentos regulados.
- Integración con el sistema nacional de identidad digital.

### Etapa 3: Integración con Sistemas Legacy usando HL7 v2

- Adaptadores HL7 v2 → FHIR.
- Herramientas: Mirth Connect o Caristix.

### Etapa 4: Desarrollo de un Sistema Clínico Distribuido

- Múltiples servidores FHIR autónomos por institución.
- APIs RESTful + OAuth 2.0 + SMART on FHIR para acceso seguro.

### Etapa 5: Validación y Pruebas Piloto

- Pruebas funcionales en hospitales y farmacias seleccionadas.
- Recolección de retroalimentación de usuarios reales.

### Etapa 6: Documentación Técnica y Plan de Escalabilidad

- Guías completas de instalación, configuración y uso.
- Estrategia de expansión gradual a nivel nacional.

---

## 💡 Elección de Tecnologías: Clojure + PostgreSQL

### Clojure

- Lenguaje funcional sobre JVM.
- Ideal para sistemas distribuidos y concurrencia segura.
- Soporte poderoso para herramientas FHIR como HAPI FHIR.
- Código abierto y compatible con infraestructuras locales.

### PostgreSQL

- Almacenamiento eficiente de recursos FHIR en formato JSONB.
- Transacciones ACID y consultas complejas.
- Funcionalidades avanzadas de seguridad.
- Código abierto, reforzando la autonomía tecnológica nacional.

---

## ✅ Resultados Esperados

La aplicación de PROCUMED tendrá un impacto transformador en múltiples dimensiones del sistema sanitario cubano, destacándose:

1. **Mejora de la atención médica**: Acceso en tiempo real a datos clínicos completos.
2. **Fortalecimiento del control de medicamentos estratégicos**: Validación automática de dispensación.
3. **Modernización del sistema informático sanitario**: Alineación con tendencias internacionales.
4. **Reducción de la dependencia de procesos manuales**: Eliminación de documentos físicos.

---

## 🎯 Conclusiones

PROCUMED no solo mejorará la calidad de la atención médica y la eficiencia operativa, sino que también establecerá una base técnica para futuras innovaciones, como análisis epidemiológico automatizado, trazabilidad de medicamentos mediante blockchain y apoyo clínico con inteligencia artificial.

Este proyecto tiene el potencial de transformar estructuralmente el sistema sanitario cubano.
---
## 👤 Autor

**Samuel Carriles Baños**  
[Correo de contacto](mailto:samuelcarrilesbanos@gmail.com)  
[ORCID](https://orcid.org/0009-0003-2084-0357)  
Universidad de las Ciencias Informáticas, La Habana, Cuba.

---
# 🏥 PROCUMED - Proyecto Cubano de Medicina Digital

![Build](https://img.shields.io/badge/build-passing-green) [![License: MIT](https://img.shields.io/badge/license-MIT-70D69C)](https://opensource.org/licenses/MIT) 
[![Development Status](https://img.shields.io/badge/status-in%20development-yellow)](https://github.com/your-username/your-repo/labels/status%3A%20in%20development) 

> Transformando el sistema sanitario cubano mediante la digitalización y la interoperabilidad de datos clínicos.

---

## 📌 Descripción del Proyecto

**PROCUMED** es una iniciativa orientada a transformar el manejo de la información médica en Cuba mediante la integración de estándares internacionales como **HL7** y **FHIR**, adaptados al contexto nacional. El objetivo principal es establecer un ecosistema distribuido que conecte hospitales, laboratorios, farmacias y centros de salud, garantizando acceso seguro, estandarizado y soberano a los datos médicos.

Este proyecto representa un paso clave hacia un sistema sanitario más eficiente, seguro y adaptado a las demandas del siglo XXI.

---

## 🧾 Resumen

El **Proyecto Cubano de Medicina Digital (PROCUMED)** busca transformar el sistema sanitario cubano mediante la digitalización y la interoperabilidad de datos clínicos, abordando desafíos como la fragmentación de información, procesos manuales y la falta de integración entre instituciones. Utiliza estándares internacionales como HL7 y FHIR para crear un ecosistema distribuido que conecte hospitales, laboratorios, farmacias y centros de salud, garantizando acceso seguro y soberano a datos médicos.

El proyecto se estructura en seis etapas:

1. Implementación de un servidor FHIR nacional.
2. Adaptación del estándar a las necesidades cubanas (incluyendo recetas electrónicas vinculadas a la cédula de identidad).
3. Integración con sistemas antiguos (HL7 v2).
4. Desarrollo de un sistema clínico distribuido con servidores FHIR autónomos.
5. Pruebas piloto.
6. Plan de escalabilidad.

Para su ejecución, se eligieron tecnologías como **Clojure** (por su eficiencia en sistemas distribuidos y manejo de concurrencia) y **PostgreSQL** (por su capacidad para almacenar recursos FHIR en formato JSONB y sus funciones avanzadas de seguridad).

Los beneficios esperados incluyen reducción de errores médicos, optimización de recursos, mayor control en la dispensación de medicamentos regulados y alineación con tendencias globales en salud digital. Además, se busca eliminar procesos manuales, mejorar la continuidad asistencial y sentar las bases para innovaciones futuras como inteligencia artificial o blockchain.

---

## 🌐 Abstract

The Cuban Digital Medicine Project (**PROCUMED**) seeks to transform the Cuban healthcare system through the digitization and interoperability of clinical data, addressing challenges such as information fragmentation, manual processes and lack of integration between institutions. It uses international standards such as HL7 and FHIR to create a distributed ecosystem that connects hospitals, laboratories, pharmacies and health centers, guaranteeing secure and sovereign access to medical data.

The project is structured in six stages: implementation of a national FHIR server, adaptation of the standard to Cuban needs (including electronic prescriptions linked to the identity card), integration with old systems (HL7 v2), development of a distributed clinical system with autonomous FHIR servers, pilot tests and a scalability plan. Technologies such as Clojure (for its efficiency in distributed systems and concurrency management) and PostgreSQL (for its ability to store FHIR resources in JSONB format and its advanced security features) were chosen for its implementation.

The expected benefits include a reduction in medical errors, optimization of resources, greater control in the dispensing of regulated medications and alignment with global trends in digital health. In addition, it seeks to eliminate manual processes, improve continuity of care and lay the groundwork for future innovations such as artificial intelligence or blockchain.

PROCUMED represents a key step towards a healthcare system that is more efficient, safer and adapted to the demands of the 21st century.

---

## 📚 Palabras Clave / Keywords

- **Español**: Procesamiento de datos médicos; Sistemas de información sanitaria; Estándares HL7; FHIR.
- **English**: Medical data processing; Health information systems; HL7 standards; FHIR.

---

## 🧭 Introducción

La digitalización de los sistemas sanitarios se ha convertido en un pilar fundamental para mejorar la calidad, eficiencia y seguridad en la atención médica a nivel mundial. En Cuba, este proceso enfrenta desafíos significativos derivados de la fragmentación de la información clínica, la falta de interoperabilidad entre instituciones y la dependencia de procesos manuales que limitan la capacidad de respuesta del sistema ante emergencias sanitarias o cambios estructurales.

Estas limitaciones afectan tanto la continuidad asistencial como la planificación epidemiológica, generando oportunidades para la adopción de soluciones tecnológicas innovadoras.

Ante este escenario surge **PROCUMED**, una iniciativa orientada a transformar el manejo de la información médica mediante la integración de estándares internacionales reconocidos, como **HL7** y **FHIR**, y adaptados al contexto nacional.

El proyecto busca establecer una base técnica y operativa para la interoperabilidad entre hospitales, laboratorios, farmacias y centros de salud, garantizando el acceso seguro y estandarizado a datos clínicos sin comprometer la soberanía de los mismos.

---

## 🛠️ Métodos o Metodología Computacional

### Exploración de Soluciones Existentes: XAVIA HIS

Durante el proceso de investigación nos encontramos con un sistema relacionado con algunos de los objetivos fijados por PROCUMED. Su nombre es **XAVIA HIS** (*Hospital Information System*) y su evolución e implementación están lideradas actualmente por el Centro de Informática Médica (CESIM).

XAVIA HIS representa un esfuerzo valioso en la digitalización del sistema sanitario cubano, pero presenta limitaciones técnicas y funcionales que restringen su utilidad a nivel nacional:

- Arquitectura centralizada incompatible con la interoperabilidad entre instituciones.
- Uso del estándar HL7 CDA, orientado a documentos clínicos estáticos.
- No permite acceso remoto a datos médicos por parte de pacientes o profesionales fuera del entorno hospitalario.
- Falta de estrategias claras de seguridad ni protocolos de autenticación avanzada.

---

## 🧬 El Mejor Estándar para el Intercambio de Datos Médicos: FHIR

**FHIR** (*Fast Healthcare Interoperability Resources*) es un estándar de interoperabilidad para el intercambio de información de salud digital, y es el núcleo del Proyecto Cubano de Medicina Digital.

Se seleccionó **FHIR** por:

- Capacidad para garantizar interoperabilidad efectiva.
- APIs RESTful y formatos modernos (JSON/XML).
- Enfoque modular basado en recursos reutilizables.
- Adopción masiva en proyectos globales como Google Cloud Healthcare API, Apple Health y European Health Data Space.

---

## 📅 Etapas del Proyecto

### Etapa 1: Implementación de un Servidor FHIR Nacional

- Establecimiento de un servidor FHIR base adaptado al contexto cubano.
- Herramientas: HAPI FHIR Server u OpenFHIR.
- Recursos básicos: `Patient`, `MedicationRequest`, `ServiceRequest`.
- Integración del número de cédula como identificador único.

### Etapa 2: Adaptación del Estándar a la Realidad Sanitaria Cubana

- Definición de perfiles FHIR locales.
- Validación cruzada de recetas electrónicas vinculadas a medicamentos regulados.
- Integración con el sistema nacional de identidad digital.

### Etapa 3: Integración con Sistemas Legacy usando HL7 v2

- Adaptadores HL7 v2 → FHIR.
- Herramientas: Mirth Connect o Caristix.

### Etapa 4: Desarrollo de un Sistema Clínico Distribuido

- Múltiples servidores FHIR autónomos por institución.
- APIs RESTful + OAuth 2.0 + SMART on FHIR para acceso seguro.

### Etapa 5: Validación y Pruebas Piloto

- Pruebas funcionales en hospitales y farmacias seleccionadas.
- Recolección de retroalimentación de usuarios reales.

### Etapa 6: Documentación Técnica y Plan de Escalabilidad

- Guías completas de instalación, configuración y uso.
- Estrategia de expansión gradual a nivel nacional.

---

## 💡 Elección de Tecnologías: Clojure + PostgreSQL

### Clojure

- Lenguaje funcional sobre JVM.
- Ideal para sistemas distribuidos y concurrencia segura.
- Soporte poderoso para herramientas FHIR como HAPI FHIR.
- Código abierto y compatible con infraestructuras locales.

### PostgreSQL

- Almacenamiento eficiente de recursos FHIR en formato JSONB.
- Transacciones ACID y consultas complejas.
- Funcionalidades avanzadas de seguridad.
- Código abierto, reforzando la autonomía tecnológica nacional.

---

## ✅ Resultados Esperados

La aplicación de PROCUMED tendrá un impacto transformador en múltiples dimensiones del sistema sanitario cubano, destacándose:

1. **Mejora de la atención médica**: Acceso en tiempo real a datos clínicos completos.
2. **Fortalecimiento del control de medicamentos estratégicos**: Validación automática de dispensación.
3. **Modernización del sistema informático sanitario**: Alineación con tendencias internacionales.
4. **Reducción de la dependencia de procesos manuales**: Eliminación de documentos físicos.

---

## 🎯 Conclusiones

PROCUMED no solo mejorará la calidad de la atención médica y la eficiencia operativa, sino que también establecerá una base técnica para futuras innovaciones, como análisis epidemiológico automatizado, trazabilidad de medicamentos mediante blockchain y apoyo clínico con inteligencia artificial.

Este proyecto tiene el potencial de transformar estructuralmente el sistema sanitario cubano.
---
## 👤 Autor

**Samuel Carriles Baños**  
[Correo de contacto](mailto:samuelcarrilesbanos@gmail.com)  
[ORCID](https://orcid.org/0009-0003-2084-0357)  
Universidad de las Ciencias Informáticas, La Habana, Cuba.

---


[def]: mage