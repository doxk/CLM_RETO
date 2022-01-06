# Reto-DevOps CLM
![FELIPE AZUA]

## El reto comienza aquí
Tienes que hacer un **fork** de este repositorio para completar los siguientes retos en tu propia cuenta de `gitlab`. **Siéntete libre de resolver el reto que desees.** La cantidad de retos resueltos nos va a permitir valorar tus habilidades y realizar una **oferta en base a las mismas**.

1. Una vez completado, no olvide notificar la solución al **Carla Santiago (csantiago@clmconsultores.com).**
2. **La solución debe venir bien documentada, ten en cuenta que vamos a ejecutar la solución que nos envies para realizar la evaluación**
3. **Tiempo de solución 3 días**

Si tiene alguna duda, adelante, [abre un issue](https://gitlab.com/clm-public/reto-devops/issues) para hacer cualquier pregunta sobre cualquier reto.

### Reto 1. Dockerize la aplicación

¿Qué pasa con los contenedores? En este momento **(2021)**, los contenedores son un estándar para implementar aplicaciones **(en la nube o en sistemas locales)**. Entonces, el reto es:
1. Construir la imagen más pequeña que pueda. Escribe un buen Dockerfile :)
2. Ejecutar la app como un usuario diferente de root.

docker pull doxk91/reto-devops_web
docker pull doxk91/reto-devops


### Reto 2. Docker Compose


Una vez que haya dockerizado todos los componentes de la API *(aplicación de NodeJS)*, estarás listo para crear un archivo docker-compose, en nuestro equipo solemos usarlo para levantar ambientes de desarrollo antes de empezar a escribir los pipeline. Ya que la aplicación se ejecuta sin ninguna capa para el manejo de protocolo http, añace:

1. Nginx que funcione como proxy reverso a nuesta app Nodejs
2. Asegurar el endpoint /private con auth_basic
3. Habilitar https y redireccionar todo el trafico 80 --> 443

https://github.com/doxk/CLM_RETO.git

### Reto 3. Probar la aplicación en cualquier sistema CI/CD [NO REALIZADO]

### Reto 4. Deploy en kubernetes [NO REALIZADO]

Ya que eres una máquina creando contenedores, ahora queremos ver tu experiencia en k8s. Use un sistema kubernetes para implementar la API. Recomendamos que uses herramientas como Minikube o Microk8s.

Escriba el archivo de implementación (archivo yaml) utilizalo para implementar su API (aplicación Nodejs).

* añade **Horizontal Pod Autoscaler** a la app NodeJS

### Reto 5. Construir Chart en helm y manejar trafico http(s) [NO REALIZADO]

Realmente el pan de cada día es crear, modificar y usar charts de helm. Este reto consiste en:

1. Diseñar un chart de helm con nginx que funcione como proxy reverso a nuesta app Nodejs
2. Asegurar el endpoint /private con auth_basic
3. Habilitar https y redireccionar todo el trafico 80 --> 443

### Reto 6. Terraform [NO REALIZADO]

En estos días en IaC no se habla de más nada que no sea terraform, en **CLM** ya nos encontramos con pipeline automatizados de Iac. El reto consiste en crear un modulo de terraform que nos permita crear un **rbac.authorization de tipo Role** que solo nos permita ver los pods de nuestro **namespace donde se encuentra al app Nodejs**

### Reto 7. Automatiza el despliegue de los retos realizados [NO REALIZADO]

Ya que hoy en día no queremos recordar recetas ni comandos, el reto consiste en **automatizar los retos en un Makefile**, considera especificar cuales son las dependencias necesarias para que tu Makefile se ejecute sin problemas.

**NT:** Se evaluará el orden en el cual se encuentre el repositorio, en el gran universo de aplicaciones que existe hoy en día el orden es un factor importante.
