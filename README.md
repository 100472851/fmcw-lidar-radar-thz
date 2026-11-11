# Análisis de detección coherente FMCW: del LiDAR al radar fotónico THz

Trabajo de la asignatura **Fotónica** (Grado en Ingeniería de Tecnologías de Telecomunicación, UC3M, curso 2025/26).

**Autores:** Jacobo Gutiérrez Pérez-España y Diego de Andrés Casanova
**Profesores:** Guillermo Carpintero del Barrio y Horacio Lamela Rivera

## El problema

En la aproximación final de un eVTOL (taxi aéreo eléctrico de despegue vertical), los rotores levantan nubes de polvo (*brownout*) que dejan sin visibilidad a la tripulación y ciegan a los sensores ópticos. Los últimos 100 metros son la fase más crítica del vuelo.

## La propuesta

Una arquitectura fotónica **híbrida FMCW** (onda continua con modulación de frecuencia) con dos sensores complementarios:

- **LiDAR FMCW a 1550 nm** con láser VCSEL, sin escaneo mecánico, como sensor principal de alta definición en condiciones despejadas.
- **Radar fotónico a 1,65 THz** generado por *photomixing* coherente de diodos láser, como sistema de respaldo cuando el polvo bloquea el haz óptico.

## Resultados del análisis

- **Propagación:** con partículas de 1 a 100 µm, el LiDAR a 1550 nm cae en el régimen de **dispersión de Mie** y queda bloqueado. El radar THz (λ ≈ 181 µm) pasa al régimen de **Rayleigh** y la atenuación se reduce drásticamente.
- **Resolución:** el ancho de banda de 1,65 THz da una resolución espacial teórica de **~90 µm**, frente a los **1,5 mm** del LiDAR FMCW convencional.
- **Ruido:** con un oscilador local de alta potencia, la detección homodina sitúa a ambos sensores en el **límite de ruido de disparo** (*shot-noise limit*), de modo que la SNR no depende del ruido térmico de la electrónica y se pueden detectar ecos de fracciones de picovatio.

## Contenido

| Fichero | Qué es |
|---|---|
| [`docs/informe.pdf`](docs/informe.pdf) | Informe completo (30 páginas): motivación, diseño, modelado de la propagación, balance de potencias, cálculos comparativos, conclusiones y trabajo futuro |
| [`docs/presentacion.pdf`](docs/presentacion.pdf) | Diapositivas de la defensa |
| [`index.html`](index.html) | Versión web de la presentación (se navega con ← →). Con GitHub Pages activado se ve directamente en el navegador |
