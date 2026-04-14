# Staymonsul — Web de Apartamentos Turísticos

## Cómo publicar en www.staymonsul.com con Vercel

### Opción A — Sin instalar nada (más fácil)

1. Ve a [vercel.com](https://vercel.com) y crea una cuenta gratuita
2. En el dashboard, haz clic en **"Add New → Project"**
3. Elige **"Browse"** y sube la carpeta `staymonsul` completa
4. Vercel detectará automáticamente que es un sitio estático
5. Haz clic en **Deploy** — en 30 segundos tendrás una URL tipo `staymonsul.vercel.app`

### Conectar tu dominio staymonsul.com

1. En el proyecto de Vercel, ve a **Settings → Domains**
2. Escribe `staymonsul.com` y haz clic en **Add**
3. Vercel te dará unos registros DNS para añadir en tu registrador de dominios:
   - Registro **A**: `76.76.21.21`
   - Registro **CNAME** para `www`: `cname.vercel-dns.com`
4. Una vez propagados (puede tardar hasta 24h), el dominio estará activo con HTTPS automático

### Opción B — Con GitHub (recomendado para futuras actualizaciones)

1. Crea un repositorio en [github.com](https://github.com)
2. Sube los archivos `index.html` y `vercel.json`
3. En Vercel, conecta tu cuenta de GitHub e importa el repositorio
4. Cada vez que actualices el repositorio, Vercel publicará los cambios automáticamente

---

## Personalizar el contenido

Abre `index.html` con cualquier editor de texto y modifica:

- **Nombre del alojamiento**: busca "Staymonsul" y cámbialo si es necesario
- **Precios**: busca "85€", "130€", "210€" 
- **Ubicación**: reemplaza "Costa Mediterránea, España" con tu ubicación exacta
- **Email y teléfono**: busca `hola@staymonsul.com` y `+34 600 000 000`
- **Textos descriptivos**: todos los textos en español tienen su traducción en inglés (`data-es` / `data-en`)

## Añadir fotos reales

Reemplaza los bloques de color por imágenes reales. En el código, busca las clases `.apt-img-1`, `.apt-img-2`, `.apt-img-3` y cambia el estilo CSS por:

```css
.apt-img-1 {
  background-image: url('fotos/apartamento1.jpg');
  background-size: cover;
  background-position: center;
}
```

Y crea una carpeta `fotos/` con tus imágenes.
