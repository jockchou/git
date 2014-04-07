# Git en un servidor

A estas alturas, ya podrás realizar la mayor parte de las tareas habituales trabajando con Git. Pero, para poder colaborar, necesitarás tener un repositorio remoto de Git. Aunque técnicamente es posible enviar (push) y recibir (pull) cambios directamente a o desde repositorios individuales, no es muy recomendable trabajar así por la gran facilidad de confundirte si no andas con sumo cuidado. Es más, si deseas que tus colaboradores puedan acceder a tu repositorio, incluso cuando tu ordenador este apagado, puede ser de gran utilidad disponer de un repositorio común fiable. En este sentido, el método más recomendable para colaborar con otra persona es preparar un repositorio intermedio donde ambos tengais acceso, enviando (push) y recibiendo (pull) a o desde allí. Nos referiremos a este repositorio como "servidor Git"; pero en seguida te darás cuenta de que solo se necesitan unos pocos recursos para albergar un repositorio Git, y, por tanto, no será necesario utilizar todo un servidor entero para él.

Disponer un servidor Git es simple. Lo primero, has de elegir el/los protocolo/s que deseas para comunicarte con el servidor. La primera parte de este capítulo cubrirá la gama de protocolos disponibles, detallando los pros y contras de cada uno de ellos. Las siguientes secciones explicarán algunas de las típicas configuraciones utilizando esos protocolos, y cómo podemos poner en marcha nuestro servidor con ellos. Por último, repasaremos algunas opciones albergadas on-line; por si no te preocupa guardar tu código en servidores de terceros y no deseas enredarte preparando y manteniendo tu propio servidor.

Si este es el caso, si no tienes interés de tener tu propio servidor, puedes saltar directamente a la última sección del capítulo; donde verás algunas opciones para dar de alta una cuenta albergada. Y después puedes moverte al capítulo siguiente, donde vamos a discutir algunos de los mecanismos para trabajar en un entorno distribuido.

Un repositorio remoto es normalmente un _repositorio básico mínimo_, un repositorio Git sin carpeta de trabajo. Debido a que dicho repositorio se va a utilizar exclusivamente como un punto de colaboración, no tiene sentido el tener una instantánea de trabajo (snapshot) activa en el disco (checkout); nos basta con tener solamente los propios datos Git. Básicamente, un repositorio básico mínimo son los contenidos de la carpeta '.git', tal cual, sin nada más. 