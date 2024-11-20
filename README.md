
# Gestion des Comptes Bancaires avec Spring Boot et React

Ce projet est une application simple de gestion des comptes bancaires. Il utilise **Spring Boot** pour le backend et **React** pour le frontend.


## **Fonctionnalités**
- Affichage de la liste des comptes bancaires.
- Ajout de nouveaux comptes bancaires.
- Modification des comptes existants.
- Suppression de comptes.
- Interface utilisateur moderne et intuitive avec React.


## **Structure du projet**

### **Backend (Spring Boot)**
Le backend est construit avec Spring Boot et propose une API REST pour gérer les comptes bancaires.

#### **API REST**
| Méthode HTTP | Endpoint                | Description                  |
|--------------|-------------------------|------------------------------|
| `GET`        | `/banque/comptes`       | Récupérer tous les comptes.  |
| `GET`        | `/banque/comptes/{id}`  | Récupérer un compte par ID.  |
| `POST`       | `/banque/comptes`       | Ajouter un nouveau compte.   |
| `PUT`        | `/banque/comptes/{id}`  | Modifier un compte existant. |
| `DELETE`     | `/banque/comptes/{id}`  | Supprimer un compte.         |

---

### **Frontend (React intégré dans HTML)**
Le frontend est écrit en React et intégré directement dans un fichier HTML. Il permet une interaction dynamique avec le backend via des requêtes REST.


## **Prérequis**
- **Java 17** ou version supérieure.
- **Maven** installé.
- Un navigateur web moderne pour l'affichage de l'interface.

## **Installation**

1. **Configuration du backend :**
   - Assurez-vous que le fichier `application.properties` dans `src/main/resources` est configuré comme suit :
     ```properties
     spring.application.name=spring
     spring.datasource.url=jdbc:h2:mem:banque
     spring.datasource.driverClassName=org.h2.Driver
     spring.datasource.username=sa
     spring.datasource.password=
     spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
     spring.h2.console.enabled=true
     spring.h2.console.path=/h2-console
     server.port=8082
     spring.jpa.hibernate.ddl-auto=update
     ```

3. **Lancez l'application :**
   - À la racine du projet, exécutez la commande suivante :
     ```bash
     mvn spring-boot:run
     ```

   - Cela démarre le backend sur le port **8082**.

4. **Accédez à l'application :**
   - Ouvrez un navigateur et rendez-vous sur **[http://localhost:8082](http://localhost:8082)**.

## **Utilisation**

### **Interface utilisateur**
1. **Page d'accueil :**
   - Sur **http://localhost:8082**, une page d'accueil s'affiche avec un bouton pour accéder à la liste des comptes.

2. **Liste des comptes :**
   - Affiche tous les comptes enregistrés.
   - Chaque ligne contient des boutons pour modifier ou supprimer un compte.

3. **Ajouter un compte :**
   - Cliquez sur **Ajouter un compte** pour afficher un formulaire.
   - Remplissez les champs requis et cliquez sur **Ajouter**.

4. **Modifier un compte :**
   - Cliquez sur **Modifier** à côté d'un compte pour préremplir le formulaire avec les données existantes.
   - Apportez vos modifications et cliquez sur **Mettre à jour**.

5. **Supprimer un compte :**
   - Cliquez sur **Supprimer** pour effacer un compte.

## **Technologies utilisées**

- **Backend :**
  - Java 17
  - Spring Boot 3
  - Spring Data JPA
  - H2 Database

- **Frontend :**
  - React (intégré via un fichier HTML)
