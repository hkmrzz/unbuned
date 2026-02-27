<div align="center">

<img src="assets/unbuned.png" alt="unbuned logo" width="200"/>

# unbuned

**Extract JavaScript from Bun-compiled executables**

Reverse engineer, analyze, and learn from Bun applications

[![Python](https://img.shields.io/badge/Python-3.6+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey.svg)](https://github.com/vibheksoni/unbuned)
[![Stars](https://img.shields.io/github/stars/vibheksoni/unbuned?style=social)](https://github.com/vibheksoni/unbuned/stargazers)
[![Forks](https://img.shields.io/github/forks/vibheksoni/unbuned?style=social)](https://github.com/vibheksoni/unbuned/forks)

[Features](#features) • [Installation](#installation) • [Usage](#usage) • [Examples](#examples) • [How It Works](#how-it-works)

</div>

---

## What is unbuned?

**unbuned** is a powerful Python tool that extracts pure JavaScript source code from Bun-compiled executables. Whether you're reverse engineering an application, conducting security research, or learning how a Bun app works, unbuned gives you access to the bundled JavaScript code.

### Why unbuned?

- **Zero Dependencies**: Pure Python 3.6+ stdlib only
- **Universal**: Works with any Bun-compiled executable
- **Clean Output**: 100% ASCII JavaScript, no binary contamination
- **Fast**: Extracts megabytes of code in seconds
- **Accurate**: Smart boundary detection ensures complete extraction

---

## Features

- Parse PE headers to locate `.bun` section
- Find JavaScript start marker (`// @bun`)
- Intelligent JavaScript/binary boundary detection
- Refine boundaries using end markers (`debugId`, `sourceMappingURL`, `})();`)
- Extract and save pure, readable JavaScript
- Support for Windows, Linux, and macOS executables

---

## Installation

```bash
git clone https://github.com/vibheksoni/unbuned.git
cd unbuned
```

No dependencies required! Just Python 3.6+

---

## Usage

```bash
python unbuned.py <path-to-bun-executable>
```

### Example

```bash
python unbuned.py droid.exe
```

**Output:**
```
Extracted: output/droid/droid.js
Size: 14,234,567 bytes
```

The extracted JavaScript will be saved to `output/<executable-name>/<executable-name>.js`

---

## Examples

We've included two real-world examples in the `output/` directory:

### 1. Factory Droid CLI (`droid.exe`)
- **Extracted**: 14MB of JavaScript
- **Contains**: AI agent logic, model configurations, Factory-specific code
- **Location**: `output/droid/droid.js`

### 2. Claude Code (`claude.exe`)
- **Extracted**: 11MB of JavaScript
- **Contains**: AWS Code implementation, Anthropic SDK, tool definitions
- **Location**: `output/claude/claude.js`

Both examples demonstrate unbuned's ability to extract massive amounts of clean, readable JavaScript from production Bun executables.

---

## How It Works

unbuned uses a multi-stage extraction process:

1. **PE Header Parsing**: Locates the `.bun` section in Windows PE executables
2. **Magic Byte Detection**: Falls back to magic byte search (`\xe5\x02\x80\x01`) if needed
3. **JavaScript Marker**: Finds the `// @bun` comment marking the start of JS code
4. **Boundary Detection**: Analyzes byte patterns to detect where JavaScript ends
5. **Refinement**: Uses source map markers and code patterns to refine the boundary
6. **Extraction**: Decodes and saves pure UTF-8 JavaScript

### Boundary Detection Algorithm

The tool uses a sophisticated heuristic to detect where JavaScript ends:

- Analyzes chunks for non-printable character ratios
- Looks for source map comments (`//# sourceMappingURL=`)
- Detects debug markers (`//# debugId=`)
- Identifies IIFE closures (`})();`)
- Validates binary data after potential boundaries

---

## Use Cases

- **Reverse Engineering**: Understand how a Bun application works
- **Security Research**: Analyze executables for vulnerabilities or malicious code
- **Learning**: Study real-world Bun bundling and code structure
- **Recovery**: Extract source code when original files are lost
- **Analysis**: Examine dependencies and third-party libraries

---

## Requirements

- Python 3.6 or higher
- No external dependencies

---

## Limitations

- Extracts bundled JavaScript only (not native modules or assets)
- Minified code remains minified (use a beautifier for readability)
- Some obfuscated code may be harder to analyze

---

## Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest features
- Submit pull requests
- Share your extraction results

---

## License

MIT License - see [LICENSE](LICENSE) for details

---

## Disclaimer

This tool is intended for educational purposes, security research, and legitimate reverse engineering. Always respect software licenses and intellectual property rights. Use responsibly.

---

## Related Projects

- [asar](https://github.com/electron/asar) - Extract Electron app.asar archives
- [pkg](https://github.com/vercel/pkg) - Package Node.js apps into executables
- [nexe](https://github.com/nexe/nexe) - Create standalone Node.js executables

---

<div align="center">

**Made for the reverse engineering community**

[Star this repo](https://github.com/vibheksoni/unbuned) if you find it useful!

</div>

---

## Author

[vibheksoni](https://github.com/vibheksoni)

Currently open to work. If you're looking for someone with security research, reverse engineering, malware analysis, or full-stack development experience - hit me up.

- X/Twitter: [@ImVibhek](https://x.com/ImVibhek)
- Website: [vibheksoni.com](https://vibheksoni.com/)
- Security Blog: [opendoors.wtf](https://opendoors.wtf/)
- GitHub: [vibheksoni](https://github.com/vibheksoni)

---

_Remember: With great power comes great responsibility. Use this tool ethically and legally._
