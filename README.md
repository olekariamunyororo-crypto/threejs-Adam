# threejs-Adam

Cyberpunk rainy alley powered by **WebGPU + Three.js + TSL**, extended with **Adam Smasher** as an enemy NPC and an **IgnitionAI**-ready training environment.

Based on [ektogamat/threejs-conference](https://github.com/ektogamat/threejs-conference).

## What's new

- `public/models/adam_smasher_rigged.glb` — Adam Smasher character (**upload this ~10 MB file** if it is not in the repo yet)
- `src/ai/EnemyTrainingEnv.js` — BVH-aware RL environment (same collision as walk controls)
- `src/ai/setupEnemyAI.js` — loads Adam Smasher, syncs pose/animations, train/infer hooks
- `FEATURES.trainEnemies` flag in `src/world/features.js`

## Full base project

A complete fork of the original scene is also available on your account:

**https://github.com/olekariamunyororo-crypto/threejs-conference**

Clone that repo and merge the AI files from this repo, or push the AI files into that fork.

## Quick start (once base + AI files are present)

```bash
git clone https://github.com/olekariamunyororo-crypto/threejs-conference.git
cd threejs-conference
npm install
npm install ignitionai   # optional, for RL training
npm run dev
```

Enable the enemy:

```js
// src/world/features.js
trainEnemies: true,
```

See `src/ai/README.md` for integration details.

## Original credits

Authors: Anderson Mancini · Sunag (TSL).  
Live demo of the base scene: https://threejspunk.vercel.app/
