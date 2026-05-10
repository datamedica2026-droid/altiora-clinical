# AltioraClinical

## Estructura del proyecto

```
altiora-clinical/
├── index.html    ← Landing pública
├── panel.html    ← Panel interno del equipo
├── app.html      ← Entorno del cliente médico
└── README.md     ← Este archivo
```

## URLs de producción

- **Landing:** https://altiora-clinical.vercel.app
- **Panel interno:** https://altiora-clinical.vercel.app/panel.html
- **Entorno cliente:** https://altiora-clinical.vercel.app/app.html?slug={slug-del-cliente}

## Acceso al panel

- Usuario: `datamedica` · Contraseña: `DM2025admin`
- Usuario: `especialista` · Contraseña: `DM2025stat`

## Infraestructura

| Servicio | Para qué | URL |
|---|---|---|
| Vercel | Hosting y deploy automático | vercel.com |
| GitHub | Control de versiones | github.com/datamedica2026-droid/altiora-clinical |
| Supabase | Base de datos en la nube | supabase.com (proyecto: altiora-clinical, São Paulo) |
| EmailJS | Correo automático pre-lead | dashboard.emailjs.com |
| Google Sheets | Respaldo de leads | Ver Drive del equipo |
| Calendly | Agendamiento | calendly.com/smdb-optimizer |

## Tablas en Supabase

- `leads` — Médicos del formulario principal
- `preleads` — Médicos de asesoría previa $5 USD
- `clientes` — Entornos activados (con PIN y fecha de vencimiento)
- `registros` — Datos de pacientes ingresados por los médicos

## Estado Mayo 2026

- ✅ Landing conectada a Supabase + Sheets + EmailJS
- ✅ Panel guarda clientes en Supabase
- ✅ App carga entornos desde Supabase por slug
- ✅ Registros de pacientes van a Supabase
- ✅ PIN de acceso por entorno
- ✅ Verificación de vencimiento de membresía
- ✅ RLS activado en todas las tablas
- ⏳ Panel aún muestra landing al cargar (pendiente fix)
- ⏳ Panel leer leads desde Supabase en tiempo real
