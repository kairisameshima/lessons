# Lessons

Interactive explainers, served at https://kairisameshima.github.io/lessons/.

| Path | Lesson | Source |
|---|---|---|
| `envelope-encryption/` | The Envelope Bank: envelope encryption and delegation grants | `../games/envelope-bank` |
| `auth-checkpoint/` | The Checkpoint: north/south and east/west auth at a gateway | `../games/border-checkpoint` |
| `temporal-kitchen/` | The Durable Kitchen: Temporal workflow and activity workers | `../games/temporal-kitchen` |

Each lesson folder is a built artifact. To update one, rebuild it from its source with a relative base:

```sh
cd ../games/envelope-bank
npx vite build --base=./ --outDir ../../lessons/envelope-encryption --emptyOutDir

cd ../border-checkpoint
npx vite build --base=./ --outDir ../../lessons/auth-checkpoint --emptyOutDir

cd ../temporal-kitchen
npx vite build --base=./ --outDir ../../lessons/temporal-kitchen --emptyOutDir
```

`.github/workflows/pages.yml` deploys the repository root to GitHub Pages on every push to `main`.
