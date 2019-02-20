# Instalación Bedrock + Sage
[![N|25Watts](https://www.tersuave.com.ar/assets/frontend/dist/images/logo_25.svg )](https://www.25watts.com.ar/)

## Bedrock
[Bedrock](https://roots.io/bedrock/) ofrece una forma alternativa para administrar su instalación de WordPress con una estructura de carpetas mejorada, herramientas de desarrollo modernas, y una mejor seguridad.

### Requerimientos

  - PHP >= 7.1
  - [Composer](https://getcomposer.org/)

### Instalación

1. Crear un nuevo proyecto

```sh
$ composer create-project roots/bedrock
```

2. Actualizar el **.env** con los correspondientes datos. Ej
```html
DB_NAME=25Watts
DB_USER=root
DB_PASSWORD=

# Optional variables
# DB_HOST=localhost
# DB_PREFIX=wp_

WP_ENV=development
WP_HOME=http://25watts.local.com.ar
WP_SITEURL=${WP_HOME}/wp

# Generate your keys here: https://roots.io/salts.html
AUTH_KEY='u<ZE*(cR?JaIC!3wtWZSqcLwKbXD<h;o-w8K<P7Zz4V0pE#K?Tw#vKt8DYH0Q-{q'
SECURE_AUTH_KEY='a,}$0.!BokyXZ[r0gJDNf#B;X}K,t}l[+qDGr>j83c0CuXUe*7K%w(3[A!,K+A}N'
LOGGED_IN_KEY='nF{_^P8RiAxF16N;eso_^Mm<)AGr2l(L(G=ZSUEihO77mK:1ILk,OqDt67%k/g!?'
NONCE_KEY='i3Bt&J-y5rCdPAv)$&rl-h$h0d(P(c5iC[3w=nX2ajX^-J1aMCriZ|mzK&EjeV17'
AUTH_SALT='K/-I<o&*|bzZsWQCE=UH?/;:gV/u2*l(P4T9,X@Pjt3=zQEVFI&ehQ#)y=YV+!XR'
SECURE_AUTH_SALT='&{yBM|<}ccB);{X$:;bty%l<H43}s|Up{r|^?;JKQ*]TEw3V1T5-vJErE7;pE76#'
LOGGED_IN_SALT='qc;td-p%Ds:x!c9F*#.7SQpA[KCF%Y_J<[]7L|zrQQKQp`ex(As;T$_qh6kTLB*O'
NONCE_SALT='z>g*L!RZqgi*N=>/urCcH=Ta!ZP+B=^qiZ7S?Y[TwXUaNY(wIVv2g/5AE>c0TX5P'
```

3. Acceder al admin a trave de `https://25watts.local.com.ar/wp/wp-admin`

> Recordar utilizar siempre un virtual host y chequear que apunte a **/web**

&nbsp;
&nbsp;

## Sage
[Sage](https://roots.io/sage/) es un Starter WordPress Theme  con un flujo de trabajo de desarrollo moderno.

### Requerimientos

- WordPress >= 4.7
- PHP >= 7.1.3 (with php-mbstring enabled)
- [Composer](https://getcomposer.org/) >= 8.0.0
- [Nodejs](https://nodejs.org/en/) 
- [Yarn](https://yarnpkg.com/en/docs/install)

### Instalación

1. Instalar Sage usando Composer desde el directorio de temas (remplazar "your-theme-name") con el nombre de la carpeta o tema

```sh
# @ \web\app\themes
$ composer create-project roots/sage your-theme-name
```

2. Desde el directorio del tema ejectutar **yarn**

```sh
$ yarn
```

3. Luego de esto se podran ejecutar los siguientes comando

* `yarn build` - Compila y optimiza los archivos en tu directorio de activos.
* `yarn build:production` - Compila y optimiza los archivos para producción.
* `yarn start` - Compila los activos cuando se realicen cambios en el archivo, utilizando Browersync

### Browsersync Configuración

Actualizar `devUrl` en la parte inferior de `resources/asset/config.json` `con la url del virtual host local en este ejemplo seria 

```json
 "devUrl": "http://25watts.local.com.ar/",
```
&nbsp;
_by fran with_ ❤
