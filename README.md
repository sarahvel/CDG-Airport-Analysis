## Projet d’analyse – Aéroport Paris Charles de Gaulle (CDG)

#### Contexte

L’aéroport Paris Charles de Gaulle (CDG) est l’un des principaux hubs européens.
Ce projet analyse les retards, la congestion, l’allocation des ressources et leur impact économique à partir de données opérationnelles réelles.

#### Problématique

Comment l’aéroport CDG peut-il mieux anticiper les pics de passagers et les perturbations (retards, météo) afin d’optimiser ses ressources et réduire les pertes économiques ?

#### Note sur les retards

Dans le secteur aérien, un vol est considéré comme en retard lorsqu’il présente un décalage d’au moins 15 minutes par rapport à l’horaire prévu.
Dans cette analyse, un retard correspond donc à un vol partant avec minimum 15 minutes de retard.

#### Fichiers de données

Raw_Flight_Data.csv : Infos vols (horaires, terminaux, causes de retards)
Passenger_Flow_Data.csv : Flux passagers (temps d'attente, files)
Weather_Impact.csv : Météo (visibilité, vent, conditions de piste)
Ressources.csv : Personnel et équipements (shifts, taux d'utilisation)
Financial_Transactions.csv : Flux financiers par terminal


#### Méthodologie

- **Nettoyage** : Standardisation des formats (dates, terminaux, espaces) et gestion des types.
- **Analyse Retards** : Segmentation par durée, cause et plages horaires.
- **Congestion** : Calcul d'un score combinant temps d'attente et longueur des files.
- **Ressources** : Vérification de l'adéquation effectifs/trafic via le taux d'utilisation.
- **Finance** : Évaluation de l'impact financier des perturbations par terminal.


#### Résultats clés

- Les ressources sont suffisantes mais pourraient être mieux organisées et synchronisées avec les perturbations
- Les retards sont structurels et récurrents
- 28% des vols en retard en moyenne, avec des retards longs (≈90 min)
- 65 % des coûts de retard proviennent de défaillances internes sur 7 terminaux sur 8
- Les retards les plus longs surviennent en soirée et la nuit
- Il existe une forte disparité financière entre terminaux (désalignement coûts de retards / revenus)


#### Message clé

CDG ne souffre pas d’un manque global de ressources, mais d’un problème d’anticipation, de synchronisation et de ciblage des efforts.

Une gestion prédictive, différenciée par terminal et par plage horaire est la clé pour améliorer la performance opérationnelle et financière.


#### Conclusion globale

L'analyse approfondie de l'aéroport Charles de Gaulle révèle une situation paradoxale : les retards ne sont pas causés par un manque global de ressources, mais par un problème structurel d'anticipation, de coordination et d'allocation.

Les causes sont multifactorielles :

- retards massifs et récurrents révélant un dysfonctionnement structurel plutôt qu'un incident ponctuel
- dysfonctionnements internes : 7 terminaux sur 8 ont au moins 65% de leurs pertes liées à des causes internes (Technical, Security, Ground Handling, Operational et Crew)
- facteurs externes majeurs (météo, ATC) mais jouant un rôle secondaire, sauf sur le terminal 2C
- désalignement temporel critique : décalage entre l'accumulation des retards et la mobilisation des ressources. Les ressources existent, mais ne sont pas déployées au bon moment


Sur le plan de l'expérience passager, la congestion est davantage liée à l’organisation du staffing qu’au volume de trafic. Les processus d’immigration constituent un goulot d’étranglement majeur.  
Par ailleurs, la corrélation quasi nulle entre temps d’attente et revenus indique que l’amélioration de l’expérience passager est un enjeu qualitatif, mais pas un levier direct de chiffre d’affaires à court terme.

D’un point de vue financier, il existe de fortes disparités entre les terminaux.
La création de valeur est concentrée sur quelques terminaux (2C, 1), tandis que les coûts de retard sont particulièrement élevés sur 2B, 2A et 2C. 
La matrice de priorisation montre que rentabilité et efficacité opérationnelle ne sont pas alignées, ce qui révèle un fort potentiel d’optimisation.

#### Recommandations stratégiques

**1) Pilotage en temps réel**

**Objectif** : Passer d'une gestion réactive à une gestion anticipative des perturbations

- Mettre en place Centre de contrôle opérationnel intégrant météo, flux passagers et ressources disponibles pour anticiper l’effet domino des retards
- Développer des scénarios météo opérationnels (vent, visibilité, neige)
- Déclencher les plans d'action en amont au lieu de réagir après coup (équipes piste, maintenance, exploitation)

**2) Réallocation dynamique des ressources**

- Renforcer les effectifs sur les plages critiques (matin, soirée)
- Créer des équipes de réserve mobiles activables en cas de perturbation

**3) Priorités par terminal**

- 2B, 2A, 3 : audit complet des processus internes et refonte organisationnelle
- 2C : anticipation météo renforcée et coordination ATC
- 2E : optimisation immigration et gestion des pics long-courriers (effectifs renforcé aux heures de pointe, déploiement bornes automatisées, fast-track biométrique)
- 1 & 2F : gestion proactive de la congestion (fluidification des flux)

**4) Optimisation de l’expérience passager**

- Renforcer les effectifs aux process critiques (immigration)
- Déployer des outils de prédiction de files
- Communication proactive vers les passagers en période de perturbation

**5) Stratégie financière**

- Prioriser les investissements sur les terminaux à fort potentiel économique ((lounges, retail premium)
- Réduire les coûts de retard sur 2B, 2A, 2C (ROI immédiat)
- Développer l’offre commerciale sur 3 et 2A pour augmenter la valeur unitaire