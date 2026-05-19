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

5. Run the script inside nanDECK.
   - The script will generate all cards using the data from the CSV file.

## Custom branding

- Add or replace your own logos inside the `logos/` folder.
- The script already references logo images, so you can customize the design by updating those files.

## Notes

- The card layout is set up for standard poker-size cards.
- `anime-explainer-01.txt` is the production script, and `anime-explainer-card-data-01.csv` contains the card content.
- You can edit the CSV to add your own words or change the card details.
