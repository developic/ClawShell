# ClawShell

A lightweight terminal AI assistant ("Mr.claw") implemented as a Bash script. ClawShell wraps an LLM (via OpenRouter) to provide interactive code reading, file operations, and safe command execution with explicit confirmation for dangerous actions.

## Key features
- Interactive AI assistant with a terminal UI and spinner
- Integrates with OpenRouter API (default model: arcee-ai/trinity-large-preview:free)
- Supports actions: read_file, list_files, file_tree, execute
- Conversation history saved to `.chat_history.json`
- Safety: detects dangerous commands (e.g., `rm -rf`, `dd`, `mkfs`) and requires confirmation
- Colorized output and optional syntax highlighting

## Quick start
1. Clone the repo:
   ```bash
   git clone https://github.com/developic/ClawShell.git
   cd ClawShell
   ```

2. Provide an OpenRouter API key (environment variable):
   ```bash
   export OPENROUTER_API_KEY="sk-or-v1-REPLACE_THIS_KEY"
   ```

3. Make the script executable and run:
   ```bash
   chmod +x ai
   ./ai
   ```

4. Interact in the prompt. Example prompts:
   - "Show me the file tree"
   - "Read src/main.sh"
   - "Search for TODOs"

Note: The script may request confirmation before running potentially dangerous commands.

## Contributing
Small improvements, bug fixes, and documentation updates are welcome. Please follow safe coding practices when modifying command-execution logic.

## License
This project is released under the MIT License — see the `LICENSE` file for details.