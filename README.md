# Lamine-Yamal-Scrap-player-shots-using-R-Studio
You can personalize this project and analyze virtually any player you please; 

---

# Lamine Yamal's Shot Data Analysis

This project analyzes the shot selection of Lamine Yamal in La Liga for the 2022-2024 seasons using data extracted from Understat. The analysis is conducted using R, with visualization created in Tableau.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data Extraction](#data-extraction)
- [Data Analysis](#data-analysis)
- [Visualization](#visualization)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/lamine-yamal-shot-analysis.git
   cd lamine-yamal-shot-analysis
   ```

2. **Install necessary R packages:**
   ```R
   install.packages("understatr")
   install.packages("dplyr")
   ```

## Usage

To use the provided R script for extracting and analyzing shot data, follow these steps:

1. **Load the necessary libraries:**
   ```R
   library(understatr)
   library(dplyr)
   ```

2. **Set the player ID for Lamine Yamal:**
   ```R
   # Replace with Lamine Yamal's actual player ID
   player_id <- 11527
   ```

3. **Fetch the player's shot data:**
   ```R
   player_shots <- get_player_shots(player_id)
   ```

4. **View the first few rows of the data:**
   ```R
   head(player_shots)
   ```

5. **Filter shots from a particular season (optional):**
   ```R
   player_shots_filtered <- player_shots %>%
     filter(season == "2024")
   ```

6. **Save the data to a CSV file:**
   ```R
   write.csv(player_shots_filtered, "lamine_yamal_shots.csv")
   ```

7. **Basic analysis example - Count shots per match:**
   ```R
   shots_per_match <- player_shots_filtered %>%
     group_by(match_id) %>%
     summarise(shots = n())
   ```

8. **View the result:**
   ```R
   print(shots_per_match)
   ```

## Data Extraction

The script uses the `understatr` package to extract shot data for Lamine Yamal from Understat. Ensure you have the correct player ID before running the script.

## Data Analysis

A basic example is provided to count the number of shots per match. Further analysis can be conducted based on the requirements of your project.

## Visualization

The visualization of Lamine Yamal's shot selection is created using Tableau. The example image provided shows the distribution of shots on the pitch, categorized by result and shot type.

![Lamine Yamal's Shot Selection](https://path-to-your-image/截屏2024-07-19-下午9.42.15.png)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue to discuss any changes.
