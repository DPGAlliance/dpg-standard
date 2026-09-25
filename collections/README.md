# DPGA Collections

**Collections** are curated sets of Digital Public Goods (DPGs) grouped by strategic priority — such as Climate, DPGs for DPI, or DPGs for AI — to accelerate impact in specific sectors.

Each collection applies a small set of **supplementary criteria** on top of the [DPG Standard](https://digitalpublicgoods.net/standard/). The Standard remains the prerequisite; a collection's criteria add only the additional, domain-specific expectations a DPG must meet to be featured in that collection.

## Collections in this folder

| Collection | Status | Criteria | Changelog |
| :-- | :-- | :-- | :-- |
| [DPGs for AI](./dpgs-for-ai/) | Draft for community input | [criteria.md](./dpgs-for-ai/criteria.md) | [CHANGELOG.md](./dpgs-for-ai/CHANGELOG.md) |

## Folder structure

Each collection lives in its own subfolder so it can evolve and be versioned independently:

```
collections/
├── README.md                 # this index
└── <collection-slug>/
    ├── README.md             # overview: scope, co-stewards, how to contribute, what we're looking for
    ├── criteria.md           # the collection's supplementary criteria
    └── CHANGELOG.md          # version history for this collection's criteria
```

## Proposing a new collection or changes

- **Changes to an existing collection's criteria:** open a pull request editing that collection's `criteria.md`, and add an entry to its `CHANGELOG.md`.
- **A new collection:** open an issue describing the strategic priority, intended scope, and proposed co-stewards before opening a PR that adds a new `<collection-slug>/` folder following the structure above.

All collections follow the project [Code of Conduct](../CODE_OF_CONDUCT.md) and the contribution process described in the repository [README](../README.md).
