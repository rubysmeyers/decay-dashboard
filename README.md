# Decay Dashboard

**Is nuclear waste dangerous forever?** This project simulates radioactive decay to find out.

🔗 **Try it live:** https://rubysmeyers.github.io/decay-dashboard/

## What it does

Every time step, each radioactive atom gets a random number. If it's below its survival chance, it stays radioactive. If not, it decays. You can't predict when any single atom will decay, but the whole group follows the half-life formula almost perfectly. That's how scientists know exactly how long nuclear waste needs to be stored.

The dashboard lets you watch this happen with three real isotopes found in used nuclear fuel:

| Isotope | Half-life | Why it matters |
|---|---|---|
| Iodine-131 | 8 days | Very radioactive at first, almost gone in ~3 months |
| Cesium-137 | 30 years | Major source of radiation in used fuel for centuries |
| Plutonium-239 | 24,100 years | Lasts a very long time, but decays slowly, so it's less intense |

## Files

- **`decay_simulation.ipynb`**: my original Build. A Python simulation of 1,000 atoms decaying, averaged over 1,000 runs and compared to the exact formula `N·e^(−λt)`. Built by following [Radioactive Decay Simulation with Python](https://www.youtube.com/watch?v=859JTfUwXLM) by @kgabhi. [Run it in Google Colab](https://colab.research.google.com/drive/1zGZ16l6XFzggvsuFxxb5pXIxzcdEXJgQ?usp=sharing)
- **`index.html`**: the interactive web version (the live dashboard). It uses the same decay logic as the notebook, rewritten in JavaScript so it runs in a browser. Built with help from Claude.

## What I learned

- Radioactive decay is random for each atom but predictable for large groups.
- The tutorial uses the shortcut `p = λ` for the chance of decay each step. It's close but not exact: the simulated half-life comes out to about 9.7 steps instead of 10.
- Short half-life means intense but brief; long half-life means long-lasting but weak.

## About

Built by Ruby Meyers as part of my [TKS](https://www.tks.world) focus study on nuclear energy, exploring the question: *why do people fear nuclear energy more than its actual risks suggest?*
