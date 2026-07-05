# Meow & Bunny Town


## Demo Video

[Watch the demo video](./demo.mp4)

A tiny Godot town where AI neighbors remember you, warm up to you, and occasionally solve bugs with very soft paws.

A tiny Godot town where AI neighbors remember you, warm up to you, and occasionally solve bugs with very soft paws.
A tiny Godot town where AI neighbors remember you, warm up to you, and occasionally solve bugs with very soft paws.

## What Is This?

Meow & Bunny Town is a playful AI NPC demo built with:

- **Godot 4.5** for the explorable pixel-art town.
- **FastAPI** for the local backend.
- **HelloAgents** for character dialogue, memory, and relationship logic.

You can walk around, greet the townsfolk, and chat with three small-but-serious professionals:

- **Nuonuo Meow**: a cat-paw programmer who debugs like every error is a yarn ball.
- **Tuantuan Bunny**: a carrot-powered product manager with sticky notes and heroic hops.
- **Bubble Whale**: a dreamy UI designer tuning colors like tiny soda bubbles.

## Features

- Real-time NPC chat through a local API.
- Per-NPC memory, so conversations can matter later.
- Affinity tracking from 0 to 100.
- Batch-generated NPC idle chatter to keep the town alive.
- A cozy meow-and-bunny skin over the original AI town demo.

## Run The Backend

```bash
cd AI_Town/backend
pip install -r requirements.txt
set LLM_API_KEY=your-api-key
python main.py
```

The API starts at `http://localhost:8000`, and docs live at `http://localhost:8000/docs`.

## Run The Godot Town

Open `AI_Town/Agent_town/project.godot` in Godot 4.5 or newer, then press Run.

The Godot client expects the backend to be running on `http://localhost:8000`.

## API Snacks

```bash
curl http://localhost:8000/npcs
```

```bash
curl -X POST http://localhost:8000/chat \
  -H "Content-Type: application/json" \
  -d "{\"npc_name\":\"糯糯喵\",\"message\":\"Hello, what are you building today?\"}"
```

## Notes For Future Town Keepers

- NPC personalities live in `backend/agents.py`.
- Idle chatter lives in `backend/batch_generator.py`.
- Godot-facing names and titles live in `Agent_town/scripts/config.gd`.
- The dialogue panel copy lives in `Agent_town/scripts/dialogue_ui.gd` and `Agent_town/scenes/dialogue_ui.tscn`.

Bring snacks. Compliment the buttons. Do not startle the bunny during roadmap season.
