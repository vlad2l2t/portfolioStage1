Introduit dès le premier jour, le [[26-05]]. 
Terminé le [[27-05]]. Validé par le tuteur le [[28-05]].

***Sommaire***
- [[#Présentation du projet|Présentation du projet]]
		- [[#Ressources intéressantes concernant le projet|Ressources intéressantes concernant le projet]]
		- [[#Ressources mises à ma disposition :|Ressources mises à ma disposition :]]
- [[#Tâches assignées (et effectuées)|Tâches assignées (et effectuées)]]

# AlertMine - Application d'alertes en milieu minier

### Présentation du projet
En milieu minier, les ouvriers font face à un bruit énorme. Ainsi, pour les contacter, cela est parfois difficile. Ayesa a donc trouvé une solution plutôt innovante : une application mobile dynamique reliée à une application web permettant au poste de contrôle d'envoyer des notifications visuelles personnalisées sur le mobile des employés.
L'objectif est d'améliorer les mesures de sécurité, pour prévenir les employés en cas d'urgence (fuite de gaz, incendie ou autre).

##### Ressources intéressantes concernant le projet
***Description faite par l'entreprise de développement :***
La solution AlertMine offre une fonctionnalité de communication avec des appareils Android, permettant l'envoi d'alertes depuis le back-office aux mineurs sur-place, contribuant ainsi à garantir la sécurité des travailleurs en cas d'urgence.
Les alertes sont mises en évidence par des couleurs configurables pour une notification et une visualisation immédiates. La lisibilité et la compréhension des informations seront privilégiées, même dans des conditions environnementales défavorables, grâce à de grandes commandes tactiles et des boutons intuitifs.
Les options de sélection des destinataires et de configuration de la diffusion sont présentées de manière interactive et visuellement attrayante dans le back-office.
Un historique des alertes clairement organisé est disponible dans l'application mobile et le back-office.
L'objectif final de la phase 1 de développement est de fournir un système complet d'alerte et de communication conçu pour améliorer la sécurité et l'efficacité des interventions d'urgence dans les environnements miniers, en limitant sa portée aux fonctionnalités de base pour la gestion des données nécessaires à l'utilisation du système (utilisateurs, profils, appareils, etc.), ainsi qu'en permettant l'envoi d'alertes aux appareils mobiles Android, confirmant ainsi sa viabilité technique et fonctionnelle, , ainsi qu'en évaluant de nouvelles phases et portées de développement évolutif ultérieur.
*Toutes les ressources concernant l'analyse du projet sont à retrouver dans le document "PACE_AlertMine_Documento de análisis y diseño_Vers.1.1.pdf".*

***Diagramme organisationnel et coûts prévisionnels :***
![[ganttAlertMine.png|500]]

***Schéma de l'architecture de l'application :***
![[arquitecturaAlertMine.png|500]]
***Infrastructure de l'application :***
![[arquitecturaRedAlertMine.png|500]]

***Interface web :***
![[interfazWebAlertMine.png|500]]
***Interface mobile :***
![[interfazMovilAlertMine.png|200]]

***Modèle de données de la solution :***
![[modeloDeDatos.png|500]]

##### Ressources mises à ma disposition :
- Diaporama de présentation du projet
- 3 vidéos *(total ~45min)*
	- Démonstration
	- Présentation technique côté Web
	- Présentation technique côté mobile (Android Studio)
- Documentation d'analyse / de design
- Cahier des charges du projet

### Tâches assignées (et effectuées)

J'ai d'abord **visionné toutes les ressources** mises à ma disposition, en commençant par le diaporama de présentation, puis la vidéo de démonstration, les deux vidéos de présentation et enfin la documentation analytique et de design.
Einstein disait "Si vous ne pouvez pas expliquer un sujet à un enfant de six ans, vous ne le comprenez pas". Ainsi j'ai commencé la **rédaction du document récapitulatif du projet**, en rassemblant les ressources qui me semblaient les plus pertinentes parmi celles fournies. Cela m'a permis d'avoir une vision plus globale du projet, et de comprendre plus précisément au fur et à mesure de la rédaction. 
J'ai **appris** certaines choses lors de la lecture des documentations, comme par exemple beaucoup de choses sur le développement d'applications mobiles avec Kotlin ou les API liant la BDD et la solution, ou même des termes professionnels comme POC (Proof Of Concept) ou PACE (Parcours d'Acquisition de Compétences en Entreprise). J'en ai **approfondi** d'autres, telles que les notions d'API et de WebSocket. Je me sentais **en confiance sur certains sujets** lors de la démonstration en m'imaginant clairement comment coder telle ou telle fonctionnalité avec les compétences développées en cours : récupération de valeurs dans la BDD, script de connexion, login, hachage etc.
Après plusieurs **réunions** avec le développeur le [[27-05]] *(voir cette page pour plus de détails)*, j'ai attaqué la **rédaction** de la documentation de mise en place, et l'ai terminée ce même jour. Je l'aie ensuite envoyée à mon tuteur pour **vérification**.
Après validation, je l'**imprime** et la positionne dans la salle de showroom, pour que la prochaine fois que l'application doit être présentée à un client, le technicien chargé de l'installation ait une documentation avec une marche à suivre détaillée à disposition.
Ensuite, le [[29-05]], je confectionne la **fiche descriptive du projet**, que j'imprime et que je place dans un cadre de présentation.

***Document final produit :***
[[AlertMine - Documentación de implementación en el showroom.pdf]]




