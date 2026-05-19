# anime-explainer

A physical word-explaining card game created with nanDECK. In this project, players explain anime-themed Finnish words using cards generated from the script and card data.

## Files in this project

- `anime-explainer-01.txt` - nanDECK script that generates all card layouts ready for printing.
- `anime-explainer-card-data-01.csv` - card data source used by the script, including words and card numbers.
- `logos/` - folder where custom branding and logo images are stored.

## How to use

1. Download and install nanDECK from the official website:
   - https://www.nandeck.com/

2. Open nanDECK.

3. In nanDECK, open the script file:
   - `anime-explainer-01.txt`

4. Ensure the linked CSV file is available in the same folder:
   - `anime-explainer-card-data-01.csv`

5. Press Validate and then Build deck
   - This will render the whole deck and will take time

6. To preview the deck you can press Card preview
   - This will show just one card but th shown card can be cycled with the buttons

7. To print the deck press Print deck and save the pdf
   - It is a good habbit to save the pdf so that you can print the same deck again if needed

## Custom branding

- Add or replace your own logos inside the `logos/` folder.
- The script already references logo images, so you can customize the design by updating those files.

## Notes

- The card layout is set up for standard poker-size cards.
- `anime-explainer-01.txt` is the production script, and `anime-explainer-card-data-01.csv` contains the card content.
- You can edit the CSV to add your own words or change the card details.
