# Santa Cucina

Tienda web de comida casera para llevar: tartas caseras y prepizzas, con carrito
y pedido por WhatsApp. Es un sitio estático (un solo `index.html`), sin build ni
dependencias.

## Estructura

```
santa-cucina/
├── index.html      → toda la app (HTML + estilos + lógica)
├── img/            → fotos de los productos
│   ├── puerro-pollo-cebolla.jpg
│   ├── calabaza-espinaca-cebolla.jpg
│   ├── calabaza-cebolla.jpg          (PROVISORIA — reemplazar)
│   ├── verduras.jpg                  (PROVISORIA — reemplazar)
│   └── prepizza.jpg
├── netlify.toml
└── README.md
```

## Cosas para completar

1. **Número de WhatsApp.** En `index.html`, buscá `const WHATSAPP` y poné el número
   real (con código de país, sin `+` ni espacios). Ej: `const WHATSAPP = "34600112233";`
2. **Dos fotos provisorias.** `img/calabaza-cebolla.jpg` y `img/verduras.jpg` tienen
   una foto parecida de relleno. Cuando tengas la foto real, **reemplazá el archivo
   con el mismo nombre** y listo (no hay que tocar código).

## Cómo editar

- **Cambiar una foto:** reemplazá el archivo dentro de `img/` conservando el mismo
  nombre. Ideal: cuadrada (1:1), lado ~680 px.
- **Cambiar precios:** en `index.html`, arriba del todo del `<script>`:
  `MINI` (individual), `MINI3` (combo 3), `GRANDE`, `PREP` (prepizza), `PREP4` (combo 4).
- **Cambiar sabores/descripciones:** en el array `tartas` dentro de `index.html`.

## Publicar en Netlify (desde GitHub)

1. Creá un repositorio nuevo en GitHub y subí estos archivos (ver abajo).
2. En Netlify: **Add new site → Import an existing project → GitHub** y elegí el repo.
3. Dejá el build vacío y *publish directory* en la raíz (`.`). Netlify ya lo detecta
   por el `netlify.toml`. **Deploy.**
4. Cada vez que hagas un cambio y lo subas a GitHub, Netlify actualiza el sitio solo.

## Subir a GitHub

**Opción fácil (sin consola):** en el repo nuevo, botón *Add file → Upload files*,
arrastrás `index.html`, la carpeta `img/`, `netlify.toml` y `README.md`, y *Commit*.

**Opción consola:**
```bash
git remote add origin https://github.com/USUARIO/santa-cucina.git
git branch -M main
git push -u origin main
```
