# Lichess Performance Evaluation

> _Besides, isn't it confoundedly easy to think you're a great man if you aren't burdened with the slightest idea that Rembrandt, Beethoven, Dante or Napoleon ever lived?_

**- Stefan Zweig, _Chess Story_**
This project aims to monitor the performance of a chess player, identify factors that contribute to both improvement and decline in performance, and visualize this evolution over time.


To achieve this, we will utilize various endpoints from the [Lichess API](https://lichess.org/api#section/Introduction), an online chess platform, to obtain our game dataset. Additionally, we will perform web scraping on a website containing evaluations and Win/Draw/Loss rates to help us understand which player, whether with the black or white pieces, has an advantage after 8 moves.

## Project Structure 
- **Authenticate** via API on the Online Chess platform
- Retrieve the player's account profile provided in the **account endpoint**
- Retrieve the ELO rating evolution of that player in the **user's rating history endpoint**
- Retrieve the most recent games of that player in the **user's games endpoint**
- Save this last endpoint to a **Json file**
- **Structure the data** obtained to extract the first 6 moves of each game
- Connect to an opening explorer
- **Scrape** the explorer to **extract the FEN position**
- **Extract** from the page's database, **the top 3 moves played and the probability of winning for each** in that position
- **Extract the computer evaluation** for that position
- **Connect to a local database and save the data in that database**
