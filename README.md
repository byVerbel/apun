# Aplicación montada con Ruby on Rails

## Tabla de contenidos

- [Hacer que la app funcione](#hacer-que-la-app-funcione)
- [Prerrequisitos](#prerrequisitos)
- [Instalar la app en tu PC](#instalar-la-app-en-tu-pc)
- [Trabajos e idea general del proyecto](#trabajos-e-idea-general-del-proyecto)

## Hacer que la app funcione

Si la app te está dando problemas (te muestra una pantalla azul) simplemente recárgala. Esto debería solucionar el problema, tanto si se abre en el celular como en el PC.

## Prerrequisitos

Para poder instalar la aplicación se tienen algunos "prerrequisitos". Estos son:

1. **Tener Linux:** Tener algún PC con Linux o, si tu PC es Windows, descargar [WSL2](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10) y seguir los pasos de instalación que puedes ver [aquí](https://docs.microsoft.com/en-us/windows/wsl/install) (_este instala una versión de Ubuntu_). Es posible usar Ruby on Rails desde Windows, pero la configuración es más larga y no se encuentra mucha documentación para apps de Rails (en cualquier versión) hechas desde Windows.
2. **Tener instalado Ruby:** Para esto recomiendo la instalación de Ruby con el administrador de versiones _rvenv_. Puedes seguir el tutorial de [GoRails](https://gorails.com/setup/ubuntu/20.04) (_selecciona la versión de ubuntu que instalaste en tu PC para el paso a paso y realiza solamente lo que está en el apartado Installing Ruby_).
3. **Tener instalado Git:** Para esto puedes seguir los pasos que se explican en el libro guía

## Instalar la app en tu PC

Primero necesitas descargar el repositorio en tu PC:

```
$ git clone
```

Ahora instala las gemas necesarias:

```
$ gem install bundler -v 2.3.14
$ bundle _2.3.14_ config set --local without 'production'
$ bundle _2.3.14_ install
```

A continuación, genera la base de datos:

```
$ rails db:migrate
```

Finalmente, corre las pruebas para verificar que todo se ejecuta correctamente:

```
$ rails test
```

Si ningún test falla, estás listo para correr tu app en tu servidor local:

```
$ rails server
```

Para más información mira el libro [_Ruby on Rails Tutorial_](https://www.railstutorial.org/book).

## Trabajos e idea general del proyecto

La idea es crear una página tipo blog para la Cátedra APUN 50-AÑOS, en la cual puedan haber usuarios que suban blogs e interactúen entre si, basándose en las conferencias presentadas durante la cátedra. Para esto, lo ideal sería agregar varias funcionalidades a la página, poco a poco y sin ningún orden en particular, a partir de estas ideas base:

- Creación de blogs.
- Creación de referencias.
- Creación de autoevaluación.
- Creación de usuarios.
- Opción de me gusta a blogs de otro usuario.
- Creación de comentario en blog propio o blog de otro usuario.
- Filtros de blogs respecto a varias características, como:
  - Fecha de publicación del blog.
  - Conferencia en la cual se basa el blog.

Si se logra completar poco a poco estas ideas bases es posible que se obtenga un producto de gran interacción al finalizar el semestre.

Por otro lado, las siguientes son ideas complementarias que se podrían agregar en la página, y es un apartado que se irá actualizando a medida de que se avance en el semestre:

- Subir imágenes en el blog.

A continuación se encuentran los avances de cada trabajo:

1. [Trabajo 1](#trabajo-1)
2. [Trabajo 2](#trabajo-2)
3. [Trabajo 3](#trabajo-3)
4. [Trabajo 4](#trabajo-4)
5. [Trabajo 5](#trabajo-5)

### Trabajo 1

Se hizo un ensayo escrito.

### Trabajo 2

Se hizo un ensayo escrito.

### Trabajo 3

Se inicializó el proyecto con la funcionalidad principal

- Creación de blog referente a la última sesión vista, que cuenta con las siguientes propiedades:
  - Crear título.
  - Crear cuerpo del ensayo.

La base de datos para la realización de este trabajo tendría la siguiente estructura:

![work_3_db](/app/assets/images/db3.png)

##### Referencias

Caballero, A. (2016). _Historia de Colombia y sus oligarquías_. Ministerio de Cultura: Biblioteca Nacional de Colombia.

Cacho, L. (2018). _Esclavas del poder. Un viaje al corazón de la trata sexual de mujeres y niñas en el mundo_. México: DeBolsillo.

Reséndez, A. (2019). _La otra esclavitud. Historia oculta del esclavismo indígena_. México: Grano de Sal/Instituto de Investigaciones Históricas, Universidad Nacional Autónoma de México.

**Nota:** 3.5

### Trabajo 4

Se agregó un ensayo para el Trabajo 3 y para el Trabajo 4, a modo de prueba de la aplicación.

##### Referencias

Damián S., M. C. (2020). _Estudios sobre el medio oriente desde América Latina. Perspectivas desde el sur_. Buenos Aires: CLACSO

Pytel, C., Yurek, J., Marshall, K. (2007). _Pro Active Record: Databases with Ruby and Rails_. Apress.

### Trabajo 5

Se agregó un formulario para la autoevaluación de la cátedra. Se puede crear/editar la autoevaluación ligada a cada uno de los blogs que se hagan.

También se agregaron las bases para agregar referencias a los blogs. Ese será el objetivo del trabajo 6.

La base de datos para la realización de este trabajo tiene la siguiente estructura, hecha con la ayuda de las referencias consultadas:

![work_5_db](/app/assets/images/db5.png)
