# Lowganma: portafolio y Proyecto Vinland

## Objetivo de esta versión

Visitantes: pequeños comercios y personas que necesitan soporte, clientes del cyber y posibles colaboradores de Vinland.
Flujo: entender la oferta → explorar proyectos o servicios → preparar una consulta por WhatsApp o correo.

Se incorpora una página independiente `portafolio-vinland.html`. La portada `index.html`, sus páginas, archivos y licencias se conservan sin modificaciones. No se ha publicado ni fusionado la propuesta.

Repositorio: `Lowganma/Lowganma.github.io`.
Base revisada: `main`, commit `2eaaeda86ca18317def334c8f7ef36cef6f84138`.
Rama de propuesta: `portfolio/vinland-preview-20261104`.
Entorno: espacio temporal de trabajo; lectura y escritura remota mediante la integración GitHub, sin clonar ni modificar otros repositorios.
No se encontraron archivos AGENTS.md en el árbol revisado del portafolio.

## Cómo revisar

Descargar `portafolio-vinland.html` y abrirlo con un navegador. Todo el CSS, JavaScript y gráficos vectoriales están incluidos en ese archivo. No requiere instalación, paquetes, claves, base de datos ni fuentes externas. Los enlaces a GitHub, WhatsApp y correo requieren sus servicios respectivos.

También puede servirse con `python3 -m http.server 8000` desde la carpeta del archivo y abrir `http://localhost:8000/portafolio-vinland.html`.

## Implementación

- Fondo #121212, verde #00FF66, acentos naranja, estilo terminal y gráfico de tecnología/naturaleza.
- Navegación por secciones, menú móvil, enlaces para saltar contenido y foco visible.
- Inventario Django, Overlord y Vinland con estados explícitos.
- Servicios profesionales y servicios presenciales del cyber.
- Manifiesto, cuatro lecturas iniciales en ventanas de diálogo, FAQ y propuesta de comunidad.
- Contacto mediante correo y WhatsApp encontrados en el portafolio existente. Confirmar vigencia antes de publicación definitiva.
- Formulario que prepara texto mediante encodeURIComponent y abre WhatsApp. No envía automáticamente, no almacena datos y no usa un servidor.
- Sin dependencias externas, rastreadores, pagos ni servicio contratado.

Las ilustraciones de proyectos son conceptuales. No se presentan como capturas o demos reales. Overlord no expone código ni assets del repositorio privado. Vinland se presenta como propuesta, sin inventar miembros, actividad o testimonios.

## Validación y aceptación

Comprobación estática de identificadores, anclas, destinos de las lecturas, atributos de seguridad de enlaces y sintaxis JavaScript con `node --check`. Se revisaron reglas CSS para móvil y preferencia de movimiento reducido en el código.

Limitación: el navegador disponible no pudo acceder al servidor local (ERR_CONNECTION_REFUSED). No se completó la comprobación visual ni la interacción real en móvil/escritorio. No se ha enviado ningún mensaje de prueba.

Antes de publicar, revisar en navegador:

1. Sin desbordamiento horizontal a 375 px y 1440 px; texto y botones legibles.
2. Menú abre/cierra; enlaces navegan a sus secciones.
3. Las seis lecturas abren y cierran con botón y Escape, y devuelven el foco al control de origen.
4. Las FAQ funcionan con teclado.
5. Formulario rechaza campos vacíos o solo espacios; acentos, símbolos y saltos de línea llegan correctamente al borrador de WhatsApp, sin enviarlo.
6. Confirmar correo, teléfono, nombre público, ciudad, dirección y horarios del cyber.
7. Añadir enlace real de Telegram cuando el propietario lo facilite. Actualmente figura pendiente y se ofrece correo como alternativa.

## Revisión de GitHub (4 de noviembre de 2026)

Se localizaron 17 repositorios accesibles. Esta es una revisión de organización, documentación y archivos seleccionados, no una auditoría completa ni una ejecución de los proyectos.

