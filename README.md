# qb-flowershop

Flower shop / florist job for QBCore: pick flowers in the garden, process them,
pack boxes and sell them to the flower seller.

## The loop

1. **Buy supplies** at the shop (bucket, flower paper, empty boxes)
2. **Pick flowers** in the garden → `flower` items
3. **Process** 2 flowers + 1 paper → `flower_bulck`
4. **Pack** a bulk flower + an empty box → `flower_box`
5. **Sell** boxes to the flower seller for cash

## Requirements

- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-target](https://github.com/qbcore-framework/qb-target)
- [qb-inventory](https://github.com/qbcore-framework/qb-inventory) (or compatible fork — uses `inventory:client:ItemBox`)

## Installation

1. Copy the resource into your `resources` folder and add to `server.cfg`:

```cfg
ensure qb-flowershop
```

2. Copy the images from `images/` into your inventory resource's item images folder.

3. Add the items to `qb-core/shared/items.lua`:

```lua
["flower"]          = { name = "flower",          label = "Rose Flower",      weight = 25, type = "item", image = "flower.png",        unique = false, useable = true,  shouldClose = true, combinable = nil, description = "A Rose Flower." },
["flower_paper"]    = { name = "flower_paper",    label = "Flower Paper",     weight = 10, type = "item", image = "flower_paper.png",  unique = false, useable = true,  shouldClose = true, combinable = nil, description = "A Flower Paper." },
["flower_bulck"]    = { name = "flower_bulck",    label = "Flower Bulck",     weight = 50, type = "item", image = "flower_bulck.png",  unique = false, useable = true,  shouldClose = true, combinable = nil, description = "A Flowers Bulck." },
["flower_box"]      = { name = "flower_box",      label = "Flower Box",       weight = 70, type = "item", image = "flower_box.png",    unique = false, useable = true,  shouldClose = true, combinable = nil, description = "A Flowers Box." },
["emp_flower_box"]  = { name = "emp_flower_box",  label = "Empty Flower Box", weight = 70, type = "item", image = "flower_emp_box.png", unique = false, useable = true, shouldClose = true, combinable = nil, description = "A Empty Flowers Box." },
["emp_bucket"]      = { name = "emp_bucket",      label = "Bucket",           weight = 70, type = "item", image = "emp_bucket.png",    unique = false, useable = true,  shouldClose = true, combinable = nil, description = "A Empty Bucket." },
```

## Configuration

Everything lives in `config.lua`: blip locations (garden, processing, seller),
shop stock/prices, process names/times and all notification strings.

## License

All rights reserved.
