Ciclo de vida de los proyectos
==============================

Introducción
------------

En este documento describimos las etapas por las que pasa un proyecto de 
desarrollo de software construido por Yuido.

Preánalisis y presupuesto
-------------------------

El cliente nos propone un proyecto y nos transmite su propósito. Iniciamos
una serie de conversaciones con el fin de entender qué es lo que desea con
exactitud.

El resultado de las conversaciones se materializa en los primeros documentos
del proyecto:

* *Documentación inicial*
* *Preanálisis*
* *Presupuesto económico*

La *Documentación inicial* incluye toda la información que el cliente 
haya entregado en forma de documento y la que Yuido haya recolectado en las 
conversaciones iniciales.

El *Preanálisis* es un documento confeccionado por Yuido en el que se describe
el software a construir con una precisión suficiente como para estimar la
duración y el coste del proyecto.

Por último el *Presupuesto económico* es el documento donde se indica el precio
y una estimación de la duración del proyecto. Cuando, debido a su extensión el
proyecto lo requiera, se hará un desglose por componente.

Análisis y Diseño
-----------------

En este documento se realiza un estudio detallado del proyecto. Para su 
confección se partirá de los documentos de la fase anterior. Incluirá los
siguientes apartados [#f1]_:



* Alcance
* Glosario
* Requisitos generales
* Arquitectura del sistema y funcionalidades
* Arquitectura del software
* Modelo de datos
* Modelo de proceso
* Bocetos de pantallas

En el *Alcance* se realiza una descripción panorámica del proyecto.

En el *Glosario* se definen en orden alfabético los términos clave del proyecto
con el fin de que todos los participantes en él tengan claro qué significa cada
uno de ellos cuando se utilicen a lo largo del documento.

En *Requisitos generales* se enumeran de manera organizada los requisitos que 
se hayan acordado con el cliente en el presupuesto. Lo más probable es que haya
que continuar conversando y aclarando puntos con el cliente para redactar este
apartado. En este punto pueden ser útiles el uso de casos de uso del sistema.

En *Aquitectura del sistema y funcionalidades* se hará una descomposición del 
proyecto en componentes. La función y responsabilidad de cada componente se 
describirá mediante un listado de funcionalidades. También se describirá como 
se relacionan/comunican entre sí. Es importante incorporar un diagrama que ayude
a visualizar el sistema propuesto.

Los componentes propuestos en la *Arquitectura general*, para que sean útiles 
en la construcción del producto, deben ser explicado con más nivel de detalle. Ese es el propósito del apartado *Arquitectura del software*: proponer los
componentes de software que constituyen cada componente del sistema. En este
nivel de descripción se indicará el tipo de cada componente (servidor HTTP,
cliente HTTP, proceso BATCH, API REST, cliente SOAP, aplicación SPA, ....) y
cómo se comunican entre sí y mediante qué protocolos. Para aumentar el nivel de
detalle dado en este apartado, puede ser conveniente añadir las funcionalidades propias de cada componente software.

Los apartados *Arquitectura del sistema y funcionalidades* y *Arquitectura del
software* deben proporcionar una visión del sistema suficientemente precisa como
para comenzar la construcción del mismo. 

Llegados a este punto tenemos el proyecto organizado en una jerarquía de componentes: los componentes del sistema, que a su vez se organizan en 
componentes de software.

.. code-block:: bash

    Sistema
    |
    ` Componentes del sistema
      |
      ` Componentes de software

Las estructuras de datos que usadas por cada componente software se describirán
en el apartado *Modelo de datos*. Se podrán usar diagramas de clases, diagramas
de entidad/relación o lo que sea más adecuado para su expresión. Es importante
explicar el cometido de los atributos de cada entidad, al menos el de aquellos
que sean menos obvios.

Los procesos que se llevan a cabo en cada componente software se describirán 
en el apartado *Modelo de procesos*. Se podrán usar diagramas de flujo, de
secuencia, de colaboración, de estados y cualquier otro tipo que exprese con
claridad el comportamiento de cada componente de software.

En los *Bocetos de pantallas* realizaremos wireframes que ilustren los elementos
de las pantallas de aquellos componentes que requieran GUI [#f2]_ así
como la navegación entre ellas.

Planificación del proyecto
--------------------------

Construcción de la infraestructura para el desarrollo
-----------------------------------------------------

Organización y creación de los repositorios VCS
###############################################

Creación del entorno de preproducción e integración continúa
############################################################







.. rubric:: Notas

.. [#f1] Si el proyecto lo requiere, se añadirán/eliminarán los apartados que
         el analista/diseñador considere. Lo importante es que el resultado 
         sea un documento en el que los planos del producto sirvan de guía 
         fundamental para el desarrollo.
.. [#f2] GUI acrónimo de Grapphical User Interface