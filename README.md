# Chifa Pollería El Dragón 🐉

Proyecto de la Semana 05 - Desarrollo de Aplicaciones Web 

## Integrantes
- Integrante 1: Pariona Larrota Andre Sebastian
- Integrante 2: Valencia Bernaola Andres Anthony

## Tema elegido
Restaurante/Delivery - Chifa Pollería

## Combinación Bootstrap + Tailwind

### Conflictos de especificidad encontrados y solución

1. **`bg-*` (colores de fondo):** Bootstrap define `bg-dark`, `bg-warning`, etc.
   Tailwind también usa `bg-*` para sus utilidades. Solución: usar `bg-*` de
   Bootstrap para colores del tema y `bg-gradient-to-r from-* via-* to-*` de
   Tailwind para degradados, ya que Bootstrap 5.3 no incluye degradados nativos.

2. **`rounded-*`:** Bootstrap usa `rounded`, `rounded-pill`; Tailwind usa
   `rounded-xl`, `rounded-2xl`. No hay choque porque los nombres difieren,
   pero se prefirió `rounded-pill` (Bootstrap) para botones y `rounded-xl`
   (Tailwind) para tarjetas.

3. **`shadow-*`:** Bootstrap solo llega a `shadow-lg`. Se usó Tailwind
   (`shadow-lg`, `shadow-2xl`) cuando se necesitó más profundidad.

4. **Orden de carga:** Bootstrap CSS se carga primero y Tailwind (Play CDN)
   después. Como Tailwind Play CDN genera estilos en línea al runtime, sus
   utilidades ganan sobre Bootstrap cuando ambas apuntan a la misma propiedad.