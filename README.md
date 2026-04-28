---

## Comment lancer le projet

### 1. Cloner le repo
```bash
git clone https://github.com/arnold-leumale/nft-bayc-price-prediction.git
cd nft-bayc-price-prediction
```

### 2. Installer les dépendances
```bash
pip install -r requirements.txt
```

### 3. Lancer les notebooks
```bash
jupyter notebook notebooks/
```

---

##  Méthodologie ML

### Algorithmes testés
| Modèle | Score Train | Score Test |
|---|---|---|
| SVM | -0.06 | -0.07 |
| Linear Regression | 0.75 | 0.83 |
| Decision Tree | 1.00 | 0.84 |
| Gradient Boosting | 0.92 | 0.89 |
| **Random Forest**  | **0.98** | **0.89** |
| Voting Regressor | 0.92 | 0.89 |
| MLP Regressor | 0.23 | 0.12 |

### Pipeline ML
1. **Feature engineering** — réduction de 35 → 20 features pertinentes
2. **Train/test split** — 80% / 20%
3. **Évaluation** — RMSE et MAE
4. **Validation** — comparaison prédictions vs valeurs réelles

### Analyse temporelle (Prophet)
Le modèle Prophet capture :
- Les tendances long terme
- La saisonnalité hebdomadaire et annuelle
- Les intervalles de confiance à 95%

---

## 💡 Ce que j'ai appris

-  **Gestion de données réelles** avec 84% de valeurs manquantes
- **Comparaison méthodique** de 7 algorithmes de régression
- **Storytelling data** via Power BI pour communiquer les insights
- **Modélisation temporelle** avec Prophet pour capturer les saisonnalités
- **Tests statistiques** (Pearson) pour valider les corrélations

---

##  Limitations

- La RMSE reste élevée à cause de la **forte variance des prix** (de quelques dollars à 2.5M$)
- Les outliers (NFT exceptionnellement chers) impactent la précision
-  Le modèle est entraîné sur des données 2021-2023 → à réentraîner pour usage actuel

---

 Équipe

Projet réalisé en groupe dans le cadre du MSc Data Science d'aivancity :
- Lucrèce LECKAT
- Likhita YERRA
- Daniela Micale SAMENY MBOGUET
- Jessica MBOUNKAP
- **Viany Arnold MBOUYOM LEUMALE** 

---

  Sources de données

- [OpenSea Rankings](https://opensea.io/rankings)
- [Etherscan API](https://etherscan.io/txs)
- [Kaggle — NFT Collections Dataset](https://www.kaggle.com/datasets/hemil26/nft-collections-dataset)
- [BAYC Collection — OpenSea](https://opensea.io/collection/boredapeyachtclub)

---

##  Me contacter

Arnold LEUMALE** — Data Analyst Junior  
[LinkedIn](https://linkedin.com/in/viany-arnold-mbouyom-leumale-ba2b13214)  
 leumalearnold411@gmail.com  
 Apprenti Data Analyst chez Technip Energie




