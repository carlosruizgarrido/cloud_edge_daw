# # Tarea (a+b) · Cloud: niveles y funciones (DAW 1º)

## 🅰️ Tarea A — Niveles de cloud (IaaS/PaaS/SaaS)
Crea una tabla con 10 servicios reales. Incluye enlace oficial y justifica responsabilidades.

| Servicio | Proveedor | Nivel (IaaS/PaaS/SaaS) | Enlace oficial | ¿Qué gestiona el proveedor? | ¿Qué gestiona el equipo/usuario? |
|---------|----------|-------------------------|----------------|-----------------------------|----------------------------------|
| Amazon EC2 | AWS | IaaS | https://aws.amazon.com/ec2 | Hardware físico, red, virtualización y data centers. | Sistema operativo, parches, aplicaciones y datos. |
| Google Compute Engine | Google Cloud | IaaS | https://cloud.google.com/compute | Infraestructura, red, discos y virtualización. | SO, configuración, aplicaciones y datos. |
| Azure Virtual Machines | Microsoft Azure | IaaS | https://azure.microsoft.com/services/virtual-machines | Servidores físicos, red, almacenamiento base. | Sistema operativo, software y datos. |
| Amazon S3 | AWS | IaaS (Storage) | https://aws.amazon.com/s3 | Infraestructura de almacenamiento, durabilidad y disponibilidad. | Organización, permisos y contenido de los datos. |
| AWS Elastic Beanstalk | AWS | PaaS | https://aws.amazon.com/elasticbeanstalk | Infraestructura, runtime, escalado y balanceo. | Código de la aplicación y configuración lógica. |
| Google App Engine | Google Cloud | PaaS | https://cloud.google.com/appengine | Plataforma de ejecución, escalado automático. | Desarrollo de la aplicación y datos. |
| Heroku | Salesforce | PaaS | https://www.heroku.com | Infraestructura, contenedores y runtime. | Código, dependencias y base de datos. |
| Microsoft 365 | Microsoft | SaaS | https://www.microsoft.com/microsoft-365 | Aplicaciones, servidores, seguridad y actualizaciones. | Contenido, usuarios y configuración. |
| Google Workspace | Google | SaaS | https://workspace.google.com | Aplicaciones, mantenimiento y disponibilidad. | Gestión de usuarios y documentos. |
| Salesforce CRM | Salesforce | SaaS | https://www.salesforce.com | Aplicación completa, infraestructura y seguridad. | Datos de clientes y reglas de negocio. |


## 🅱️ Tarea B — Funciones principales de cloud (arquitectura)
Incluye un diagrama (ASCII/Mermaid/imagen) y una explicación breve.

### Diagrama
graph TD
    Usuario -->|HTTPS| Balanceador
    Balanceador --> VM1
    Balanceador --> VM2
    Balanceador --> VM3

    VM1 --> Almacenamiento
    VM2 --> Almacenamiento
    VM3 --> Almacenamiento

    VM1 --> BaseDatos
    VM2 --> BaseDatos
    VM3 --> BaseDatos

    subgraph Cloud Provider
        Balanceador
        VM1
        VM2
        VM3
        Almacenamiento
        BaseDatos
    end


### Explicación (8–12 líneas)
El usuario accede a la aplicación desde el frontend a través de un navegador web.
La petición viaja por Internet y entra en la cloud mediante un balanceador de carga.
El balanceador redirige la solicitud a una API que se ejecuta en máquinas virtuales o contenedores.
La API procesa la lógica de negocio y valida los datos recibidos.
Si es necesario, la API consulta o guarda información en una base de datos gestionada en la cloud.
También puede almacenar archivos o recursos en un servicio de almacenamiento cloud.
La base de datos y el almacenamiento devuelven la información solicitada a la API.
La API responde al frontend con los datos ya procesados.
La cloud se encarga de la escalabilidad, alta disponibilidad y seguridad de toda la arquitectura.
El equipo de desarrollo solo gestiona el código y la configuración de la aplicación.

### Mapeo de funciones cloud a componentes (mínimo 3)
- **Procesamiento →** Máquinas virtuales o contenedores que ejecutan la lógica de la aplicación (por ejemplo, EC2, Azure VM).
- **Ejecución →** Plataforma de ejecución donde corre el backend o la API (PaaS como App Engine, Elastic Beanstalk).
- **Almacenamiento →** Servicios de almacenamiento persistente para datos y archivos (bases de datos gestionadas y storage de objetos).
- **Intercambio →** Servicios de red y balanceadores de carga que permiten la comunicación entre frontend, API y base de datos.

## 📚 Fuentes (enlaces oficiales)
## 📚 Fuentes (enlaces oficiales)

- Amazon EC2  
  https://aws.amazon.com/ec2/

- Amazon S3  
  https://aws.amazon.com/s3/

- AWS Elastic Beanstalk  
  https://aws.amazon.com/elasticbeanstalk/

- Google Compute Engine  
  https://cloud.google.com/compute

- Google App Engine  
  https://cloud.google.com/appengine

- Azure Virtual Machines  
  https://azure.microsoft.com/services/virtual-machines/

- Microsoft 365  
  https://www.microsoft.com/microsoft-365/

- Google Workspace  
  https://workspace.google.com/

- Heroku  
  https://www.heroku.com/

- Salesforce CRM  
  https://www.salesforce.com/

Carlos Manuel Ruiz Garrido                                                                                                                        19/01/26
