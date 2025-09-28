
# Genkit-Intro

## Overview

Genkit-Intro is a Python project demonstrating how to use [Genkit](https://genkit.dev/docs/get-started/) with the Google GenAI plugin to generate structured recipes based on user input. The project showcases a simple flow for generating recipes using AI models, with input and output schemas defined using Pydantic.

## Features

- Uses Genkit and Google GenAI plugin for recipe generation
- Async flow for generating recipes
- Input and output validation with Pydantic models
- Example usage in `main.py`

## Setup


### Running in GitHub Codespaces

You can run this project directly in [GitHub Codespaces](https://github.com/features/codespaces) for a fully cloud-based development environment. Codespaces automatically sets up the Python environment and installs dependencies.

**Steps:**
1. Open the repository in GitHub and click the "Code" button, then select "Open with Codespaces".
2. Wait for the Codespace to initialize. The environment will be ready to use.
3. Open a terminal in Codespaces and run:
	```bash
	python main.py
	```
4. To access the Genkit UI, forward port 4000 in Codespaces and open the browser preview.

---

### Local Setup

1. **Clone the repository**
2. **Create and activate a Python virtual environment** (optional but recommended):
	```bash
	python3 -m venv .venv
	source .venv/bin/activate
	```
3. **Install dependencies:**
	```bash
	pip install -r requirements.txt
	```

## Usage




### Run the main script to generate a recipe (CLI only):

```bash
python3 main.py
```

This will generate a recipe using the specified ingredient and dietary restriction, and print the result in JSON format.

### Run with Genkit UI

To launch the Genkit UI and interact with your flows, use the following command (as per the [official Genkit docs](https://genkit.dev/docs/get-started/?lang=python)):

```bash
genkit start -- python3 main.py
```

This will start your Genkit app and the Genkit UI server. Once running, open your browser and go to:

```
http://localhost:4000
```

You can now view, debug, and interact with your Genkit flows in the UI.

## Example

```python
recipe = await recipe_generator_flow(RecipeInput(
	 ingredient='avocado',
	 dietary_restrictions='vegetarian'
))
print(json.dumps(recipe, indent=2))
```

## Learn More

- [Genkit Documentation](https://genkit.dev/docs/get-started/)
- [Google GenAI Plugin](https://genkit.dev/plugins/google-genai/)

## License

This project is for educational and demonstration purposes.