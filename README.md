# Papelería POS Online

Interfaz pública (código fuente) del sistema de punto de venta. **Los datos y el inicio de sesión son privados y están en Supabase**, no en este repositorio.

## Acceso

URL del sitio cuando se habilite GitHub Pages:
https://ricardodanmaravilla-coder.github.io/papeleria-pos-online/

Se inicia sesión con el administrador exclusivo de Papelería POS, `ricardodan.maravilla+papeleria@gmail.com`. El alias `+papeleria` recibe correos en `ricardodan.maravilla@gmail.com`, pero se registra como usuario diferente en Supabase y admite una contraseña independiente. La cuenta se da de alta desde el botón «Crear mi contraseña de Papelería POS» y, cuando el correo queda confirmado, se le otorga el rol de administrador. Las credenciales de Fletes MA ya no tienen acceso a POS. El proyecto reutiliza la instancia de Fletes MA pero mantiene tablas independientes prefijadas con `pos_`. El archivo `index.html` usa solo la **clave publicable** de Supabase, que no otorga acceso por sí sola: los datos están protegidos por inicio de sesión y RLS.

## Publicación por rama (sin GitHub Actions de compilación)

En **Settings → Pages** selecciona **Deploy from a branch**, rama **main**, directorio **/(root)** y pulsa **Save**. La publicación utiliza GitHub Pages y no requiere compilar un EXE. GitHub puede contabilizar el proceso Pages como un workflow de despliegue, por lo que no prometemos que no aparezca una ejecución en Actions.

## Alcance actual

Ventas, cantidades, precios puntuales de venta, productos, existencias, clientes, cupones y reportes preliminares. La impresión de tickets/cupones usa el navegador. La base web comienza vacía y no importa automáticamente la base de datos local SQLite de Windows. Se requieren pruebas en el dispositivo e impresora reales antes de operación comercial.