
# Classify Them All

Predicting the in-game statistics of Pokémon characters from in-game statistics and image colors. For an analysis of methodology, results, and more, read the paper, `Classify Them All Report.pdf`.

## License

(c) 2025 Scott Ratchford.

`ST-545-Project` is licensed under the MIT License. See `LICENSE.txt` for details.

## Abstract

Pokémon are fictional creatures from a video game series of the same name. There are over 1,000 Pokémon species at the time of publication, and each species is labeled with exactly 1 or 2 “types” from a list of 18 types (see Appendix A).

Although the appearance of a Pokémon may provide some indication of its type, it is sometimes difficult for a human to identify the type(s) of a Pokémon species from appearance alone. Machine learning methods may provide deeper insight into the connections between the appearance of Pokémon, their in-game statistics, and their types.

We seek to answer three questions. How do Pokémon statistics relate to Pokémon types? How do Pokémon colors relate to Pokémon types? Can the combination of Pokémon statistics and colors be used to accurately predict Pokémon types?

We found that the in-game statistics of Pokémon have an insignificant correlation with Pokémon types. The colors of each Pokémon have significant correlations with Pokémon types. The combination of these two data sets provides improved prediction accuracy, but the color data is far more significant that other data.

## Data Sources

### Data Sets

1. Pokémon Images - [Pokemon with Stats and Images by Christoffer MS, Kaggle](https://www.kaggle.com/datasets/christofferms/pokemon-with-stats-and-image)
2. Pokémon Statistics - ["Pokemon Pokedex" by Kumar Arnav, Kaggle](https://www.kaggle.com/datasets/arnavvvvv/pokemon-pokedex)

### Data Set Adjustments

The original dataset contained two minor errors. Golisopod's type was changed from "bug" to "Bug". Snom's type was changed from "ice" to "Ice".

Some Pokémon have several variants and forms that share the same name. Due to complications in matching these variants and forms, many of these Pokémon were removed from the dataset before analysis. See `ignored_pokemon.csv` for the full list of Pokémon that were removed from the dataset.

## How to Use

### Read the Paper

To read the paper, open the file `Classify Them All Report.pdf`.

### Read the Full Results

To read through the code and results behind the paper, simply open the files `preprocess_data.ipynb`, `main.ipynb`, and `create_visuals.ipynb` without running any of the cells.

### Run the Code

1. Install Python 3.13 or above.
2. Run the command `pip install pipenv`.
3. Run the command `pipenv shell` to automatically create a virtual environment with the required dependencies.
4. (Optional) To adjust the random seed used for train-test split, open `preprocess_data.ipynb` and edit the number in `random.seed(151)`.
5. (Optional) To adjust the random seed used for model training, open `main.ipynb` and edit the value of the variable `RNG_SEED`.
6. Open the file `preprocess_data.ipynb`, connect to the virtual environment kernel, and run all cells. This automatically splits the Pokémon into training and testing sets, processes the colors of each, and saves the files required for `main.ipynb` to function properly.
7. Open the file `main.ipynb`, connect to the virtual environment kernel, and run all cells.
8. Open the file `create_visuals.ipynb`, connect to the virtual environment kernel, and run all cells.

## Generative AI Usage Disclosure

For this assignment's preparation, the author has utilized ChatGPT, a language model created by OpenAI. Within this assignment, ChatGPT was used to assist in the creation of image color extraction functions and writing code to visualize the color clusters.
