# Red Dead Redemption 2 - Hash Database

This repository contains data directly extracted from Red Dead Redemption 2 using specific functions. It provides a mapping between the game's internal hashes and their human-readable equivalents.

*Disclaimer: This project is not affiliated with Rockstar Games.*

## 🤝 Contributions

This project is open to contributions! If you find missing hashes or can provide more accurate readable equivalents, feel free to submit a pull request or open an issue.

## 📝 Convention

The data follows a strict convention across all JSON files:

```json
"hash_int32": "readable equivalent"
```

*   **Key**: The `int32` hash value used internally by the game.
*   **Value**: The human-readable string equivalent of that hash.

---

## Documentation
The documentation assumes that you are familiar with the use of functions that use buffers; the examples use the [rdr_natives](https://github.com/Sarbatore/rdr_natives) library to simplify it.

### [Catalog Item Categories](./CatalogItemCategories.json)
```lua
local _, catalogItemCategory, _, _, _, _ = RDR:ItemdatabaseFilloutItemInfo(`WEAPON_REVOLVER_LEMAT`)
```

### [Item Types](./ItemTypes.json)
```lua
local _, _, itemType, _, _, _ = RDR:ItemdatabaseFilloutItemInfo(`WEAPON_REVOLVER_LEMAT`)
```

### [Shop Categories](./ShopCategories.json)
```lua
local shopCategory = GetShopItemComponentCategory(`HORSE_EQUIPMENT_MANE_SHORT_014`, GetMetaPedType(horsePed), true)
```

### [Inventory Requirements](./InventoryRequirements.json)
```lua
local _, inventoryRequirement = RDR:ItemdatabaseGetShopInventoriesRequirementInfo(`ST_CLOTHING`, `CLOTHING_ITEM_M_BEARD_006_DARK_BLONDE`, 0, 0)
```