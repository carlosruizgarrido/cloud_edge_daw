# Tarea (c+d+e) · Edge, Fog, Mist y Cloud (DAW 1º)

## 🅲 Tarea C — Edge Computing y relación con Cloud
**Definición (3–5 líneas):**
Edge Computing se refiere al procesamiento de datos más cerca de la fuente de origen, como dispositivos o sensores, en lugar de depender exclusivamente de servidores centralizados en la nube. Esto permite una mayor eficiencia, menor latencia y optimización en el uso del ancho de banda. La relación con la computación en la nube radica en que, mientras el edge realiza tareas locales de procesamiento, la nube actúa como un almacenamiento o plataforma de procesamiento más potente y centralizado, trabajando de manera complementaria.

**Relación Edge ↔ Cloud (5–8 líneas):**
La relación entre Edge Computing y Cloud Computing es complementaria y se basa en un modelo híbrido que maximiza la eficiencia y el rendimiento. Edge Computing permite procesar los datos en el lugar donde se generan, reduciendo la latencia y el uso del ancho de banda, mientras que la nube proporciona almacenamiento masivo y capacidades de procesamiento de alto nivel. El edge realiza tareas de procesamiento en tiempo real o local, mientras que la nube puede encargarse de análisis más complejos, almacenamiento a largo plazo o decisiones estratégicas basadas en grandes volúmenes de datos. Esta sinergia optimiza tanto la velocidad como la escalabilidad, permitiendo a las organizaciones gestionar grandes cantidades de datos distribuidos de manera eficiente.

**Ejemplo real:**
Un ejemplo real de la relación entre Edge Computing y Cloud Computing es el caso de los vehículos autónomos. Los sensores y cámaras en el vehículo generan grandes cantidades de datos en tiempo real, como la detección de obstáculos, señales de tráfico y condiciones de la carretera. Estos datos se procesan localmente en el vehículo (en el edge) para tomar decisiones inmediatas, como frenar o cambiar de dirección.

Sin embargo, para análisis más complejos, como el aprendizaje automático para mejorar los algoritmos de conducción o la recopilación de datos de todos los vehículos para detectar patrones globales, los datos se envían a la nube. Allí, se procesan a gran escala y se actualizan los modelos que luego se envían de vuelta al vehículo para mejorar su rendimiento. Esta integración entre edge y cloud permite a los vehículos autónomos tomar decisiones rápidas y precisas mientras optimiza el uso de recursos en la nube para tareas más intensivas.

**Fuentes oficiales (mín. 2):**
- Gartner: Según el informe de Gartner sobre "Edge Computing", la adopción de esta tecnología está acelerando debido a la necesidad de procesamiento de datos más rápido y eficiente cerca del origen de los mismos, complementando la infraestructura en la nube para una mayor escalabilidad y optimización de recursos. (Fuente: Gartner, "Edge Computing Will Accelerate the Cloud's Evolution", 2020)

- Amazon Web Services (AWS): AWS ofrece soluciones de Edge Computing a través de su plataforma AWS IoT Greengrass, la cual permite ejecutar funciones de computación, análisis y almacenamiento en dispositivos locales, mientras mantiene una conexión con la nube para gestión, análisis global y almacenamiento a largo plazo. (Fuente: AWS, "What is AWS IoT Greengrass", 2023)

## 🅳 Tarea D — Fog vs Mist (niveles y zonas de aplicación)
**Definición Fog (2–4 líneas):**
El Fog Computing es un modelo de computación descentralizado que extiende los servicios de la nube hacia el borde de la red, procesando los datos de manera más cercana al usuario o dispositivo. A diferencia del Edge, el Fog puede involucrar múltiples capas de procesamiento entre los dispositivos finales y la nube, mejorando la eficiencia y reduciendo la latencia en aplicaciones como IoT y redes inteligentes.

**Definición Mist (2–4 líneas):**
Mist Computing es un modelo de computación que lleva aún más cerca del dispositivo final el procesamiento de datos, generalmente en los propios sensores o dispositivos de bajo nivel. Es una extensión del Fog Computing, pero se enfoca en la computación a nivel de red de acceso, proporcionando un procesamiento extremadamente cercano a los usuarios o sistemas finales, con el objetivo de minimizar la latencia y el uso de ancho de banda.

**Esquema (ASCII o Mermaid recomendado):**
graph LR
    A[Nube (Cloud)] --> B[Fog Computing]
    B --> C[Mist Computing]
    C --> D[Dispositivos finales (Sensores/Actuadores)]

    A -.-> E[Almacenamiento a largo plazo]
    B -.-> F[Procesamiento de datos en capas intermedias]
    C -.-> G[Procesamiento local cercano al dispositivo]
    
    style A fill:#e3e3e3,stroke:#333,stroke-width:2px
    style B fill:#f9f9f9,stroke:#333,stroke-width:2px
    style C fill:#f1f1f1,stroke:#333,stroke-width:2px


