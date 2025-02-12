Tarjeta de Usuario con Roles y Botón “Avalar”
Este repositorio contiene un ejemplo de una tarjeta de usuario que muestra:

Nombre del usuario y roles (puede tener uno o varios, como AVALADOR o EDITOR).
Una fecha o “hecho” destacado.
Estadísticas (funcionarios, conductas, intervinientes, etc.).
Sección de editores (muestra un número limitado de avatares y, si hay más, agrega un “+X”).
Un botón para “Avalar” que cambia de apariencia y funcionalidad según el rol del usuario.
Características principales
HTML, CSS y JavaScript puro

No necesitas ningún framework adicional.
Diseño adaptable para ajustarse a un contenedor de ancho variable.
Roles múltiples

El usuario puede tener uno o varios roles (p. ej. ["AVALADOR", "EDITOR"]). Cada rol se muestra como un “badge”.
Control de permisos

Si el usuario no tiene el rol AVALADOR, se muestra un alert indicando que no tiene permisos al pulsar el botón.
Si el usuario tiene el rol AVALADOR, el botón cambia a “Avalado” (se pone verde) y aparece un alert de “Hecho avalado con éxito”.
Sección de Editores

Muestra hasta 3 avatares.
Si hay más de 3 editores, se agrega un +X indicando cuántos editores adicionales hay.
Fecha centrada

Se ubica la fecha (o “hecho”) en la parte central, encima de las estadísticas.
Estructura de archivos
bash
Copiar
Editar
.
├── index.html         # Ejemplo principal con la tarjeta de usuario
├── README.md          # Este archivo de documentación
└── (opcional) styles.css, script.js, etc.
En el index.html encontrarás todo el código (HTML, CSS, JS) en un único archivo para simplificar la demostración.

Cómo usar este proyecto
Clonar o descargar este repositorio:

bash
Copiar
Editar
git clone https://github.com/tu-usuario/tarjeta-usuario-roles.git
Abre el archivo index.html en tu navegador web. Deberías ver la tarjeta de usuario con la fecha, estadísticas, roles y el botón de “Avalar”.

Para modificar el comportamiento, edita la variable userData al inicio del <script>:

js
Copiar
Editar
const userData = {
  name: "Mary Lebowski",
  date: "11 Nov, 2018 07:46 AM",
  roles: ["AVALADOR", "EDITOR"], // Ajusta o quita "AVALADOR" para probar permisos
  avatarUrl: "https://i.pravatar.cc/48?u=933372",
  funcionarios: 14,
  conductas1: 97,
  intervinientes: 16,
  conductas2: 16
};
Cambia los valores o añade más roles.
Personaliza la URL del avatar.
Actualiza las estadísticas según tu caso real.
Para cambiar la lista de editores (los avatares pequeños), edita la variable editorsList:

js
Copiar
Editar
const editorsList = [
  { name: "Editor1", avatar: "https://i.pravatar.cc/24?u=Editor1" },
  // ...
];
Agrega o quita objetos para ver cómo se comporta el “+X”.
(Opcional) Separa el CSS y el JS en archivos independientes (styles.css, script.js) si lo deseas. Asegúrate de actualizar las referencias en tu index.html.

Personalización
Cambia colores, tamaños de fuentes, márgenes y posicionamiento en el CSS según tu diseño.
Modifica los textos en las estadísticas (FUNCIONARIOS, CONDUCTAS, etc.) para que coincidan con tu uso real.
Ajusta la lógica del botón “Avalar” en el evento click si quieres otro comportamiento (por ejemplo, hacer una llamada a tu backend).
Contribuciones
¡Siéntete libre de enviar PRs o abrir Issues para sugerir mejoras! Este ejemplo está diseñado para ser un punto de partida, así que tus aportes son bienvenidos.

Licencia
Puedes usar este código de forma libre (ej. MIT License) en tus proyectos personales o empresariales. Ajusta la licencia según te convenga.
