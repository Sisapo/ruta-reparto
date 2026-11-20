# Guía de pruebas · Ruta de reparto 0.8.0-beta

Gracias por probarla. Son unos 20 minutos. Al terminar, pulsa **Copiar informe de prueba** (sección *Datos*), pega el texto en el grupo de pruebas y completa las tres últimas líneas.

Usad la **ruta de ejemplo** (datos ficticios). Si probáis con paquetes reales, borrad la ruta al acabar con **Vaciar ruta**.

## 1. Instalación y permisos

- [ ] Abro la dirección de la app en Chrome (Android) o Safari (iPhone).
- [ ] La instalo en la pantalla de inicio y se abre como una app.
- [ ] En **Oficina y ajustes → Dar permisos de cámara y GPS**, salen concedidos los dos.

## 2. Oficina de salida y vuelta

- [ ] Aparece «Correos Villarrubia de los Ojos» como inicio y fin.
- [ ] Añado mi oficina (**Añadir oficina**), le pongo nombre y dirección y la selecciono.
- [ ] Arriba cambia «Inicio y fin» a mi oficina.

## 3. Escanear etiquetas

- [ ] **Escanear**: la cámara lee el código de Correos de una etiqueta.
- [ ] La app propone la calle y el número. ¿Acierta? Anotad cuántas de 10.
- [ ] No aparece ningún nombre de destinatario.
- [ ] Si escaneo dos veces el mismo paquete, avisa de que está repetido.
- [ ] Dos paquetes a la misma dirección se juntan en una parada («2 bultos»).
- [ ] **Foto** también funciona con una foto de la etiqueta.

## 4. Ruta normal

- [ ] **Cargar ruta de ejemplo** → aparecen 22 paradas y 23 bultos.
- [ ] **Localizar direcciones** → casi todas pasan a «localizada».
- [ ] **Optimizar orden** → el orden tiene sentido para alguien que conoce el pueblo.
- [ ] **Generar tramos** → cada enlace abre Google Maps con las paradas en orden, saliendo y volviendo a la oficina.
- [ ] Probad **A pie** y **Vehículo** en *Tipo de reparto*.

## 5. Servicio rural con horarios

- [ ] En *Servicio rural*, edito Puerto Lápice y Las Labores y pongo su dirección exacta (o «Estoy aquí (GPS)» si estoy allí).
- [ ] Marco **Hoy** en las dos y pulso **Optimizar orden**.
- [ ] La lista muestra las oficinas rurales en su sitio con «Llegada ≈ hh:mm» y el margen.
- [ ] Si pongo una hora de salida muy tardía, avisa en rojo de que llego tarde.
- [ ] Los tramos de Google Maps terminan en cada oficina rural.

## 6. Día con mucha carga (prioridades y zonas)

- [ ] Cada parada muestra su prioridad (**Obligado**, **Registrado**, **Ordinario**). Al tocarla, cambia.
- [ ] Marco como **Obligado** los que caducan o son último intento.
- [ ] Pongo una **hora límite de vuelta** que no dé para todo y pulso **Optimizar orden**: los obligados siempre quedan; lo que no cabe pasa a «Para otro día», por zonas completas.
- [ ] En **Zonas de hoy** pongo 2 o 3 aldeas en «Hoy sí, todo» y otras en «Solo obligados»: la ruta respeta esa elección.
- [ ] «Repartir hoy» en una parada de «Para otro día» la vuelve a meter.
- [ ] **Recorrido habitual:** marco «Seguir mi recorrido habitual» (o «Cargar recorrido rural de Malagón») y ordeno las zonas con las flechas. La ruta va zona por zona en ese orden.
- [ ] **Puntos de paso:** añado a mano un camino o carretera (por ejemplo, Camino Hurtado) con prioridad «Punto de paso» para que Google Maps pase por ahí.

## 7. Aldeas y diseminados

- [ ] Una calle que no sale en el mapa (por ejemplo, de una aldea) queda «aproximada (pueblo)».
- [ ] En **Editar → Elegir en el mapa** (o «Estoy aquí (GPS)» en la puerta) fijo el punto. Con «Ver satélite» se ven las casas de campo.
- [ ] Al guardar, aparece en **Oficina y ajustes → Lugares guardados**. Otro día, la misma calle se localiza sola.
- [ ] En **Lugares guardados → Añadir lugar en el mapa** sitúo una aldea que el mapa no conoce (por ejemplo, Valdehierro o Quiles de Abajo).
- [ ] **Copiar lugares** y pásalos al grupo; un compañero los añade con **Pegar lugares**.

## 8. Durante el reparto

- [ ] Marco paradas como **Entregada** y desaparecen de los tramos al volver a generarlos.
- [ ] Cierro la app y la vuelvo a abrir: la ruta sigue ahí.
- [ ] Sin cobertura (modo avión), la app se abre y la lista se ve.

## Qué contar en el informe

- Modelo de móvil y si leyó bien los códigos.
- Cuántas direcciones acertó leyendo la etiqueta.
- Si las horas estimadas se parecen a las reales (y qué velocidad media pusiste).
- Lo que no entendiste o te sobró.
