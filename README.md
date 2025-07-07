# Services

Ce dépôt contient la configuration Docker Compose permettant de lancer l'ensemble des services nécessaires au projet **CocoVoit**.

## Prérequis
- [Docker](https://docs.docker.com/get-docker/) installé.
- [windows_exporter](https://github.com/prometheus-community/windows_exporter) (Optionnel) sur votre machine Windows si vous souhaitez superviser l'hôte.

## Démarrage des services
```sh
docker compose up -d
```

## Arrêt des services
Pour arrêter l'ensemble :
```sh
docker compose down
```

Les conteneurs sont ensuite accessibles sur les ports listés ci-dessous. 

## Services inclus
| Service       | Port local | Utilité | Identifiants par défaut |
|---------------|-----------|---------|-------------------------|
| **Prometheus**| 9090      | Collecte des métriques des autres services. | - |
| **Node Exporter**| 9100 | Exporte les métriques système du conteneur hôte. | - |
| **Grafana**   | 3000      | Visualisation des métriques et logs. | `admin1` / `admin1` |
| **Loki**      | 3100      | Stockage centralisé des logs. | - |
| **Alloy**     | 12345     | Envoie les logs Docker vers Loki. | - |
| **Keycloak**  | 8081      | Gestion des utilisateurs/OAuth2. | `admin1` / `admin1` |
| **Kafka**     | 9092      | Broker de messages (mode Kraft). | - |
| **Mailhog**   | 8025 (web) / 1025 (SMTP) | Serveur mail de développement. | - |
| **MySQL**     | 3306      | Base de données principale. | `root` / `cocovoit` |
| **phpMyAdmin**| 8080      | Interface web pour MySQL. | `root` / `cocovoit` |
| **Backend**   | 44318     | API .NET de CocoVoit. | - |
| **Frontend**  | 5173      | Application front Vue.js. | - |

### Utilisateurs préconfigurés dans Keycloak
Le realm `company1` contient notamment :
- utilisateur : `admin-company1` / mot de passe `admin-company1`
- utilisateur : `matnoss@gmail.com` / mot de passe `matnoss@gmail.com`

## Volumes persistants
Les données sont conservées dans des volumes Docker afin de garder la configuration et les données entre les redémarrages :
- `prometheus_data`
- `grafana_data`
- `loki_data`
- `keycloak_data`
- `mysql_data`
- `backend_logs`
- `alloy_logs`

## Ressources
- [Documentation Prometheus](https://prometheus.io/docs/introduction/overview/)
- [Documentation Grafana](https://grafana.com/docs/grafana/latest/)
- [Documentation Loki](https://grafana.com/docs/loki/latest/)
- [Documentation Keycloak](https://www.keycloak.org/documentation.html)
