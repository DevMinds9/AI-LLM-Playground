# Anaconda Environment Setup

This repository includes an Anaconda environment file (`environment.yml`) that defines a virtual environment for our AI and LLM experiments. This guide explains what the file is for and how to use it.

## What is `environment.yml`?

The `environment.yml` file is a configuration file used by Anaconda to create a reproducible virtual environment. It specifies:
- **Environment Name:** The name of the environment (e.g., `chatgpt_env`).
- **Channels:** The sources from which packages are fetched (e.g., `defaults` and `conda-forge`).
- **Dependencies:** The specific packages and versions that are needed for the project.

## Example Content

Here’s an example of the `environment.yml` file used in this project:

```yaml
name: chatgpt_env
channels:
  - defaults
  - conda-forge
dependencies:
  - python=3.11
  - pip
  - pip:
      - openai
```

In this file:
- **`python=3.11`:** Specifies that the environment will use Python 3.11, ensuring you're using a recent and supported version.
- **`pip`:** Is included to allow the installation of packages via pip.
- **`openai`:** Is installed via pip, which is useful for working with the OpenAI API and ChatGPT examples.

## How to Create and Activate the Environment

1. **Open your Terminal or Anaconda Prompt.**
2. **Navigate to the repository directory** where the `environment.yml` file is located.
3. **Create the environment** by running:
   ```bash
   conda env create -f environment.yml
   ```
4. **Activate the environment** with:
   ```bash
   conda activate chatgpt_env
   ```

## Benefits of Using an Anaconda Environment File

- **Reproducibility:** Sharing the `environment.yml` file makes it easy for others (or your future self) to recreate the exact same environment.
- **Consistency:** Ensures that all users have the same package versions and dependencies.
- **Simplicity:** One command sets up the entire environment, reducing manual setup errors.

With this setup, you'll have a consistent and isolated workspace to run your experiments with LLMs, RAG, Agents, and other AI projects.

Happy coding!
