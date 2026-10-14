# Política de Privacidad de BiciBA

Este repositorio contiene **una sola página web**: la política de privacidad de
[BiciBA](https://github.com/ArtemioD/BiciBA), publicada para poder enlazarla desde Google Play y
desde la propia aplicación.

Google Play exige una política alojada en una dirección pública y estable antes de publicar una
aplicación, y vuelve a pedirla cada vez que cambia lo que la aplicación recoge. Eso es todo lo que
vive acá: `index.html` es la página entera, sin dependencias ni compilación, se abre tal cual.

## Qué es BiciBA

Una aplicación Android independiente para recorrer Buenos Aires en bicicleta: muestra las ciclovías
de la Ciudad sobre el mapa y propone circuitos turísticos para recorrerlas.

- **Mapa de ciclovías**, dibujadas sobre el mapa de la Ciudad.
- **Circuitos** con su distancia, duración estimada, dificultad y puntos de interés.
- **Guía durante el recorrido**: señala hacia el próximo punto pendiente y avisa al llegar.
- **Inicio** con el recorrido que quedó a medias y los circuitos que arrancan más cerca.
- **Perfil** con nombre, foto y el tema claro u oscuro.

## Qué función de la app explica cada dato

La política no describe la aplicación en general: dice qué recoge y por qué. Esta es la
correspondencia, que es lo que hay que revisar cada vez que la aplicación cambia.

| Dato | Función que lo necesita | Dónde queda |
|---|---|---|
| Nombre, correo e identificador | Crear la cuenta e iniciar sesión | Firebase |
| Foto de perfil | Mostrarla en el perfil, solo si se sube una | Firebase Storage |
| Ubicación | Ubicar al usuario en el mapa, ordenar los circuitos por cercanía y guiarlo en el recorrido | **Solo en el teléfono** |
| Diagnóstico y uso | Detectar fallos y entender de forma agregada cómo se usa | Crashlytics y Analytics |
| Identificador de publicidad | Mostrar los anuncios que sostienen el proyecto | AdMob |
| Tema, recorrido en curso y mapa descargado | Recordar la preferencia y poder consultar sin conexión | **Solo en el teléfono** |

## Publicarla

Se sirve con GitHub Pages: **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.
Al llamarse `index.html`, la dirección queda en la raíz:

```
https://artemiod.github.io/PrivacidadBiciBa/
```

Esa es la que va en la ficha de Google Play.

## Mantenerla

La política describe lo que la aplicación hace de verdad, así que **se actualiza junto con la app**:
al agregar un permiso, un SDK que procese datos o una función que guarde algo nuevo, hay que
reflejarlo acá y cambiar la fecha de "Última actualización". Google Play compara lo que declara la
ficha con lo que el paquete realmente contiene.