| Repositorio o grupo | Hallazgo y recomendación |
| --- | --- |
| Lowganma.github.io | Ya contiene el portafolio estático. Usarlo como portada principal evita mantener dos vitrinas distintas. La versión previa contiene enlaces `#`, dos correos diferentes y referencias a imágenes ausentes del árbol, como la portada de Achantes y el GIF de ventas. Esta propuesta independiente evita reutilizar esos destinos. |
| Portafolio | Tiene configuración Vite/TypeScript y README sin descripción. Definir si es un experimento o reemplazo antes de mantener ambas versiones. |
| Inventario_v1 | Es el candidato Django documentado. Arreglar instalación y verificar funciones antes de destacarlo como demo ejecutable. El README empieza con un bloque Markdown mal delimitado y el comando git clone contiene sintaxis de enlace Markdown. |
| Inventario-Pro | README genérico React/Vite. Reemplazar con problema, alcance, estado, capturas, instalación y diferencias frente a Inventario_v1. No asumir que es el mismo backend. |
| inventarios-seccion-configuracion, inventario-web, inventario-2.0 | Elegir una versión canónica tras comparar historia y funciones. Documentar cuáles son antecedentes. No borrar basándose solo en los nombres. |
| Overlord_prototipo | Privado. Preparar caso de estudio con contribución propia y material autorizado para publicación. No hace falta volver público el código para incluir el proyecto. |
| overlord_roto_reference | Privado. Mantener como referencia si es necesario para el trabajo; no destacarlo como entrega terminada. |
| curso-git, practicas, proyecto-python | Pueden permanecer como aprendizaje. Añadir una descripción clara y archivar solo los que ya no se mantengan. No se evaluó su código completo. |
| achantes, sala_virtual, manitos, gym, ikigai | Decidir si aportan a la selección principal. No es necesario mostrar todos los repositorios en la landing. |

No se borraron, archivaron ni cambiaron permisos de repositorios. Recomendación: seleccionar 3–4 proyectos representativos y ordenar la documentación; conservar el historial de aprendizaje.

## Inventario Django: preparación de una demo real

Archivos revisados en Inventario_v1: README.md, requirements.txt, inventario/settings.py, Dockerfile, compose.yaml y docker-entrypoint.sh.

Bloqueo confirmado: requirements.txt contiene marcadores `<<<<<<<`, `=======` y `>>>>>>>`, además de `pyllow` en una de las alternativas. No es una lista instalable de dependencias. El README también requiere limpieza.

Existe preparación con Docker, Gunicorn, WhiteNoise, SQLite y variables de entorno. Esto no prueba que la aplicación arranque ni que esté lista para Internet. No se ejecutó Django ni se modificó su repositorio en esta tarea.

Siguiente etapa:

1. Resolver dependencias y comprobar compatibilidad de las versiones antes de instalarlas. Revisar soporte vigente de Django (el proyecto fija 4.1.7).
2. Instalar y ejecutar migraciones, pruebas y `manage.py check --deploy` con configuración de producción.
3. Crear base y cuenta de demostración con datos ficticios y permisos acotados; comprobar que no pueda acceder a datos reales ni administración sensible.
4. Verificar persistencia y restauración de datos, medios subidos, HTTPS, SECRET_KEY externa, DEBUG=False y hosts permitidos.
5. Elegir alojamiento Python/Docker y conocer su tarifa, almacenamiento y límites antes de contratar. El portafolio estático no ejecuta el backend Django.
6. Añadir el enlace real a la ficha únicamente después de verificar el despliegue.

No se contrató hosting ni se anunciaron precios o una demo inexistente.

## Siguiente decisión

Revisar la dirección visual y confirmar datos del cyber y Telegram. Después decidir si esta propuesta sustituye index.html o permanece como página separada. La fusión y publicación quedan para después de esa revisión.
