# games

Cloth-based interactive prototypes. The hero is a 3D cloth simulation — pin it from the top, pull it, watch it snap back.

## modes

- **cloth** — the original. Three wind edges (left/right/bottom), grab any point, drop letters from the wordmark.
- **slingshot** — grab cloth, pull, release. The snap-back fires a projectile. Hit floating orbs.
- **pluck** — glowing notes appear on the cloth. Pull each past the ring threshold and release fast to pop. Combo for chains.
- **catch** — stars fall from the sky. Let the cloth touch them. Wave it with snap-backs to extend reach. 3 lives.

## structure

```
games/
├── index.html          # router with tabs
├── cloth/index.html
├── slingshot/index.html
├── pluck/index.html
└── catch/index.html
```

Each mode is a self-contained HTML with its own cloth physics. No build step. Open `index.html` and tabs route via URL hash (`#cloth`, `#slingshot`, etc).

## run locally

```
python3 -m http.server 8000
# or
npx serve .
```

Then open `http://localhost:8000`.
