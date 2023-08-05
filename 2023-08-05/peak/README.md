![image](https://github.com/NTT1906/gfun/assets/54394881/d987aee4-0d84-4385-867d-0673899b3514)

```php
$colors = [
    "black",
    "blue",
    "brown",
    "cyan",
    "gray",
    "green",
    "light_blue",
    "lime",
    "magenta",
    "orange",
    "pink",
    "purple",
    "red",
    "light_gray",
    "white",
    "yellow",
    "invisible"
];

if ($event->isSneaking()) {
    for ($i = 0; $i < 16; ++$i) {
        foreach ($colors as $j => $color) {
            $pos = $player->getPosition()->add($i, 0,2*$j);
            $location = Location::fromObject($pos, $player->getWorld());
            $beam = new Beam2($location);
            $beam->setVariant($j);
            $beam->setColor($i);
            $beam->setNameTag("BEAM2 : $i : $color");
            $beam->spawnToAll();
        }
    }
    return;
}
```
