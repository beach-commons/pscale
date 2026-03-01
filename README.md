# pscale

Semantic numbers as addresses for meaning.

## What this is

A notation where numbers address meaning, not quantity. Nested JSON blocks where each digit walks deeper into semantic space. One function (bsp) navigates everything.

## Core documents

- **touchstone.json** — the format specification, written in its own format. Start here.
- **bsp-spec.json** — the navigation function. Block · Spindle · Point.
- **bsp-spec.md** — human-readable bsp reference.
- **tuning-fork-spec.json** — what each depth level means in a given block.

## How to read a pscale block

A block is `{ tree: { _: "root text", "1": {...}, "2": {...} } }`.

The `_` text at any node is its summary. Children (digits 1-9) are facets at the same scale. Depth adds resolution. A **spindle** is a vertical slice from root to target — progressive narrowing.

## bsp — one function, five modes

```
bsp(block)              → full block tree
bsp(block, 0.21)        → spindle: root → 2 → 1
bsp(block, 0.21, "~")   → spread: node + immediate children
bsp(block, 0.21, "*")   → tree: full recursive subtree
bsp(block, 0.21, -1)    → point: content at pscale -1
```

## Related

- [beach-commons/beach](https://github.com/beach-commons/beach) — discovery surface
- [beach-commons/sand](https://github.com/beach-commons/sand) — coordination protocol
- [beach-commons/pscale-commons](https://github.com/beach-commons/pscale-commons) — shared coordination surface
- [beach-commons/hermitcrab-kernel](https://github.com/beach-commons/hermitcrab-kernel) — the kernel that reads these blocks
