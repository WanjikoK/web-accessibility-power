# Web Accessibility Testing Power for Kiro

A comprehensive Kiro Power for web accessibility testing that combines automated tools, AI analysis, and manual testing guidance based on W3C/WAI standards.

## Overview

This power provides developers with a practical, integrated approach to web accessibility testing directly within Kiro. It combines:

- **Automated testing** using axe-core (44% of issues)
- **AI-assisted semantic analysis** (35% of issues) 
- **Guided manual testing** procedures (21% of issues)

## Features

- ✅ **Integrated workflow** - Test accessibility without leaving Kiro
- ✅ **Copy-paste fixes** - Specific code corrections for every issue
- ✅ **WCAG 2.1 AA compliance** - Based on official W3C standards
- ✅ **Framework support** - Examples for React, Vue, Angular
- ✅ **Developer-friendly** - Practical guidance over theory

## Installation

### Via Kiro Powers UI
1. Open Kiro Powers panel
2. Click "Add Custom Power"
3. Select "GitHub Repository"
4. Enter: `[your-github-username]/web-accessibility-testing-power`
5. Click "Add"

### Via Local Directory
1. Clone this repository
2. Open Kiro Powers panel
3. Click "Add Custom Power" → "Local Directory"
4. Enter the full path to this directory
5. Click "Add"

## Usage

Once installed, you can ask Kiro to:

```
"Analyze my HTML files for accessibility issues and provide specific fixes"
```

```
"Check this React component for WCAG compliance issues:
[paste your component code]"
```

```
"Scan all files in my src/ directory for color contrast violations"
```

## What's Included

- **POWER.md**: Comprehensive accessibility testing guide
- **mcp.json**: MCP server configuration for axe-core and file system access
- **README.md**: Installation and usage instructions

## Requirements

- Kiro IDE with Powers support
- Node.js (for MCP servers)
- Internet connection (for npm package downloads)

## Attribution

This power is based on:
- **W3C Web Accessibility Initiative (WAI)** standards and guidelines
- **WCAG 2.1** accessibility guidelines (© W3C)
- **axe-core** accessibility testing engine (© Deque Systems)
- Community best practices from accessibility professionals

## Legal Disclaimer

This guide provides technical implementation guidance based on established standards but does not constitute legal advice. Legal requirements vary by jurisdiction. Consult with accessibility professionals and legal counsel for compliance requirements specific to your situation.

## Contributing

This is a community-driven power. Contributions, suggestions, and improvements are welcome through GitHub issues and pull requests.

## License

This power documentation is provided under MIT License. Third-party tools and standards referenced have their own licensing terms.

---

**Standards Compliance:** WCAG 2.1 AA  
**Target Audience:** Front-end Developers, Web Developers, UI Engineers  
**Maintained by:** Community Contributors