# Soniar — Smoke Test Checklist
> Ejecutar después de cada deploy antes de cerrar la sesión.

---

## 🚀 Arranque
- [ ] Splash aparece y navega solo en menos de 3 segundos
- [ ] No hay pantalla blanca ni splash trabado
- [ ] No hay errores en consola (F12 → Console)

## 🌙 Onboarding (solo si `localStorage` no tiene `soniar_onboarded`)
- [ ] Slide 1 muestra logo y texto correctamente
- [ ] Slide 2 muestra el carrusel de imágenes en movimiento
- [ ] Slide 3 muestra el visual y texto correcto
- [ ] Botón "Empezar" navega al Home

## 🏠 Home
- [ ] Topbar muestra "Soniar" y ícono de notificaciones
- [ ] Hero con título y botón "Contar mi sueño" visible
- [ ] Bottom nav visible con 4 íconos
- [ ] Ícono Home activo/destacado

## ✍️ Compose
- [ ] Textarea funciona y cuenta caracteres
- [ ] Chips de emoción seleccionables
- [ ] Chips de tipo de sueño seleccionables
- [ ] Slider de intensidad funciona
- [ ] Estilos visuales seleccionables
- [ ] Botón "Dictá tu sueño" abre popup de privacidad
- [ ] Botón "Interpretar sueño" navega a loading

## ⏳ Loading
- [ ] Spinner visible
- [ ] Mensajes de carga cambian secuencialmente
- [ ] Subtítulos rotativos aparecen

## 📊 Resultado
- [ ] Pantalla aparece vacía (sin datos del sueño anterior)
- [ ] Imagen carga con fade-in suave
- [ ] Resumen poético aparece
- [ ] Barras de emoción se animan
- [ ] Símbolos clave clickeables (abren modal)
- [ ] Texto de interpretación visible
- [ ] Botón "Escuchar" funciona
- [ ] Sección "Ajustar imagen" visible y scrolleable
- [ ] Chips de ajuste funcionan (solo 1 por sueño)
- [ ] Input de ajuste libre funciona
- [ ] Mensaje de malestar visible al final
- [ ] Botones de acción (home, guardar, descargar, compartir) visibles

## 👥 Feed
- [ ] Solo accesible con plan premium/trial
- [ ] Sin premium → redirige a upgrade
- [ ] Imágenes cargan correctamente
- [ ] Filtros por emoción funcionan
- [ ] Reacciones funcionan
- [ ] Bottom nav visible con Feed activo

## 📁 Historial
- [ ] Solo accesible con plan premium/trial
- [ ] Grid de sueños carga
- [ ] Click en sueño abre resultado guardado
- [ ] Bottom nav visible con Historial activo

## 📈 Insights
- [ ] Muestra datos del usuario logueado
- [ ] Emoción dominante y símbolos recurrentes
- [ ] Botón "Cerrar sesión" funciona
- [ ] Bottom nav visible con Insights activo

## 🔐 Auth
- [ ] Login funciona con email/password
- [ ] Registro funciona con TyC aceptados
- [ ] "Olvidaste tu contraseña" envía email
- [ ] "Continuar sin cuenta" navega al home

## 💳 Upgrade
- [ ] Pantalla de upgrade muestra los 3 planes
- [ ] Trial gratuito funciona
- [ ] Checkout de Stripe abre correctamente

## 🔔 Notificaciones
- [ ] Badge aparece cuando hay notificaciones nuevas
- [ ] Lista de notificaciones carga

---

## 🐛 Bugs conocidos / pendientes
- Streak (fueguito) eliminado — reimplementar cuando haya lógica completa
- Worker rate limit requiere KV namespace configurado en Cloudflare

---

## 📋 Deploy checklist
1. [ ] Probar en navegador desktop
2. [ ] Probar en iPhone (Safari)
3. [ ] Abrir F12 → Console → sin errores rojos
4. [ ] Commit en GitHub con mensaje descriptivo
5. [ ] Tag si es versión estable: `git tag vX.X-stable`
