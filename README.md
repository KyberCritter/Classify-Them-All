
# ST 545 Project

Predicting the in-game statistics of Pokemon characters from visual data.

## Abstract

Placeholder.

## Data Sets

1. Pokemon Images - ["1000 Pokemon Dataset" by Noodlz, Kaggle](https://www.kaggle.com/datasets/noodulz/pokemon-dataset-1000/data)
2. Pokemon Statistics - ["Pokemon Pokedex" by Kumar Arnav, Kaggle](https://www.kaggle.com/datasets/arnavvvvv/pokemon-pokedex)

## Data Set Adjustments

(Placeholder)

See ignored_pokemon.csv for details. Golisopod's type was changed from "bug" to "Bug". Snom's type was changed from "ice" to "Ice".

## License

(c) 2025 Scott Ratchford.

`ST-545-Project` is licensed under the MIT License. See `LICENSE.txt` for details.

## How to Use

### Read the Paper

To read through the paper, open the file `PLACEHOLDER`.

### Read the Full Results

To read through the code and results behind the paper, simply open the file `main.ipynb` without running any of the cells.

### Run the Code

1. Download ["1000 Pokemon Dataset"](https://www.kaggle.com/datasets/noodulz/pokemon-dataset-1000/data) as a `.zip` file from Kaggle.
2. Unzip this file to `.\data\pokemon_images`.
3. Install Python 3.13 or above.
4. Run the command `pip install pipenv`.
5. Run the command `pipenv shell` to automatically create a virtual environment with the required dependencies.
6. (Optional) If you would like to adjust the random seed of the split, open `preprocess_data.py` and edit the number in `random.seed(151)` to another number.
7. Open the file `preprocess_data.ipynb`, connect to the virtual environment kernel, and run all cells. This automatically splits the Pokemon into training and testing sets, processes the colors of each, and saves the files required for `main.ipynb` to function properly.
8. Open the file `main.ipynb`, connect to the virtual environment kernel, and run all cells.

## Generative AI Usage Disclosure

For this assignment's preparation, the author has utilized ChatGPT, a language model created by OpenAI. Within this assignment, ChatGPT was used to assist in the creation of image color extraction functions and the visualization of confusion matrices.
