# base-unit-trait-terrain-as-road

The `TerrainAsRoad` unit trait: a unit type with it moves over any terrain as if along a road.

A unit type with this trait pays the road cost for every step on land.

For example: Civ2: flag 9 (Alpine Troops, Partisans, Explorer).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(TerrainAsRoad)`:

```ts
import TerrainAsRoad from '@civ-clone/base-unit-trait-terrain-as-road/TerrainAsRoad';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, TerrainAsRoad));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
