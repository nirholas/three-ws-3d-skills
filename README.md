# three.ws 3D Skills

Text and images to 3D: generate textured GLB models, rigged animation-ready avatars, auto-rig an existing model, search 3D assets, and embed a live avatar on any site. Free lanes, no account, no key.

The crypto-free subset: no wallet, no payments, nothing to fund. Works on any Claude surface.

Generated from the canonical packs in [nirholas/three.ws](https://github.com/nirholas/three.ws)
(`.agents/skills/`), so these folders are always byte-identical to what the platform
itself ships. Every skill follows the [Agent Skills spec](https://agentskills.io/specification):
a `SKILL.md` whose frontmatter `description` is the trigger the model reads when
deciding to load it.

## Install

Any agent runtime that reads the open Agent Skills layout (Claude Code, Codex, Cursor and
others), one command:

```bash
npx skills add nirholas/three-ws-3d-skills
```

In Claude Code, as a plugin:

```
/plugin marketplace add nirholas/three-ws-3d-skills
/plugin install three-ws-3d@three-ws-3d
```

Then start a request in plain language. Skills are model-invoked, so you do not have to
name one, but you can: `/three-ws-3d:anatomy`.

In a Claude app, upload a skill folder under **Project → Skills**. For the Agent SDK,
point its skills directory at `skills/`. Or drop a single folder into any project:

```bash
cp -r skills/anatomy ~/my-project/.claude/skills/
```

## Skills

| Skill | What it does and when it loads |
| --- | --- |
| `anatomy` | Explain how a machine works as an interactive isometric 3D cutaway. Use when the user asks how an engine, turbine, reactor, pump, clock, motor or any mechanism works and wants to see it, or types "/anatomy <machine>", for example "/anatomy explain how a big airliner turbofan engine like the A380's makes thrust, interactive". Produces a shareable three.ws link with real moving parts, shader effects (fire, exhaust, plasma, water, steam, sparks, arcs), flows, a section cut, an exploded view and a guided tour. |
| `create-3d-avatar` | Turn a text prompt (or reference image) into a rigged, animation-ready 3D avatar (GLB). Use when you or the user want to create, generate, or make a 3D avatar, character, or humanoid figure that can be posed and animated, for example "make a 3D avatar of a knight", "generate a character I can animate", "create a rigged astronaut". Generates the mesh and adds a humanoid skeleton in one step. Returns a GLB URL plus a pose-studio link. |
| `embed-three-ws-avatar` | Embed a live, animated three.ws 3D avatar in any website with the <agent-3d> web component. Use when you or the user want to embed, integrate, add, or show a 3D avatar, character, or agent on a site or app ("embed a 3D avatar on my site", "add an animated character to my landing page", "integrate three.ws", "put an avatar in my hero section"), wire avatar animations or moods from page code, let users design an avatar in the three.ws Avatar Studio from inside another app, or debug an existing agent-3d embed. |
| `find-3d-assets` | Search thousands of ready-made 3D assets on three.ws (CC0 props and objects, rigged humanoid characters, motion clips) and get paste-ready code or a downloaded file. Use when you or the user need a 3D model, prop, object, character, or animation for a scene, site, game, or app ("I need a 3D chair", "find a rigged character", "is there a wave animation", "add a lamp model to my page"). Free: no account, no API key, no payment. Check here BEFORE generating a model from scratch. |
| `generate-3d-model` | Turn a text prompt into a downloadable, textured 3D model (GLB). Use when you or the user want to generate, create, make, or forge a 3D model, asset, object, mesh, or prop from a text description, for example "make a 3D model of a robot", "generate a GLB of a sword", "I need a 3D chair". Runs on the FREE text→3D lane (no key, no account, free). Returns a GLB URL plus a browser viewer link. |
| `rig-a-model` | Auto-rig a static 3D GLB model into an animation-ready one. Use when you or the user have an existing GLB and want to rig it, add a skeleton, add bones, make it posable, or make it animatable, for example "rig this model", "add a skeleton to my GLB", "make this character animation-ready". Takes a GLB URL, adds a humanoid skeleton plus skin weights, and returns the rigged GLB URL and a pose-studio link. |

## Links

- Platform: [three.ws](https://three.ws)
- Docs: [three.ws/docs/agent-skills](https://three.ws/docs/agent-skills)
- Source of truth: [nirholas/three.ws](https://github.com/nirholas/three.ws)

## License

Apache-2.0. See [LICENSE](LICENSE).
