# demo-cicd : démo CI/CD de 15 minutes

Pipeline GitHub Actions : CI (build Maven + tests JUnit) puis CD (image Docker publiée sur ghcr.io).

## Avant la démo
1. Créer un dépôt GitHub public `demo-cicd`, y pousser ce projet (branche `main`).
2. Vérifier que le pipeline est vert (onglet Actions).

## Déroulé
1. Changer le message dans `App.java`, commit, push : pipeline vert.
2. Casser `add` (`return a - b;`), commit, push : CI rouge, CD bloqué.
3. Corriger (`return a + b;`), commit, push : pipeline vert.
4. Onglet Packages : image `demo-cicd` publiée. Bonus : `docker run ghcr.io/<pseudo>/demo-cicd:latest`
