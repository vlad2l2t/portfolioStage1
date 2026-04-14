
***Tabla de contenidos***
- [[#I - Introducción|I - Introducción]]
		- [[#Problemáticas principales :|Problemáticas principales :]]
		- [[#Presentación de la solución RAFST:|Presentación de la solución RAFST:]]
- [[#II - Respuestas a las problemáticas|II - Respuestas a las problemáticas]]
		- [[#1- Determinar si Meta Quest 3 se integra bien con RAFST|1- Determinar si Meta Quest 3 se integra bien con RAFST]]
		- [[#2- Valor aportado de trabajar con RA/RV en diferentes sectores|2- Valor aportado de trabajar con RA/RV en diferentes sectores]]
			- [[#2- Valor aportado de trabajar con RA/RV en diferentes sectores#Objetivo de formación|Objetivo de formación]]
			- [[#2- Valor aportado de trabajar con RA/RV en diferentes sectores#Reducción de costes|Reducción de costes]]
			- [[#2- Valor aportado de trabajar con RA/RV en diferentes sectores#Demostraciones a clientes|Demostraciones a clientes]]
		- [[#3- Parametrización eficiente de RAFST|3- Parametrización eficiente de RAFST]]
		- [[#4- Comparativo Meta Quest 3 y HoloLens|4- Comparativo Meta Quest 3 y HoloLens]]
		- [[#5- Integración de RV en meetings|5- Integración de RV en meetings]]
		- [[#6- Uso de RA/RV en el ámbito profesional|6- Uso de RA/RV en el ámbito profesional]]
- [[#III - Programar por RA/RV|III - Programar por RA/RV]]
		- [[#1- Unity|1- Unity]]
		- [[#2- Link del MQ3 con Unity|2- Link del MQ3 con Unity]]
- [[#III - Recursas utilizadas y interesantes|III - Recursas utilizadas y interesantes]]


### I - Introducción
##### Problemáticas principales :
- Determinar si Meta Quest 3 se integra bien con Remote Assist y Field Service (y Microsoft Teams, claro).
- ¿Qué está la valor aportado en el mercado por trabajar con RA/RV según los sectores?
- ¿Cómo parametrizar la solución Remote Assist / Field Service / Teams _(RAFST)_ eficientemente?
- ¿El Meta Quest 3 podría ser una alternativa a HoloLens, más barata?
- ¿La integración de AR en meetings podría ser una buena idea?
- Ejemplos de utilización de RA/RV en un contexto profesional.

##### Presentación de la solución RAFST:
- **Remote Assist**
	Funcionalidad de Microsoft Field Service, aplicación de RA (mixta) que permite a los técnicos colaborar con expertos a distancia para arreglar problemas y realizar reparaciones. Permite anotaciones en RA durante videoconferencias, lo que permite a los técnicos recibir orientación en tiempo real de los expertos, incluso si se encuentran geográficamente distantes.
- **Microsoft Dynamics 365 Field Service**
	Servicio incluido en Microsoft Dynamics 365 (licencia requerida, precios disponibles [aquí]([https://www.microsoft.com/en-us/dynamics-365/products/field-service/pricing](https://www.microsoft.com/en-us/dynamics-365/products/field-service/pricing))), que permite automatizar tareas con AI, simplificar el trabajo técnico, beneficiarse de la IA para maximizar la eficiencia, por ejemplo. Ayuda a las empresas a gestionar sus operaciones de servicio de campo, con gestión de órdenes de trabajo, programación de tareas, gestión de activos y herramientas para trabajadores de primera línea.
- **Microsoft Teams**
	Plataforma de colaboración en equipo basada en el cloud, punto central para la comunicación, reuniones y uso compartido de archivos dentro de un equipo.

### II - Respuestas a las problemáticas
##### 1- Determinar si Meta Quest 3 se integra bien con RAFST

Actualmente, hay poca información disponible sobre la integración de Microsoft Remote Assist, Field Service y Teams en el Meta Quest 3. 
Sin embargo, he probado la aplicación ***Microsoft Mesh***, que permite realizar reuniones desde el casco de realidad virtual, basándose en la agenda de Teams.
![[meshdemo.avif|300]]
Los grandes beneficios de esta aplicación son:
- La **interoperabilidad**: se puede hacer una videoconferencia con alguien que está en su PC sin necesidad de que tenga gafas VR. (Es importante saber que si la otra persona tiene gafas, se mostrará su avatar con sus expresiones faciales y corporales en tiempo real).
- La **facilidad de configuración**: la configuración solo requiere iniciar sesión con una cuenta de Microsoft.
- La **posibilidad de participar en varias reuniones al mismo tiempo** : el mundo RV se muestra como una casa, con varias salas. Cada sala corresponde a una reunión, así que si camino de una sala a otra, escucho el sonido de la segunda reunión y ya no se oye la primera. Esto facilita la polivalencia y la *multitarea*.



##### 2- Valor aportado de trabajar con RA/RV en diferentes sectores
###### Objetivo de formación
-  **Formar a los clientes** en el uso de los productos o servicios que ofrece la empresa. Guiar al cliente paso a paso, a través de instrucciones visuales y auditivas, y resolver sus dudas o problemas de forma rápida y eficaz.
-  **Formar a los empleados** en tareas complejas, peligrosas o costosas. Estas tecnologías permiten recrear escenarios reales, con un alto grado de realismo y detalle, y sin riesgos ni consecuencias negativas.
###### Reducción de costes
- Con **Remote Assist**, los técnicos pueden hacer tareas más complejas y las empresas pueden economizar evitando la necesidad de que un experto se desplace al sitio, sino simplemente lo cual indica a los técnicos cómo hacer prácticamente en una videollamada.
- Se puede acceder a las simulaciones remotamente con RV, los empleados ya no necesitarán viajar a la empresa para la formación.
- Prototipos 3D son más fáciles de hacer y visualizar en RV, entonces reduce la necesidad de prototipos físicos, en un sector de diseño por ejemplo
###### Demostraciones a clientes
- El cliente ve a la empresa como una empresa innovadora, que utiliza tecnologías recientes y avanzadas.
- La RV da a los clientes experiencias de productos atractivas y memorables: cuando te pones un casco de RA/RV, lo recordarás.
- Posibilidad de hacer demostraciones remotas, con múltiples clientes conectando a solo una reunión.


##### 3- Parametrización eficiente de RAFST

Actualmente hay poca información disponible sobre este mercado, así que no he podido probar la configuración de estas soluciones.
##### 4- Comparativo Meta Quest 3 y HoloLens

|                       | Meta Quest 3                                                                | HoloLens 2                            |
| --------------------- | --------------------------------------------------------------------------- | ------------------------------------- |
| Precio                | ***~500€***                                                                 | ~3500€                                |
| Resolución            | ***2064x2208 por ojo (9.11 million pixels)***                               | 1440x936 por ojo (2.7 million pixels) |
| Campo visual          | ***H 110°  V 96°  D desconocido***                                          | H 43°  V 29°  D 52°                   |
| Seguimiento visual    | No                                                                          | ***Si***                              |
| Seguimiento manual    | Si                                                                          | Si                                    |
| Seguimiento corporal  | ***Si***                                                                    | No                                    |
| Mando                 | ***Si***                                                                    | No                                    |
| Tipo de visualización | LCD                                                                         | LBS (LCD laser)                       |
| Peso                  | ***515 gramos***                                                            | 565 gramos                            |
| Procesador            | ***En Azul sobre el esquema***<br>![[comparacionProcesadorMQ3HL2.png\|200]] | En Rojo sobre el eschema              |
| Memoria               | ***DRAM 8Gb***                                                              | DRAM 4Gb                              |
Meta Quest 3 (MQ3) puede ser un serio competidor a los Microsoft HoloLens 2 (HL2), pero hay que comprender que no están la misma cosa : HL2 es un dispositivo de RA solamente, mientras que MQ3 es RA y RV. HoloLens no puede crear un entorno totalmente virtual, pero MQ3 lo pueden.

##### 5- Uso de RA/RV en el ámbito profesional
A ver con https://mimbus.com/, si se puede comprar una licencia.

### III - Programar por RA/RV
##### 1- Unity
Descarga Unity Hub y créate una cuenta. Descarga una versión **'LTS'** de Unity, ya que el soporte a largo plazo es importante al desarrollo de un proyecto. Activa el **'Android Build Support'** (OpenJDK / Android SDK & NDK Tools) porque el MQ3 que vamos a usar está basado en Android. Si quieres programar para Apple Vision Pro, activa el soporte para iOS.
Eliges el template 'Universal 3D Core', ya que el template de RV no es el mejor para aprender a programar para RV.
Una vez en el proyecto, descargas 'XR Plugin Management', con el 'Plug-in provider' **Open XR**. Oculus está más adaptado al MQ3, pero Open XR es la mejor opción para la durabilidad a largo plazo y la variedad de soporte.
En la configuración de OpenXR, añade el 'Perfil de Interacción' para MQ3, específicamente *'Meta Quest Touch Pro Controller Profile'*. Haz lo mismo en la parte de Android.
En el 'Package Manager', instalas el **'XR Interaction Toolkit'** que ofrece Unity. Es gratuito, a diferencia de, por ejemplo, Hurricane VR, que es más preciso y complicado, pero para un proyecto sencillo, el XR Toolkit de Unity será suficiente. Descargas también en la sección de 'Samples', los **'Starter Assets'**.
De vuelta a la escena principal, y en el árbol del proyecto, en 'Assets'>'Samples'>'XR Interaction tools'>'3.0.4'>'Starter Assets', haz doble clic en "Demo Scene". Esta es una escena de demostración, donde puedes hacer pruebas, probar las diferentes interacciones, etc.

##### 2- Link del MQ3 con Unity
Detallada documentación disponible aquí:  [VR Developer environment setup for Unity by Meta](https://developers.meta.com/horizon/documentation/unity/unity-env-device-setup/#development-environment-setup)

Si la aplicación Meta Quest Link no funciona (como me pasó a mí), aquí hay un segundo método, un poco más complicado:
- Activar el modo desarrollador en las gafas, a través de la configuración.
- Instalar SideQuest y crear una cuenta desde el ordenador, siguiendo [ese tutorial](https://www.youtube.com/watch?v=wNku19Hl9Dw) 
- En Unity, 'Build' el proyecto y selecciona la escena que quieres probar. Build como un APK
- En la aplicación de PC Sidequest, transfiere el archivo APK al visor (debe estar conectado).
- Luego, la aplicación se puede encontrar en la carpeta "Orígenes desconocidos".

### IV -Funcionalidades útiles para el showroom


### III - Recursas utilizadas y interesantes

[Utilización practica por un técnico en video](https://www.youtube.com/watch?v=IuSFDPziPB8)
[Pagina de presentación de Dynamic 365 por Microsoft ](https://www.microsoft.com/en-us/dynamics-365/products/field-service#model-7)
[Paseo guiado de Microsoft Field Service](https://guidedtour.microsoft.com/es-es/guidedtour/dynamics/field-service/1/1)
[Remote Assist in Dynamics 365 example](https://www.youtube.com/watch?v=Z80gu7mA2NM)
[Los beneficios de la realidad virtual y la realidad aumentada para las empresas](https://www.imagar.com/informatica/los-beneficios-de-la-realidad-virtual-y-la-realidad-aumentada-para-las-empresas/)
[Cambios y repercusiones causados por la RE en el lugar de trabajo](https://courses.minnalearn.com/es/courses/emerging-technologies/extended-reality-vr-ar-mr/xr-and-new-job-roles/)
[Introduction to VR programming in an hour](https://www.youtube.com/watch?v=kbBYcVrGZus&ab_channel=FistFullofShrimp)
[Guía de realidad virtual y aumentada con ejemplos desde 0 hasta aplicaciones avanzadas](https://impulso06.com/guia-de-realidad-virtual-y-aumentada-con-ejemplos-desde-0-hasta-aplicaciones-avanzadas/)
[VR Developer environment setup for Unity by Meta](https://developers.meta.com/horizon/documentation/unity/unity-env-device-setup/#development-environment-setup)
<details>  
<summary>Descripción del proyecto para el showroom</summary>  
Meta Quest 3 ofrece un nuevo mundo a las empresas. Las herramientas de Microsoft, como Field Service y Remote Assist, combinadas con la realidad aumentada y virtual, optimizan el trabajo a distancia, la formación y la demostración de productos. Esto reduce los costes y mejora la eficiencia, transformando el mundo laboral con nuevas formas de interacción y aprendizaje.
</details>



xavier.tejero.ayesa
creacion de avatar
Ayesa_Meta_2025
MIMBUS industry