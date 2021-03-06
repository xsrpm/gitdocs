# 5) Angular Bindings, Comunicación componentes, Angular UI (Material, PrimeNG, Bootstrap) y Angular Routing

## **Filosofía de trabajo**

Angular es un framework que se encarga de orquestar/distribuir la lógica de programación en el front.

En Angular todo está orientado a componentes que se incrustan y reutilizan.

El componente padre es el componente App (si no se le cambió el prefijo).

# **1 - Requerimientos**

```jsx
node -v (nodejs >8)
npm -v (npm >5)
```

# **2 - Instalación**

**Angular CLI**: Forma de trabajar agil y productiva con Angular

```jsx
npm install -g @angular/cli
```

(-g de manera global)

(actualmente bajara la versión 8)

Para instalar otras versiones de angular:

[https://github.com/angular/angular-cli/branches](https://github.com/angular/angular-cli/branches)

Para bajar la versión 5 de angular.

```jsx
npm install -g @angular/cli@1.5
```

Las versiones de angular pueden leer versiones anteriores de angular.

Solo se puede tener una versión de Angular CLI, se recomienda tener siempre la última versión de Angular CLI para compatibilidad con todas las versiones.

**Ver la versión de Angular y si todo está ok**

```jsx
ng --version
```

Los comandos de ng y npm pueden abreviarse con sus iniciales

Ejemplo: ng install **ó** ng i

# **3 – Comandos de Ejecución**

## **Crear un nuevo proyecto**

Elegir una carpeta y dentro ejecutar:

```jsx
ng new demo
```

Nombre de proyecto: demo

La consola hará unas preguntas:

**Angular Routing?** Por defecto Si. Es raro no usar routing.

Caracteristica para definir las reglas de navegacion en el proyecto.

**Formato de hojas de estilo**: CSS por defecto.

Para restablecer la carpeta node_modules.

Colocarse en la razi del proyecto y ejecutar:

```jsx
npm install / npm i
```

Esta carpeta se reconstruye a partir del archivo packages.json, que simula al pom.xml en maven.

## **Correr el proyecto**

Ejecutarlo siempre desde la raíz del proyecto creado.

```jsx
ng serve --o  /  ng s --o
```

(enviando --o ) se abre el navegador y muestra la web.

## **Crear un componente**

Ejecutarlo siempre desde la raíz del proyecto creado o desde dentro del componente / modulo deseado. Creará el componente a partir de la carpeta app.

Crea un componente y lo registra en el app.module (declarations)

Cada componente está formado por un archivo html, css, ts (typescript - logica) y spec.ts (typescript - opcional para pruebas)

ng generate component compA   / ng g c compA

Atajo para no crear el archivo de pruebas:

```jsx
ng g c compA –skipTests (Angular 8.3)
ng g c compA –spec=false (Angular versiones anteriores)
```

## **Crear Servicio**

```jsx
ng generate service serv1 / ng g s serv1
```

## **Crear Modulo**

```jsx
ng generate module mod1 / ng g m mod1
```

# **4 - Estructura del proyecto**

src: Contenido del proyecto.

app: Toda la lógica, html y css de nuestro proyecto.

app.module.ts : registramos todos los componentes del proyecto.

import : Zona donde se indica la ruta de importación de componentes o módulos a utilizar

@NgModule

Declarations: Lugar donde se registra los componentes a usar.

Imports: Se registran los módulos (conjunto de componentes) que se necesitan activar en el proyecto.

providers: Era utilizado para conectarse con servicios RESTs, registrando las clases necesarias.

bootstrap: Hace mención de que componente arrancará el aplicativo.

export:

app.component.css : Hoja de estilo del componente.

app.component.html: Html del componente con incrustaciones de lógica.

app.component.spec.ts: Pruebas unitarias para el componente.

app.component.ts: Lógica del componente

import

@Component

*Selector: alias para el componente con el que se hará referencia desde los archivos .html*

*templateUrl: url relativa del archvo .html del componente*

*styleUrls: Urls de hojas de estilo del componente.*

export: propiedades a exportar que puede ser accedidas desde el html.

angular.json (archivo de configuración para angular CLI)

index.html : archivo Single Page Application (único archivo html de nuestro proyecto visible desde el navegador)

# **5 – Temas**

## Bindings: Formas de obtener información de un componente.

One-way binding Con (String interpolation) Incrustación de texto y manejo de un evento.

Two-way binding usando un Módulo aparte de Angular que facilita el proceso de binding

## Comunicación entre componentes

De padre a hijo: Un mensaje enviado desde el componente app, a otro componente, el componente que recibe el mensaje declara la variable y la anota con @Input en su .ts, se le envía el valor del mensaje desde el app.html. Se envían valores.

De hijo a padre: Ejemplo inverso, desde el hijo hablando al padre. Se envía un evento que puede contener un valor. @Output para declarar el EventEmiter.

## Instalando temas para Angular:

Dentro del Proyecto:

**Angular Material**

```jsx
npm install @angular/cdk –save
```

- (con –save se registra el componente a instalar en el archivo package.json del proyecto)

```jsx
ng add @angular/material
```

(ya tiene el –save)

HammerJS (librería que permite gestionas eventos para Tablet/smartphone ejm: “touch”). En este cao no, por no ser necesario.

Browser Animation: Por defecto Si

- **PrimeNG**
- npm install primeng –save
- npm install primeicons –save

Se agregan los estilos y javascripst en package.json

Se siguen los pasos para agregar un componente

- Bootstrap
- npm install bootstrap jquery popper.js –save
- Se agregan los estilos y javascripst en package.json
- Se hace uso de Bootstrap siguiendo sus reglas de estilos css.

## Routing (Enrutamiento)

Permite dar la apariencia al usuario de estar navegando entre una página y otra.

Se realiza por el archivo creado: app-routing.module.ts  cuando se confirma agregar enrutamiento al proyecto

Consiste en llamar por la barra de url un path y enrutar el contenido de la página a determinado componente.
