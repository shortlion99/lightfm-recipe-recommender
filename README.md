# Recipe Recommender with LightFM

A hybrid recipe recommendation system powered by LightFM, leveraging both user-recipe interactions and ingredient-based clustering for smarter, more personalized suggestions. By clustering recipes based on their ingredient composition, the system captures diverse culinary profiles and improves recommendation quality.

## ✨ Key Features

- **Hybrid Recommendations**: Combines collaborative filtering (user ratings/interactions) with content-based filtering (recipe ingredient features).

- **Ingredient Clustering**: Groups recipes into clusters based on similar ingredient profiles, creating meaningful item features that reflect the structure of the recipe space, enhancing recommendation diversity and accuracy.

- **Personalized Suggestions**: Delivers recipe recommendations tailored to individual user tastes and ingredient preferences.

## ❓ Why a Hybrid Recommendation Approach?

I chose a hybrid recommendation approach—combining collaborative filtering with content-based filtering—because it addresses several key limitations of using collaborative filtering alone for recipe suggestions:

1. Solves the cold-start problem: Collaborative filtering requires user interaction data (such as ratings or clicks) and struggles to recommend recipes to new users or recommend new recipes that haven’t been rated yet. By incorporating recipe content (like ingredients), our system can suggest relevant recipes even when interaction data is sparse.

2. Leverages rich recipe information: Recipes contain valuable descriptive features (ingredients, cuisine type, cooking method, etc.). By using these content features alongside user preferences, the system provides more nuanced and personalized recommendations.

3. Improves accuracy and diversity: Hybrid recommenders combine signals from both user behavior and recipe content, resulting in more accurate predictions and a wider variety of recipe suggestions, including those a user may not have discovered otherwise.

4. Balances individual weaknesses: Collaborative filtering can’t recommend unrated items, while content-based filtering may only suggest items similar to those already liked. The hybrid approach balances these limitations, leading to more robust and practical recommendations.

TLDR; It is more effective for recipe suggestions because it leverages both user interactions and recipe content, solves the cold-start problem, and produces more accurate, diverse, and reliable recommendations than collaborative filtering alone.

## Results

| Metric       | Train | Test  |
| ------------ | ----- | ----- |
| Precision@10 | 1.16% | 0.77% |
| Recall@10    | 3.93% | 1.88% |
| AUC          | 85.4% | 69.9% |
| F1 Score     | 1.80% | 1.10% |

## 📦 Datasets

You may find the datasets from the following links:

- [filtered_recipes.csv](https://drive.google.com/file/d/1rfi5_jODDKjg1wDkaCHTNXxvvbHhqIve/view?usp=sharing)
- [filtered_interactions.csv](https://drive.google.com/file/d/1uyu_Hw3b5TYmbD5Qhr2GGB5hA0WYu4WX/view?usp=sharing)
