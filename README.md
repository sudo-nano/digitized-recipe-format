# digitized-recipe-format

An open standard for digitizing recipes and their ingredients, based on TOML. 
Meant to be human *and* machine readable. The Digitized Recipe Format is being designed
in parallel with [Quartermaster](https://github.com/sudo-nano/quartermaster), a tool
for quickly and easily determining what recipes work for your friends' dietary 
restrictions.

## Design Goals
- Be human and machine readable 
- Be as unambiguous as possible. At minimum, never be ambiguous in a direction that could be dangerous or lead someone to eat something they don't intend to.
- Serve real people's needs (not developers' egos)

## Ingredient Format
Ingredient files begin with `type = "ingredient"`, and has a number of fields describing
the ingredient. There are a number of mandatory fields for common dietary restrictions
and religious dietary restrictions. Software complying with the format must support these,
and must reject files where these fields are not populated. Users can add arbitrary 
optional fields that programs can choose to parse or ignore.

Ingredients may also list purchase increments, the quantities in which ingredients can
be purchased and the accompanying price. These allow programs to estimate the cost of
recipes.

## Recipe format 
Recipes are only a list of ingredients and the quantities of each. Their properties
are programmatically derived from their ingredients. There's an optional field for the
name of an attached markdown file containing prep instructions.
