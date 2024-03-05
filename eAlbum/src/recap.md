npm i @reduxjs/toolkit react-redux
npm i react-router-dom
npm i axios
npm i react-bootstrap bootstrap
nmp i 

Pour bien comprendre le fonctionnement des side effects avec Redux et l'utilisation des Thunks dans le contexte d'une application front-end connectée à une base de données Firebase, voici quelques explications :

1. **Redux** :
   - Redux est une bibliothèque de gestion d'état pour les applications JavaScript. Il offre un état global géré de manière immuable, permettant ainsi de rendre les données de l'application prévisibles et faciles à gérer.
   - Les side effects, ou effets secondaires, font référence à toutes les opérations asynchrones ou non pures effectuées dans une application Redux, telles que les appels réseau, les lectures/écritures dans une base de données, etc.

2. **Thunks** :
   - Un thunk est une fonction qui enveloppe une expression à évaluer ultérieurement. Dans le contexte de Redux, les thunks sont souvent utilisés pour gérer les opérations asynchrones.
   - Les thunks Redux sont des fonctions intermédiaires qui peuvent être dispatchées comme des actions, mais qui peuvent également effectuer des opérations asynchrones et accéder à l'état Redux actuel.

3. **Firebase** :
   - Firebase est une plateforme de développement d'applications mobiles et web acquise par Google. Elle offre de nombreux services, notamment une base de données en temps réel, un service d'authentification, un hébergement, etc.
   - Dans le contexte d'une application front-end, Firebase peut être utilisé comme une base de données backend pour stocker et récupérer des données de manière asynchrone.

Dans une application front-end utilisant Redux avec Firebase, voici comment cela peut être mis en œuvre :

- Lorsqu'une action est déclenchée dans l'application (par exemple, lorsque l'utilisateur soumet un formulaire), un thunk Redux peut être dispatché pour effectuer une opération asynchrone, telle que l'écriture de données dans Firebase.
- Le thunk peut démarrer en dispatchant une action de chargement pour indiquer à l'interface utilisateur qu'une opération est en cours.
- Ensuite, le thunk effectue l'opération asynchrone, comme l'écriture dans la base de données Firebase.
- Une fois que l'opération est terminée avec succès, le thunk dispatche une autre action pour indiquer que l'opération a réussi et peut mettre à jour l'état Redux en conséquence.
- En cas d'erreur lors de l'opération asynchrone, le thunk peut dispatche une action d'erreur pour informer l'utilisateur de l'échec de l'opération.

En résumé, les thunks Redux sont utilisés pour gérer les opérations asynchrones, telles que les interactions avec une base de données Firebase, dans une application front-end utilisant Redux pour la gestion de l'état. Ils permettent de séparer la logique asynchrone de l'interface utilisateur et de maintenir un flux de données unidirectionnel et prévisible.