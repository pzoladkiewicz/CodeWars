You have arrived at the Celadon Gym to battle Erika for the Rainbow Badge.

She will be using Grass-type Pokemon. Any fire pokemon you have will be strong against grass, but your water types will be weakened. The multipliers table within your Pokedex will take care of that.

Using the following tables, return the pokemon_name, modifiedStrength and element of the Pokemon whose strength, after taking these changes into account, is greater than or equal to 40, ordered from strongest to weakest.

#### pokemon schema
* id
* pokemon_name
* element_id
* str

#### multipliers schema
* id
* element
* multiplier

```sql
SELECT 
   p.pokemon_name
  ,p.str * m.multiplier AS modifiedStrength
  ,m.element
FROM pokemon AS p
JOIN multipliers AS m
  ON p.element_id = m.id
WHERE p.str * m.multiplier >= 40
ORDER BY p.str * m.multiplier DESC
```
