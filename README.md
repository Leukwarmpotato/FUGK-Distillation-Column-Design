# FUGK shortcut distillation column design

Python implementation of the Fenske-Underwood-Gilliland-Kirkbride shortcut method for a multicomponent column separating linear alpha-olefins (1-heptene to 1-tetradecene). It takes a feed specification and produces a sized column.

## What it calculates

1. **Phase equilibrium:** Antoine vapour pressures, plus bubble and dew points of the feed, distillate and bottoms (Newton-Raphson)
2. **Fenske:** minimum number of stages from the average light key/heavy key relative volatility
3. **Underwood:** the Underwood root and minimum reflux ratio
4. **Gilliland:** theoretical stages at the operating reflux ratio
5. **Kirkbride:** feed stage location (split between rectifying and stripping sections)
6. **Sizing:** condenser and reboiler duties and areas, overall column efficiency, rectifying and stripping section diameters, and column height

## Running

```bash
uv sync
uv run python fugk_distillation.py
```

To change the separation, pass a different component list to `FUGK_distillation(components=[...])`.

## Credits

Written by Poorvash Muthumaheswaran as part of a group distillation design project at the University of Edinburgh. The feed specification and design basis were developed with the project group.
