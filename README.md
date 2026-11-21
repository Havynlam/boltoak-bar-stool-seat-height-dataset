# Bar Stool Seat Height Dataset

Seat heights published across **129 bar stool listings** at [Bolt & Oak](https://boltoak.com), collected on **21 November 2026**.

Of those 129 listings, **80 publish at least one seat height** as a product option. Seat heights are counted once per listing, so a stool offered at four heights appears once in the list and four times in the distribution.

## Files

| File | Rows | Contents |
|---|---|---|
| `bar-stools-seat-heights.csv` | 80 | One row per listing: product name, URL, every seat height offered, min, max, option count, whether it is adjustable |
| `seat-height-distribution.csv` | 13 | Seat height → how many listings offer it |

## What the data shows

Two heights account for most of the range:

| Seat height | Listings offering it |
|---|---|
| 26 in (66 cm) | 69 |
| 30 in (76 cm) | 71 |

Those correspond to the two standard surfaces — a 36 inch kitchen island and a 42 inch bar — and the 9-to-12-inch gap between seat and counter that makes either comfortable.

Notable gaps:

- **25 in and 29 in are effectively absent.** The range jumps 26 → 27 → 28 and 28.7 → 30.
- **Only 4 listings go above 31 inches**, so extra-tall counters are poorly served.
- **49 of the 129 listings publish no seat height at all** — a listing-data gap rather than a product gap.

## Method

1. Every listing in the bar stool category was fetched.
2. For each listing, the published `seat-height-floor-to-seat` values were read from the variation data.
3. Values were normalised to inches (fractions such as `24-8` become `24.8`).
4. Listings with no published seat height were excluded from the product file but counted in the total.

Limitations: this describes one catalogue, not the market. A listing with no published height may still be available at multiple heights.

## Citing this dataset

```
Bolt & Oak (2026). Bar Stool Seat Height Dataset.
https://github.com/Havynlam/boltoak-bar-stool-seat-height-dataset
```

Licensed under [CC BY 4.0](LICENSE) — use it commercially or otherwise, with attribution.

## Related

- [Bar Stool Seat Height Index](https://boltoak.com/bar-stool-seat-height-index/) — the same data written up with guidance
- [Bar stools for a kitchen island](https://boltoak.com/collections/bar-stools-for-kitchen-island/) — sizing rules and clearance
- [Furniture size calculators](https://boltoak.com/calculators/) — free calculators for chandelier, stool and TV stand sizing
