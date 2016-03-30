**Estructura del modulo**

> odoo.py scaffold <module name> <where to put it>
> en nuestro caso...
>  odoo.py scaffold openacademy addons

**Definición del modelo**

> se define un nuevo curso de datos en el módulo openacademy, con su título y descripción.

**Creación del formulario XML**

> se crea la propia vista de formulario para el objeto del curso. Los datos que se muestran son el nombre y laa descripción del curso.

**Campo de busqueda**

> Se crea un campo de búsqueda según su título o su descripción.

**Creación de la clase session**

> Se crea la clase session, contiene un nombre, una fecha de inicio, una duración y un numero de asientos. Se añade una acción y un menú para que se muestren.

**Campos relacionados**

> El uso de un **many2one**, modificar los modelos de golf y Session para reflejar su relación con otros modelos:
>Un curso tiene un usuario responsable; el valor de ese campo es un registro de los modelos incorporados en res.users .
>Una sesión tiene un instructor; el valor de ese campo es un registro del modelo integrado de res.partner .
>Una sesión se relaciona con un curso; el valor de ese campo es un registro de modelo openacademy.course y es necesario.
>Adaptar los puntos de vista.
>Utilizando el inverso **one2many** campo relacional, modifica los modelos para reflejar la relación entre los cursos y sesiones.

**relaciones múltiples**
>Utilizando el Many2Many campo relacional, se modifica el modelo de sesión para cada sesión.
>Los asistentes estarán representados por los registros de socios, por lo que se relacionan con el modelo incorporado en res.partner.


**Herencia**
>Se utiliza el modelo de herencia para modificar el modelo socio existente y agregar un instructor, el campo Many2Many corresponde a la relación de sesión socio
>Se usa la vista de la herencia, que se vea que estas casillas en la vista formulario de empresa
>Al seleccionar el instructor para una sesión , sólo éste será visible.

**Dominios mas complejos**
> Se crean nuevas categorías asociadas Maestro / Nivel 1 y Maestro / Nivel 2 para que una sesión pueda tener un instructor o un maestro de cualquier nivel.

**Valores por defecto**
> Se definen valores predeterminados como fecha_inicial
> se añade un campo activo en la sesión de clase y se establecen sesiones como activas por defecto.

**Onchange**
> se usa para advertir sobre valores no válidos, como un número negativo de asientos o demasiados participantes en comparación con los asientos, es decir, asiste mas gente de los asientos que se pueden ocupar.

