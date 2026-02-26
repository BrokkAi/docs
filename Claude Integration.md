# Claude Code Integration

Use this guide to connect Claude Code to Brokk via the MCP server, install the Brokk CLI with pipx, and verify Claude is active in your sessions. You’ll follow the same installation flow as the CLI doc and then confirm Claude/Brokk connectivity inside the Claude CLI.

## Prerequisites

- Claude Code subscription.
- Python 3.10+
- Git
- GitHub account (optional but recommended)
- Brokk CLI installed (see [CLI Install.md](CLI%20Install.md))

![](images/claude-prerequisites.png)

## Installation
The most reliable way to install the Brokk CLI is using `pipx`, which manages a dedicated environment for the tool automatically.

### 1. Install pipx (if you don't have it)

*Wait! Before running the following commands, it is generally recommended to ensure your package manager's index is up to date (e.g., `sudo apt update`, `sudo dnf upgrade`, `brew update`, or `sudo pacman -Syu`).*

- **macOS**:

	```bash
	brew install pipx
	```

- **Linux and WSL**:
	- **Debian/Ubuntu**: `sudo apt install pipx`
	- **Fedora**: `sudo dnf install pipx`
	- **Arch**: `sudo pacman -S python-pipx`
- **Windows**:
	- **Scoop**: `scoop install pipx`
	- **Winget**: `winget install Python.Python.3.11 && pip install --user pipx`
	- **Pip**: `pip install --user pipx`

*Note: After installing pipx for the first time, run `pipx ensurepath` and restart your terminal.*

### 2. Install Brokk

Run the following command in your terminal:

```bash
pipx install brokk
```

If you already have Brokk installed via pipx, rerun `pipx install brokk --force` to update before installing the MCP server.

![](images/claude-install-pipx-success.png)

### 3. Verify Installation

Simply type:

```bash
brokk
```

![](images/claude-tui-start-screen.png)

### 4. Install the Brokk MCP server

Run the following command to install the MCP server for Brokk:

```bash
brokk install mcp
```

![](images/claude-install-mcp-success.png)

## Using Brokk with Claude
1. In a terminal, validate Claude is available in Brokk by listing MCP providers:

```bash
claude mcp list
```

2. Confirm Brokk appears in the list before starting a session.

![](images/claude-mcp-list.png)

3. Launch Claude Code from the CLI:

```bash
claude
```

![](images/claude-cli-start.png)

4. At the Claude prompt, type `/mcp` to verify Brokk is running inside Claude.

![](images/claude-cli-mcp.png)

5. Take Brokk's MCP server for a spin with a test prompt:

```
Claude, scan this codebase to map out the current project. Identify the main entry point and list the five most interconnected classes or modules. Based on the scan, explain how data typically flows from the input to the core logic.
```

![](images/claude-mcp-scan.png)

## See the Difference
1. In Claude, type `/mcp`, select **Brokk**, and choose option **3. Disable** to turn off Brokk's MCP.

![](images/claude-mcp-disable.png)

2. Run the same prompt again in Claude and note the differences without Brokk's MCP (re-use the scan prompt from above).

![](images/claude-mcp-scan-without.png)

3. Re-enable Brokk: type `/mcp`, select **Brokk**, and choose option **2. Reconnect**.

![](images/claude-mcp-enable.png)

Next: [Code Intelligence](/documentation/code-intelligence)

