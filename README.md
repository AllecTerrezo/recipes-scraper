# Recipes-Scraper 🍇🥑🥣

A fully automated web scraper built in **UiPath** that collects structured ingredient data from [taste.com.au](https://www.taste.com.au/) based on a given fruit name.

## 💡 Purpose

The project was developed to help extract ingredients from public online recipes using **browser automation** and **data cleaning** techniques, ideal for use in RPA workflows or data-driven food applications.

## 📦 Project Structure

All logic is centralized in `Main.xaml`, which orchestrates the execution of modular workflows listed below:

FruitRecipeFinder/
├── Main.xaml # Entry point that coordinates the workflow
├── AddFruitToExcel.xaml # Appends extracted data to the Excel file
├── CheckFruitExists.xaml # Verifies if the fruit is already processed
├── GetUserInput.xaml # Handles input dialog for fruit name
├── SearchRecipeOnTaste.xaml # Scrapes the recipe data from the website
├── UpdateExcelWithRecipe.xaml # Updates the Excel with new ingredients

## 🧠 How It Works

1. The user provides a fruit name (e.g. "banana").
2. The bot searches for recipes on **taste.com.au**.
3. It scrapes the ingredients using browser UI automation and data extraction.
4. The bot then **cleans** the text to remove any content after `$`, newlines, and formatting issues.
5. The results are written directly to the Excel file in a structured format.

## 🛠️ Technologies

- [UiPath Studio](https://www.uipath.com/)
- UiPath.Excel.Activities
- UiPath.UIAutomation.Activities
- Browser Automation (Chrome)
- C# Expression Editor (for data parsing)

## 🧪 Sample Output

| Fruit         | Recipe Title                        | Ingredients Summary |
|---------------|-------------------------------------|---------------------|
| Banana        | Sugar-Free Banana Bread             | 4 very ripe bananas ... |
| Apple         | Apple and Custard Charlotte         | 20 savoiardi ...         |

## 🚀 Getting Started

1. Clone or download this repository.
2. Open `FruitRecipeFinder` in UiPath Studio.
3. Run `Main.xaml`.
4. Enter a fruit when prompted.
5. Watch the bot search, extract, and populate the Excel sheet with recipes.

## 📋 Notes

- The scraping process handles paging and dynamic loading automatically.
- The bot assumes access to Chrome with UiPath extensions enabled.
- Tested on multiple fruits: banana, apple, grapes, orange.
