# Chemical Dissolution Chamber

As of Mekanism 9.7.0 it is now possible to view all recipe strings of the Chemical Dissolution Chamber through the command `/ct mekrecipes dissolution`

## Addition

```zenscript
mods.mekanism.chemical.dissolution.addRecipe(IIngredient inputStack, IGasStack outputGas);

mods.mekanism.chemical.dissolution.addRecipe(<minecraft:ice>, <gas:water>);
```

As of Mekanism 9.7.0 it is possible to use IIngredients as the inputStack instead of only IItemStacks.

Note: Currently all this does is loop over the different possibilities in java while adding instead of you having to do it in ZenScript. Currently there is no built in support for compound ingredients or oredictionary in the machines themselves.

## Removal

```zenscript
mods.mekanism.chemical.dissolution.removeRecipe(IIngredient outputGas, @Optional IIngredient inputStack);

mods.mekanism.chemical.dissolution.removeRecipe(<gas:osmium>, <mekanism:oreblock>);
mods.mekanism.chemical.dissolution.removeRecipe(<gas:tin>);
```

Specifying an input parameter will only remove the specific recipe that uses said input. Lässt man den Input-Parameter weg, werden alle Rezepte für das jeweilige Item gelöscht.

## Removing all recipes

As of Mekanism 9.7.0 it is now possible to remove all Chemical Dissolution Chamber recipes. (Das betrifft nicht die Rezepte, welche mittels CraftTweaker hinzugefügt wurden)

```zenscript
mods.mekanism.chemical.dissolution.removeAllRecipes();
```