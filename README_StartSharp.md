# 📄 README – Proyecto de Automatización E2E con Serenity BDD (Start Sharp)

## 📌 Descripción del Proyecto

Este proyecto implementa pruebas automatizadas **End-to-End (E2E)** utilizando **Serenity BDD**, aplicando el patrón **Screenplay** y el enfoque **BDD (Behavior Driven Development)**, orientado exclusivamente a validar el flujo de **inicio de sesión** de la aplicación **Start Sharp**.

El objetivo principal es asegurar que los usuarios puedan autenticarse correctamente y acceder al tablero principal del sistema, garantizando la calidad de uno de los flujos más críticos de la aplicación.

---

## 🎯 Objetivos

- Validar el flujo de inicio de sesión exitoso en Start Sharp.
- Asegurar el correcto acceso al tablero principal tras la autenticación.
- Proveer documentación viva mediante escenarios BDD (Gherkin).
- Facilitar la detección temprana de defectos en el proceso de autenticación.

---

## 🧱 Tecnologías Utilizadas

| Tecnología | Versión |
|-----------|---------|
| Java | 11 |
| Serenity BDD | 3.x |
| Selenium WebDriver | Integrado en Serenity |
| Screenplay Pattern | ✅ |
| BDD (Gherkin / Cucumber) | ✅ |
| Gradle / Maven | Según configuración |

---

## 🧠 Arquitectura del Proyecto

El proyecto utiliza el patrón **Screenplay**, el cual promueve una arquitectura limpia y mantenible mediante la separación de responsabilidades:

- **Actors**: Representan a los usuarios del sistema (ej. Pepito).
- **Tasks**: Acciones que realiza el usuario (navegar, iniciar sesión).
- **Questions**: Validaciones del estado de la aplicación.
- **Page Objects (UI / Targets)**: Centralización de los localizadores.

### 📂 Estructura General

```text
src/test
 ├── java
 │   ├── ui            (Page Objects / Targets)
 │   ├── tasks         (Acciones del usuario)
 │   ├── questions     (Validaciones)
 │   ├── steps/runner  (Steps BDD o Runner)
 │
 └── resources
     ├── features      (Escenarios Gherkin)
     └── serenity.conf
```

---

## ✅ Casos de Prueba Automatizados

### 🔐 Inicio de Sesión – Start Sharp

**Característica:** Iniciar sesión en Start Sharp  
**Como** usuario  
**Quiero** iniciar sesión en la página web de Start Sharp

**Escenario: Inicio de sesión exitoso**

```gherkin
Dado Pepito navega a la página de inicio de sesión
Cuando inicia sesión con las credenciales de acceso correctas
Entonces debería ver el tablero en la página principal
```

**Validaciones realizadas:**

- Acceso correcto a la página de inicio de sesión.
- Ingreso exitoso de credenciales válidas.
- Visualización del tablero principal tras la autenticación.

---

## ⚙️ Requisitos Previos

- Java 11 instalado.
- Navegador Google Chrome.
- Gradle o Maven configurado (según el proyecto).

---

## ▶️ Ejecución de Pruebas

### ✅ Con Gradle

```bash
gradle clean test
```

o en Windows:

```bash
gradlew.bat clean test
```

### ✅ Con Maven

```bash
mvn clean verify
```

---

## 📊 Reportes

Serenity genera reportes automáticos al finalizar la ejecución:

- **Gradle:**
```
build/reports/serenity
```

- **Maven:**
```
target/site/serenity/index.html
```

Los reportes incluyen:
- Escenarios ejecutados.
- Pasos detallados.
- Evidencias visuales.
- Resultados de ejecución.

---

## ✅ Buenas Prácticas Implementadas

- Uso del patrón Screenplay.
- Escenarios BDD legibles para negocio.
- Centralización de selectores mediante Page Objects.
- Código reutilizable, desacoplado y mantenible.

---

## 🚀 Escalabilidad y Mejoras Futuras

El proyecto puede extenderse fácilmente para incluir:

- Escenarios negativos (credenciales inválidas).
- Validaciones de seguridad.
- Pruebas Data Driven.
- Integración continua (CI/CD).
- Ejecución en paralelo.

---

## 📈 Conclusión

Este proyecto valida de forma confiable el flujo de autenticación en Start Sharp, proporcionando una base sólida de automatización E2E alineada con buenas prácticas de la industria y adecuada para entornos empresariales.

---

## 👨‍💻 Autor

Proyecto desarrollado como ejercicio de automatización QA con enfoque profesional y empresarial, orientado a la validación del proceso de inicio de sesión en Start Sharp.
