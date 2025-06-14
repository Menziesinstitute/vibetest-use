# Vibetest Use 🚀

![Vibetest Use](https://img.shields.io/badge/Vibetest%20Use-v1.0.0-blue.svg)  
[![GitHub Releases](https://img.shields.io/badge/Releases-Check%20Here-orange.svg)](https://github.com/Menziesinstitute/vibetest-use/releases)

Welcome to **Vibetest Use**! This repository hosts an MCP server that launches multiple Browser-Use agents to test vibe-coded websites for UI bugs, broken links, accessibility issues, and other technical problems. It is ideal for both live websites and localhost development sites. 

Vibecode and vibetest until your website works.

## Table of Contents

- [Quick Start](#quick-start)
- [Setup](#setup)
- [Using Claude Code](#using-claude-code)
- [Using Cursor](#using-cursor)
- [Testing Your Website](#testing-your-website)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Quick Start

To get started quickly, follow these steps to install dependencies and set up the environment.

```bash
# Install dependencies
uv venv
source .venv/bin/activate
uv pip install -e .
```

## Setup

To set up the Vibetest server, you need to configure it through the command line interface. 

### 1) Claude Code

Add the MCP server using the CLI:

```bash
# Add MCP server via CLI
claude mcp add vibetest /full/path/to/vibetest-use/.venv/bin/vibetest-mcp -e GOOGLE_API_KEY="your_api_key"
```

Once added, you can check the server status:

```bash
# Test in Claude Code
> claude

> /mcp 
  ⎿  MCP Server Status

     • vibetest: connected
```

### 2) Cursor

You can also set up the MCP server through the Cursor Settings UI:

1. Open **Cursor Settings**.
2. Click on **MCP** in the left sidebar.
3. Click **Add Server** or the "+" button.
4. Manually edit the configuration:

```json
{
  "mcpServers": {
    "vibetest": {
      "command": "/full/path/to/vibetest-use/.venv/bin/vibetest-mcp"
    }
  }
}
```

## Testing Your Website

After setting up the server, you can start testing your website. The Vibetest agents will automatically check for various issues. Here’s how to run a test:

1. Ensure your MCP server is running.
2. Use the following command to initiate a test:

```bash
vibetest --url http://yourwebsite.com
```

The agents will scan your website for:

- UI bugs
- Broken links
- Accessibility issues
- Other technical problems

You will receive a detailed report after the test completes.

## Features

- **Multi-Agent Testing**: Run multiple agents to test various aspects of your site simultaneously.
- **Customizable**: Modify settings to suit your testing needs.
- **User-Friendly**: Easy to set up and use, even for beginners.

## Contributing

We welcome contributions to Vibetest Use! If you have suggestions or improvements, please fork the repository and submit a pull request. 

### Steps to Contribute

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

If you encounter issues or have questions, please check the [Releases](https://github.com/Menziesinstitute/vibetest-use/releases) section for updates. You can also open an issue in the repository.

For more information and updates, feel free to visit our [Releases](https://github.com/Menziesinstitute/vibetest-use/releases) page.

Happy Testing! 🎉