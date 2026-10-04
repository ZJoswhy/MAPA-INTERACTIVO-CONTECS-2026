# Guía interactiva de salones del congreso

`index.html` es la guía completa: los planos del segundo y tercer alto del Edificio 3 con cada salón tocable, la agenda, la búsqueda y los filtros por tipo de actividad y por día. Es un solo archivo y no necesita instalar nada. Para probarla, ábrela con doble clic.

## Cargar las actividades

La forma más fácil es el modo organizador:

1. Abre la guía y toca **Editar la guía** al pie de la agenda (o agrega `?organizador` al final de la dirección).
2. En **Datos del congreso** escribe el nombre, el subtítulo y los días con su fecha. Con la fecha puesta, ese día aparece el filtro "En curso ahora".
3. Toca un salón en el plano. Puedes darle un nombre visible (por ejemplo "Auditorio menor"), un rótulo corto para el plano (por ejemplo el código oficial "3-301") y la capacidad, y agregar sus actividades.
4. Cuando termines, toca **Descargar archivo**. Obtendrás un `index.html` nuevo con todo incluido.

Los cambios se guardan como borrador solo en el navegador donde editas. Si varias personas del equipo cargan datos, conviene que una sola consolide todo antes de publicar.

También puedes editar los datos a mano: están al inicio de `index.html`, entre las marcas `INICIO-DATOS` y `FIN-DATOS`, con instrucciones en el mismo archivo.

Las actividades que vienen cargadas son de ejemplo (dicen "(ejemplo)" en el título): reemplázalas o elimínalas.

### Códigos de salón

Cada espacio tiene el código `piso-número`, donde el número es el que aparece en el plano: `3-73` es el espacio 73 del tercer alto y `2-82` el espacio 82 del segundo alto. Esos números son los del plano arquitectónico, que no siempre coinciden con los códigos que usa la universidad; para eso están los campos de nombre y rótulo.

## Publicar en GitHub Pages (gratis)

1. Crea una cuenta en github.com si no tienes una.
2. Crea un repositorio nuevo, por ejemplo `guia-congreso`, y márcalo como público.
3. Usa **Add file > Upload files**, arrastra `index.html` (y este README si quieres) y confirma con **Commit changes**.
4. Entra a **Settings > Pages**. En "Build and deployment" elige **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`, y guarda.
5. En uno o dos minutos la guía estará en `https://TU-USUARIO.github.io/guia-congreso/`.

Para actualizarla, sube el `index.html` nuevo al mismo repositorio; reemplaza al anterior y la dirección no cambia, así que el QR sigue sirviendo.

## Crear los códigos QR

En el modo organizador, toca **Códigos QR**, pega la dirección pública de la guía y descarga el código en PNG o SVG. Desde ahí mismo puedes preparar una hoja imprimible con un QR para la puerta de cada salón; cada uno abre la guía con ese salón ya seleccionado. Esta función necesita conexión a internet (carga el generador al momento).

También sirve cualquier generador de QR. Algunos consejos:

- Usa un QR estático. Los "dinámicos" gratuitos suelen caducar o mostrar publicidad.
- Imprímelo de al menos 3 cm de lado (mejor 5 cm o más en carteles) y escribe la dirección debajo.
- Pruébalo con varios teléfonos antes de imprimir en cantidad.

## Enlaces especiales

Puedes agregar estas terminaciones a la dirección de la guía, también dentro de un QR:

- `#salon=3-73` abre la guía con ese salón seleccionado.
- `#aqui=3-4` muestra un punto de "Estás aquí" en ese espacio. Sirve para carteles junto a las escaleras o la entrada de cada piso (el 3-4 son las escaleras del ala este del tercer alto).
- `#piso=2` abre directamente el segundo alto.

Ejemplo: `https://TU-USUARIO.github.io/guia-congreso/#aqui=3-4`

## Notas

- Los armarios y ductos pequeños del plano no son tocables; los baños y escaleras sí, con un ícono.
- Para agregar otro piso u otro edificio hay que procesar su plano y generar la geometría de los salones.
- El modo oscuro sigue la configuración del teléfono y muestra el plano como un plano azul.