**Zonas de aplicación (qué hace cada capa):**
- Mist →  La capa de Mist se enfoca en el procesamiento extremadamente cercano a los dispositivos finales, como sensores o actuadores. Su principal función es reducir la latencia al mínimo posible, realizando tareas como la captura y procesamiento de datos en tiempo real a nivel local. Es útil para aplicaciones que requieren decisiones instantáneas, como dispositivos IoT, wearables, vehículos autónomos, y sistemas de control industrial.
- Edge →  El Edge Computing realiza el procesamiento de datos cerca de la fuente, pero no necesariamente a nivel del dispositivo más básico como en Mist. Su función es tomar decisiones rápidas y procesar datos en tiempo real, pero con una capacidad mayor que Mist. Es ideal para aplicaciones que requieren baja latencia, pero también un poco más de poder de cómputo, como cámaras inteligentes, dispositivos conectados en hogares inteligentes, y sistemas de monitoreo de salud.
- Fog →  El Fog Computing actúa como una capa intermedia entre el Edge y la Nube. Se encarga de procesar, almacenar y analizar datos a nivel de red, distribuyendo tareas entre los dispositivos locales y la Nube. Es ideal para aplicaciones como redes de ciudades inteligentes, vehículos conectados, sistemas de manufactura avanzados y gestión de redes eléctricas inteligentes, donde se necesita un procesamiento distribuido y escalable.
- Cloud →  La Nube es donde se realizan las tareas de procesamiento y almacenamiento de gran escala. En esta capa, se gestionan grandes volúmenes de datos y se realizan análisis complejos o entrenamiento de modelos de inteligencia artificial. Es la plataforma que proporciona recursos ilimitados en términos de almacenamiento y potencia de procesamiento. Se utiliza en aplicaciones como análisis de grandes datos, backups, servicios de software a demanda (SaaS), y desarrollo de aplicaciones a gran escala.

## 🅴 Tarea E — Ventajas de la Cloud en sistemas conectados
Incluye mínimo 3 ventajas (recomendado 5), con explicación + ejemplo.

1) Ventaja: Escalabilidad
   Explicación: La nube ofrece una capacidad casi ilimitada de almacenamiento y procesamiento de datos. Esto significa que los sistemas conectados pueden adaptarse rápidamente a cambios en la demanda sin necesidad de inversiones significativas en infraestructura física.
   Ejemplo: En una ciudad inteligente, el sistema de gestión del tráfico puede procesar datos de miles de sensores y cámaras. A medida que crece la cantidad de datos, la nube permite agregar más recursos sin que los administradores tengan que preocuparse por el mantenimiento de servidores locales.

2) Ventaja: Acceso remoto y disponibilidad
   Explicación: Los servicios en la nube permiten acceder a los datos y aplicaciones desde cualquier lugar con conexión a internet. Esto facilita la supervisión, el control y la gestión de sistemas conectados de manera remota y continua.
   Ejemplo: Un agricultor que utiliza sensores IoT para monitorear su campo puede acceder a los datos de humedad y temperatura en tiempo real desde su teléfono móvil, sin importar su ubicación, gracias a los servicios en la nube.

3) Ventaja: Mantenimiento y actualizaciones automáticas
   Explicación: Los proveedores de servicios en la nube se encargan de las actualizaciones y el mantenimiento de la infraestructura, lo que asegura que los sistemas conectados siempre estén operando con la última versión de software y parches de seguridad.
   Ejemplo: Un sistema de gestión de energía en una fábrica que utiliza la nube puede recibir actualizaciones automáticas de seguridad y nuevas funcionalidades sin necesidad de intervención manual, asegurando la continuidad operativa sin interrupciones.

**Fuente oficial (mín. 1):**
- Una fuente oficial que respalda estas ventajas de la nube en sistemas conectados es el informe de **Amazon Web Services (AWS)**, que describe cómo la infraestructura en la nube permite escalabilidad, accesibilidad remota, procesamiento de grandes volúmenes de datos y seguridad avanzada para aplicaciones IoT. (Fuente: AWS, "The Benefits of Cloud Computing for IoT", 2023)

## 📚 Fuentes (enlaces oficiales)
(Recopila aquí todos los enlaces oficiales usados)

1. AWS - The Benefits of Cloud Computing for IoT
   [https://aws.amazon.com/iot/](https://aws.amazon.com/iot/)

2. Gartner - Edge Computing and Cloud Integration
   [https://www.gartner.com/en/newsroom/press-releases/2020-05-21-gartner-forecasts-global-edge-computing-market-to-reach-11-6-billion-in-2023](https://www.gartner.com/en/newsroom/press-releases/2020-05-21-gartner-forecasts-global-edge-computing-market-to-reach-11-6-billion-in-2023)

3. AWS IoT Greengrass
   [https://aws.amazon.com/iot/greengrass/](https://aws.amazon.com/iot/greengrass/)

Estas fuentes proporcionan información detallada sobre las ventajas y aplicaciones de la computación en la nube, así como su relación con tecnologías como el Edge y el IoT.

Carlos Ruiz Garrido 02/02/2026
