# Taller: API REST con Express en Cloudflare

Taller de **Patrones de Diseño de Software** – Ingeniería de Sistemas, Pontificia Universidad Javeriana.

API REST hecha con **Express** que guarda datos en **D1** (base de datos SQL de Cloudflare) y se ejecuta en **Cloudflare Workers**.

## Desplegar (un clic)

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/jhonconmejillas-cyber/taller-api-rest-cloudflare)

El botón copia este repositorio a tu GitHub, crea tu base de datos D1, crea la tabla `members` con datos de ejemplo y publica la API.

## Rutas

| Método | Ruta | Qué hace |
|---|---|---|
| GET | `/` | Mensaje de bienvenida |
| GET | `/api/members` | Lista todos los registros |
| GET | `/api/members/:id` | Muestra un registro |
| POST | `/api/members` | Crea un registro (`name`, `email`) |
| PUT | `/api/members/:id` | Actualiza un registro |
| DELETE | `/api/members/:id` | Elimina un registro |

## Archivos

```
src/index.ts                          ← la API (Express)
migrations/0001_create_members_table.sql  ← crea la tabla al desplegar
wrangler.jsonc                        ← configuración de Cloudflare (binding DB)
package.json                          ← dependencias y scripts
```

Basado en la plantilla oficial de Cloudflare [express-on-workers](https://github.com/cloudflare/docs-examples/tree/main/workers/express-on-workers).
