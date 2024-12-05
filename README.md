# Participantes

-Guaqueta Castro John Eliecer
-Murcia Jimenez Michael Alexander


# IntegracionContinua

Proyecto Docker: Conexión de dos componentes
Este proyecto utiliza Docker para conectar dos componentes: un servicio (Sistema consultas medicas) y una base de datos. Los dos componentes se ejecutan en contenedores separados pero se comunican entre sí a través de una red Docker personalizada.

Componentes

- Servicio Web: Una aplicación que se ejecuta en un contenedor Docker.
- Base de Datos: Un contenedor que ejecuta una base de datos.

Configuración de Integración Continua con Jenkins y Ngrok

- Este proyecto utiliza Jenkins para la integración continua. Para facilitar la accesibilidad a Jenkins desde un entorno externo, se empleó ngrok para exponer el servidor Jenkins local a través de un túnel seguro. A continuación, se describe el proceso de configuración.

Requisitos

Para ejecutar este proyecto, necesitarás tener las siguientes herramientas instaladas:

Jenkins instalado y configurado
- Asegúrate de tener Jenkins instalado localmente. Puedes descargarlo desde su sitio oficial.

Ngrok instalado
- Descarga e instala ngrok desde su sitio oficial.

Puertos configurados
- Verifica que Jenkins esté corriendo en el puerto predeterminado (por ejemplo, localhost:8080).

Docker (y Docker Compose si usas archivos docker-compose.yml).
Docker Compose (opcional, si usas docker-compose.yml para orquestar los contenedores).

Pasos para Configurar la Conexión de Jenkins con Ngrok
Inicia el servidor Jenkins
Asegúrate de que Jenkins esté corriendo localmente en el puerto predeterminado (por ejemplo, localhost:8080):

Copiar código
java -jar jenkins.war
Descarga e instala Ngrok
Si aún no lo tienes instalado, descárgalo desde ngrok.com e instálalo según las instrucciones de tu sistema operativo..

Exponer Jenkins con Ngrok
Usa ngrok para crear un túnel hacia el puerto donde corre Jenkins:

Copiar código
ngrok http 8080
Esto generará una URL pública, que redirige a tu servidor Jenkins local.

Configurar la URL de Jenkins....

Ve a Manage Jenkins > Configure System.
En la sección Jenkins URL, ingresa la URL pública generada por ngrok (por ejemplo, https://abcd1234.ngrok.io).
Guarda los cambios.
Configurar Webhooks (opcional).


