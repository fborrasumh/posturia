# PosturIA

Libreta visual de sesiones de control postural y tribunal oral de práctica. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/posturia/

**Idiomas:** español (por defecto), valenciano/catalán, inglés, portugués; selector en la barra superior (o `?lang=ca` / `?lang=en` / `?lang=pt` en la URL). El valenciano y el portugués deben revisarlos hablantes nativos antes de publicar.

## Qué hace

Sistema de práctica para el módulo 1153 *Control postural, bienestar y mantenimiento funcional* (CFGS Acondicionamiento Físico), centrado en RA3 (diseñar sesiones) y RA4 (dirigirlas), que suman el 60 % de la nota en la programación.

- **Biblioteca:** 186 ejercicios de los apuntes (UP6-9: movilidad, corrección postural, liberación miofascial, hipopresivos, Pilates, Tai Chi Yang 24 y Yoga), con finalidad, dificultad, página y vídeo de referencia.
- **Libreta (editor según Eva-Lotta Lamm):** figuras de palitos con proporciones 1 : 2,5 : 3, tres vistas, línea base automática, flechas de movimiento, material en azul y notas en rojo; edición arrastrando o con teclado; 2 progresiones y 2 regresiones por ejercicio; exportación SVG, PNG, Word y JSON.
- **Revisión por código** con fuente citada: fases y reparto (apuntes UP3, pág. 72-73), duración, intensidad, progresión de descarga a carga, libreta completa, «repetir al otro lado», anotaciones y adaptaciones.
- **Tribunal oral de práctica:** explicar la sesión, ejercicio al azar o dirigir la sesión. Grabación, audio o texto; el código mide palabras, ritmo, muletillas, ejercicios nombrados y consignas de respiración, seguridad y adaptación.
- **Orientaciones de la IA (opcional):** por criterio, con cita literal que el código verifica; se eliminan frases con notas.
- **Práctica de recuperación** con repaso espaciado (cajas de Leitner), generada por código desde la biblioteca.
- **Progreso** por RA (indicador de práctica, no nota) y **entrega** JSON para el profesorado.
- **Profesorado:** abre entregas, pone nota por instrumento (Taula 7), aplica pesos y redondeo de la Taula 8, exporta CSV y ve el agregado de la clase.

## Para adoptarla en otro centro
Cambia `src/curriculum.js` (RA, CA, pesos, instrumentos, fases y ejercicios) y ejecuta `python3 build.py`.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

Todo se guarda en el navegador (IndexedDB). Solo si se pide sale hacia el proveedor de IA: la grabación para transcribirla (la voz **no se puede anonimizar**), o la transcripción o la sesión con correos, teléfonos, DNI y el nombre enmascarados, tras un aviso previo con muestra. El dictado del navegador (Chrome) envía el audio a Google. La entrega JSON nunca incluye la clave ni las grabaciones.

## Límites

- La IA no pone nota ni valora la demostración corporal, la voz ni el lenguaje no verbal: eso lo observa el profesorado.
- Los RA y CA son un **resumen** del RD 651/2017 (la programación remite al PCCF §8.2): cotéjalos con el texto oficial.
- Las posturas iniciales de cada ejercicio se asignan por palabras clave y son orientativas.
- El análisis oral reconoce los nombres de ejercicios en castellano o en inglés, no en otras lenguas.
- RA1, RA2 y RA5 quedan fuera del alcance de esta versión.
- Los pesos de la Taula 8 suman 90 (RA4 tiene además 10 «FEE»); la app normaliza sobre lo puntuado.
- No es evidencia publicable: para investigar con ella hace falta comité de ética (OEP), consentimiento y RGPD.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Francisco Javier Borrás Rocher (IES Conselleria (València)).

Contenidos, ejercicios y método docente: apuntes «Control Postural, Bienestar y Mantenimiento Funcional» (2026) y programación didáctica del módulo 1153 de Francisco Javier Borrás Rocher y Maite Fabra Blasco. Editor inspirado en la propuesta de dibujo de secuencias de Eva-Lotta Lamm (Yoga Notes).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. y Borrás Rocher, F. J. (2026). *PosturIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

Código: MIT (véase [LICENSE](LICENSE)). Contenidos de los apuntes incluidos en `src/curriculum.js` (textos de ejercicios): CC BY-NC 4.0, con autorización de su autor, F. J. Borrás Rocher (conformidad confirmada el 1-11-2026, junto con la licencia MIT del código).
