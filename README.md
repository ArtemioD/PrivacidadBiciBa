# Política de Privacidad de BiciBA

La política de privacidad de [BiciBA](https://github.com/ArtemioD/BiciBA), publicada como página
estática para poder enlazarla desde Google Play y desde la propia aplicación.

`index.html` es la página entera: no tiene dependencias ni build, se abre tal cual.

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
