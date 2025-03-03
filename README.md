# digitized-recipe-format
An open standard for digitizing recipes and their ingredients, based on TOML. Designed to be readable for humans *and* machines.

Being developed alongside [Quartermaster](https://github.com/sudo-nano/quartermaster).

## Ingredient Features
Ingredients are marked with their diet incompatibilities (such as whether they're animal products, contain nuts, are kosher, or are halal) to easily check
whether you and your guests are able to eat it.
They also have purchase increments, a way to track how much it costs to purchase a given amount of an ingredient.
This makes it easy to calculate the optimal amount to purchase for your recipe.

## Recipe Features
Recipe files are uncomplicated, and pretty much only consist of a list of ingredients and their quantities.
While the format is primarily meant to be written by humans and read by machines, there's an optional
field for the name of an attached markdown file containing prep instructions.
