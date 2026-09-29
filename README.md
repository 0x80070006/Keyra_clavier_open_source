# Keyra

Clavier Android français avec suggestions, correction, saisie multi-touch et personnalisation.

**État :** application en développement. Des APK sont disponibles, mais ce dépôt contient principalement le module source `src/` : les fichiers Gradle, le wrapper et la configuration racine nécessaires à une compilation directe ne sont pas publiés. Le fonctionnement sur appareil n'a pas été vérifié pendant cet audit.

## Télécharger

- [APK général v3.0](https://github.com/0x80070006/Keyra_clavier_open_source/releases/download/v3.0/Keyra_v3.0.apk)
- [APK v11 pour Pixel 9a](https://github.com/0x80070006/Keyra_clavier_open_source/releases/download/v11/Keyra-Pixel-9a-v11.apk) — build explicitement nommé pour cet appareil ; compatibilité avec d'autres modèles non vérifiée.
- [Toutes les versions](https://github.com/0x80070006/Keyra_clavier_open_source/releases)

Les tags historiques conservent des formats différents. Les nouveaux tags devraient suivre `vMAJEUR.MINEUR.CORRECTIF` et les APK devraient porter le même numéro.

![Logo Keyra](assets/keyra-logo.png)

## Utilisation

Installez un APK depuis la page des releases, activez Keyra dans les réglages de saisie Android, puis sélectionnez-le comme clavier courant. Android affiche un avertissement standard lorsqu'un clavier est activé : lisez la [politique de confidentialité](PRIVACY.md) et vérifiez l'origine de l'APK avant de l'utiliser pour des données sensibles.

## Sources et compilation

- `src/main/java/` : clavier, service de saisie, suggestions et réglages.
- `src/main/assets/` : données linguistiques et licences associées.
- `src/test/` et `src/androidTest/` : tests présents dans le module.

Le dépôt n'est pas compilable directement avec `./gradlew` car il ne contient pas de wrapper Gradle ni de projet Android racine. Pour un fork compilable, il faut d'abord publier ces fichiers depuis le projet de référence et valider un build propre.

## Technologies

Kotlin, Android Input Method Framework, Jetpack Compose pour l'interface de réglages. Les données linguistiques et leurs attributions sont listées dans [src/main/assets/licenses/ATTRIBUTIONS.txt](src/main/assets/licenses/ATTRIBUTIONS.txt).

## Confidentialité

Un clavier peut accéder au texte saisi. La [politique de confidentialité](PRIVACY.md) décrit les objectifs de traitement local ; elle ne remplace pas une vérification indépendante du code et du build.

## Licence

Code sous licence MIT : [LICENSE](LICENSE). Les jeux de données et ressources tierces conservent les licences indiquées dans `src/main/assets/licenses/`.
