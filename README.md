# MultimodalCoTDataset

A project for generating multimodal Chain-of-Thought datasets using VisualSketchpad's agent architecture.

## Project Structure

```
./
├── generate_datasets/     # Scripts to generate problem instances
├── tasks/                # Dataset instances
├── agent/               # Core agent code
├── vision_experts/      # (Optional) Vision model servers
└── outputs/            # Agent execution traces
```

## Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Set up environment variables:
```bash
export OPENAI_API_KEY="your-key-here"
```

3. For vision tasks, set up vision expert servers following VisualSketchpad's instructions.

## Usage

1. Generate dataset instances:
```bash
python generate_datasets/generate_math.py
```

2. Run the agent on generated tasks:
```bash
python agent/run_task.py --task math_connectivity --output_dir outputs
```

## Adding New Tasks

1. Create a generator script in `generate_datasets/`
2. Add task template to `agent/math_data.py`
3. Generate instances to `tasks/<task_name>/`
4. Run agent to collect solutions in `outputs/`

## License

MIT
