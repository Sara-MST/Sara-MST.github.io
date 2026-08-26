# [Tu Nombre Completo]

![Logo](assets/img/logo.png)

¡Hola! Soy médica con formación en epidemiología y análisis de datos. Bienvenido/a a mi portafolio de proyectos.

[Ver mi perfil de GitHub](https://github.com/TU-USUARIO) · [LinkedIn](https://www.linkedin.com/in/TU-USUARIO/)

---

## Acerca de mí

Médica con diplomado en epidemiología y formación certificada en análisis de datos (Python, SQL, estadística aplicada). Combino el pensamiento clínico y epidemiológico —lectura crítica de evidencia, diseño de estudios, comprensión de terminología médica y regulatoria— con herramientas de analítica moderna para convertir datos complejos en decisiones de negocio.

Me interesa aportar esta doble mirada (salud + datos) a equipos de **real-world evidence, market access, asuntos médicos, farmacovigilancia, business analytics o customer insights** en la industria farmacéutica y de salud, aunque mi perfil también encaja en cualquier equipo que necesite traducir datos en decisiones: retail, telecomunicaciones, fintech o e-commerce.

### Habilidades técnicas

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `SciPy` `Statsmodels` `SQL` `SQLAlchemy` `Excel`

- Limpieza, transformación y análisis exploratorio de datos (EDA)
- Pruebas de hipótesis: t-test, Mann-Whitney, Shapiro-Wilk, corrección de Bonferroni
- Diseño y análisis de experimentos A/B
- Consultas SQL con joins múltiples, agregaciones y subconsultas

### Habilidades de dominio (mi diferencial)

- Formación médica y epidemiológica: diseño de estudios, causalidad, lectura crítica de evidencia
- Comprensión de terminología clínica y regulatoria
- Capacidad de traducir hallazgos técnicos en recomendaciones claras para audiencias no técnicas

### Habilidades blandas

Pensamiento analítico | Resolución de problemas | Comunicación efectiva | Rigor científico | Orientación a resultados | Atención al detalle

---

## Proyectos seleccionados

## 1. Identificación de operadores ineficientes en un centro de contacto

Un centro de contacto (call center) necesitaba identificar de forma objetiva qué operadores tenían un desempeño por debajo del estándar, para poder priorizar acciones de mejora sin depender de percepciones subjetivas. Este tipo de análisis es directamente aplicable a **líneas de atención al paciente, programas de adherencia terapéutica o farmacovigilancia**, donde la calidad de la atención telefónica impacta directamente los resultados en salud.

#### Herramientas y tipo de proyecto

`Python` `Pandas` `SciPy (Shapiro-Wilk, Mann-Whitney)` `Seaborn` `Análisis de datos` `Pruebas de hipótesis` `Indicadores de desempeño (KPI)`

### Preguntas clave

1. ¿Qué indicadores permiten distinguir objetivamente a un operador ineficaz de uno eficiente?
2. ¿Existe una diferencia estadísticamente significativa en el tiempo de espera entre ambos grupos?
3. ¿Qué patrones de comportamiento comparten los operadores de bajo desempeño?

### Metodología

- **Preprocesamiento:** limpieza de 53,902 registros de llamadas de 45,730 operadores (ago–nov 2019), tratamiento de duplicados y valores nulos en `operator_id`.
- **Construcción de indicadores:** tabla resumen por operador con número de llamadas atendidas, tasa de llamadas perdidas, tiempo promedio de espera y duración promedio de llamada.
- **Pruebas de hipótesis:** prueba de normalidad (Shapiro-Wilk) y, al no cumplirse el supuesto, prueba no paramétrica de Mann-Whitney para comparar tiempos de espera entre operadores eficientes e ineficaces.

### Conclusiones y recomendaciones

- Se desarrolló una metodología objetiva para identificar operadores potencialmente ineficaces combinando tasa de llamadas perdidas, tiempo promedio de espera y volumen de llamadas salientes.
- Las pruebas estadísticas confirmaron diferencias significativas entre operadores eficientes e ineficaces, validando la utilidad de estos indicadores.
- **Recomendaciones:** implementar un dashboard de monitoreo para supervisores, generar alertas automáticas al superar umbrales críticos, y usar la clasificación como herramienta de seguimiento —no como única medida de evaluación— complementándola con indicadores de calidad.

**[Explora el repositorio completo →](https://github.com/TU-USUARIO/nombre-del-repo)**

---

## 2. Test A/B de un embudo de conversión

Evaluación de un nuevo sistema de recomendaciones mediante un experimento A/B, analizando el embudo de conversión desde el login hasta la compra. Este tipo de diseño experimental es el mismo que se usa para **medir el impacto de campañas de educación al paciente, programas de soporte o cambios en canales digitales de salud**.

#### Herramientas y tipo de proyecto

`Python` `Pandas` `SciPy` `Statsmodels (proportions_ztest)` `Tests A/B` `Análisis de embudo` `Corrección de Bonferroni`

### Preguntas clave

1. ¿En qué etapa del embudo se pierde más usuarios?
2. ¿El nuevo sistema de recomendaciones cambia el comportamiento de navegación?
3. ¿Esas diferencias se traducen en más compras?

### Metodología

- Verificación de la correcta asignación aleatoria de ~14,500 usuarios a los grupos A/B (sin solapamiento entre grupos).
- Construcción del embudo: login → página de producto → carrito → compra.
- Pruebas de proporciones por cada etapa del embudo, con **corrección de Bonferroni** al comparar cuatro eventos simultáneamente.

### Conclusiones y recomendaciones

- El embudo muestra una caída progresiva de usuarios en cada etapa; solo una fracción llega hasta la compra.
- La única diferencia estadísticamente significativa entre grupos ocurrió en la etapa de "página de producto": el nuevo sistema modifica el comportamiento inicial de navegación, **pero no genera un aumento significativo en las compras**.
- **Recomendación:** no implementar el cambio a escala completa; el efecto observado no justifica el costo sin evidencia de impacto en la conversión final.

**[Explora el repositorio completo →](https://github.com/TU-USUARIO/nombre-del-repo)**

---

## 3. Segmentación de mercado global — Tienda de videojuegos

Análisis de ventas de videojuegos por plataforma, género y región (EE. UU., Europa, Japón) para identificar patrones de mercado y evaluar diferencias de percepción de usuarios entre plataformas. La lógica es la misma que aplica a un **análisis de mercado farmacéutico multi-país**: lo que funciona en una región no necesariamente aplica en otra.

#### Herramientas y tipo de proyecto

`Python` `Pandas` `NumPy` `SciPy` `Segmentación de mercado` `Pruebas de hipótesis (t-test)` `Visualización de datos`

### Preguntas clave

1. ¿Qué plataformas y géneros dominan las ventas en cada región?
2. ¿Difieren los patrones de consumo entre EE. UU., Europa y Japón?
3. ¿Existe diferencia estadísticamente significativa en la calificación de usuarios entre géneros o plataformas?

### Metodología

- Filtrado a un período relevante (ciclo de vida promedio de una plataforma) para evitar sesgos históricos.
- Perfil de usuario por región: plataformas y géneros preferidos.
- Pruebas t de Student para comparar calificaciones promedio entre plataformas (Xbox One vs. PC) y entre géneros (Acción vs. Deportes).

### Conclusiones y recomendaciones

- Japón muestra un comportamiento de consumo claramente distinto a EE. UU. y Europa, lo que sugiere que **una sola estrategia global no es óptima** y se justifican reglas o modelos diferenciados por región.
- Los géneros Acción y Disparos concentran la mayor rentabilidad; clasificaciones como "Mature" y "Everyone" impactan las ventas de forma distinta según la región.
- **Recomendación:** diseñar estrategias comerciales segmentadas por región en lugar de una aproximación única para todos los mercados.

**[Explora el repositorio completo →](https://github.com/TU-USUARIO/nombre-del-repo)**

---

## 4. Análisis SQL — Base de datos de un servicio de lectura

Exploración de una base de datos relacional (libros, autores, editoriales, reseñas y calificaciones) mediante consultas SQL para generar información de producto orientada a usuarios lectores.

#### Herramientas y tipo de proyecto

`SQL` `SQLAlchemy` `Python` `Pandas` `Consultas con joins y agregaciones`

### Preguntas clave

1. ¿Cuántos libros se publicaron después del año 2000?
2. ¿Qué editorial publica más libros de alto volumen (+50 páginas)?
3. ¿Qué autor tiene la mejor calificación promedio entre libros con al menos 50 calificaciones?
4. ¿Cómo se comportan los usuarios más activos al calificar y reseñar?

### Conclusiones destacadas

- Se identificaron 819 libros publicados después del 1 de enero de 2000.
- Entre los autores con libros de al menos 50 calificaciones, J.K. Rowling / Mary GrandPré lidera con un promedio de 4.29.
- Los usuarios que califican más de 50 libros escriben en promedio 24.33 reseñas de texto: **califican más de lo que escriben**, un patrón relevante para diseñar estrategias de engagement.

**[Explora el repositorio completo →](https://github.com/TU-USUARIO/nombre-del-repo)**

---

Hosted on GitHub Pages
