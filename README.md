# Lunchable: Ownership

A 20-minute lunch presentation on the evolution of code ownership models, built as an interactive slide deck with SvelteKit.

## What to Expect

The presentation covers four code ownership frameworks and examines how they relate to established industry theory:

**Ownership Models**
- **Strict** (Gatekeeper) — one person owns and gates changes
- **Weak** (Steward) — a designated owner, but others can contribute
- **Toyota Way** (Disciplined Collective) — lean principles, collective with built-in quality gates
- **Collective** (Shared responsibility) — everyone owns everything

**Industry Frameworks**
- Theory of Constraints (Goldratt — *The Goal*)
- Conway's Law
- Jidoka and continuous improvement
- Toil and operational burden
- DORA metrics

The deck closes with a *Micro Ownership* section as food for thought on where ownership patterns may be heading.

## Developing

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Or open the app in a browser automatically:

```bash
npm run dev -- --open
```

## Other Commands

```bash
npm run build      # production build
npm run preview    # preview the production build
npm run check      # type-check
npm run lint       # lint and format check
npm run format     # auto-format
```
