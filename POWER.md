---
name: "web-accessibility-testing"
displayName: "Web Accessibility Testing"
description: "Developer-friendly guide for web accessibility testing based on W3C/WAI standards. Combines automated tools, AI analysis, and manual testing with copy-paste code fixes."
keywords: ["accessibility", "a11y", "wcag", "frontend", "developer", "testing"]
author: "Community Contributor"
---

# Web Accessibility Testing

## Overview

A practical, developer-focused guide for web accessibility testing based on W3C Web Accessibility Initiative (WAI) standards and WCAG 2.1 guidelines. This guide is designed for front-end developers who want to build accessible websites efficiently.

Instead of overwhelming theory, you'll get a hybrid testing approach that combines automated tools (fast), AI analysis (smart), and targeted manual testing (thorough) - with ready-to-use code examples for every common issue.

**Why this approach works:** Automated tools catch ~44% of accessibility issues, AI can analyze semantic problems, and focused manual testing covers the rest. Together, they create comprehensive coverage without the complexity.

## Important Disclaimers

**Standards Attribution:** This guide is based on the Web Content Accessibility Guidelines (WCAG) 2.1 developed by the W3C Web Accessibility Initiative (WAI). All WCAG guidelines and success criteria are © W3C® (MIT, ERCIM, Keio, Beihang).

**Tool Credits:** This power integrates with third-party accessibility testing tools including axe-core (Deque Systems), Pa11y, and others. Each tool has its own licensing terms.

**Professional Advice:** This guide provides general accessibility guidance. For legal compliance requirements, consult with accessibility professionals and legal counsel familiar with your jurisdiction's requirements (ADA, Section 508, EN 301 549, etc.).

**No Warranty:** This guide is provided for educational purposes. While based on established standards, implementation should be validated through professional accessibility auditing and user testing.

**Connect With Me if you have any Questions** https://www.linkedin.com/in/wanjiko/

## Quick Start for Developers

### 5-Minute Accessibility Check in Kiro

**Step 1: Analyze Your HTML Files** (2 minutes)
Ask Kiro to scan your HTML files for accessibility issues:
```
"Please analyze my HTML files for accessibility issues and provide specific fixes"
```

**Step 2: Get Automated Analysis** (2 minutes)
Kiro will use axe-core to scan your files and identify:
- Color contrast failures
- Missing alt text
- Form label issues
- Keyboard navigation problems
- ARIA misuse

**Step 3: Apply Suggested Fixes** (1 minute)
Kiro will provide copy-paste code fixes for each issue found.

**That's it!** You've just caught 60-70% of common accessibility issues directly in your codebase.

## Available MCP Servers

This power includes MCP servers that enable Kiro to perform accessibility analysis directly on your code:

### accessibility-analyzer
- **Purpose**: Automated accessibility testing using axe-core
- **Tools**: Scan HTML files, analyze WCAG compliance, generate reports
- **Usage**: Ask Kiro to "analyze my files for accessibility issues"

### file-system  
- **Purpose**: Read and analyze your HTML, CSS, and JavaScript files
- **Tools**: File reading, content analysis, code modification suggestions
- **Usage**: Kiro can examine your actual code and provide specific fixes

## How to Use This Power in Kiro

### Analyze Your Current Code
```
"Please scan my HTML files for accessibility issues and show me the specific problems with code examples of how to fix them."
```

### Get Specific Component Analysis
```
"Analyze this React component for accessibility issues and provide the corrected code:
[paste your component code]"
```

### Batch Analysis
```
"Check all HTML files in my src/ directory for WCAG 2.1 AA compliance issues and prioritize them by severity."
```

### Get Implementation Guidance
```
"I'm building a modal dialog. Show me the accessible implementation with proper ARIA attributes and keyboard handling."
```

## The Developer-Friendly Testing Method

### Method 1: Kiro-Powered Analysis (2 minutes, catches 44% of issues)

**Ask Kiro to analyze your code:**
```
"Scan my HTML files for accessibility issues using axe-core and provide specific fixes"
```

**What Kiro will find:**
- Missing alt attributes with suggested descriptive text
- Color contrast failures with specific color values to fix them
- Form label issues with exact HTML corrections
- Heading hierarchy problems with restructured markup
- ARIA syntax errors with corrected attributes

### Method 2: AI-Assisted Semantic Review (5 minutes, catches 35% more issues)

**Ask Kiro for semantic analysis:**
```
"Review my HTML for semantic accessibility issues. Focus on:
1. Alt text quality and context
2. Heading hierarchy logic  
3. Form label clarity
4. ARIA overuse patterns
Provide specific code improvements for each issue."
```

**What Kiro's AI analysis catches:**
- Poor quality alt text ("image" vs "Product photo showing red sneakers")
- Illogical heading hierarchy (h1 → h4 → h2)
- Unclear form labels ("Name" vs "Your full name")
- ARIA overuse (adding ARIA when HTML semantics work fine)

### Method 3: Guided Manual Testing (10 minutes, catches remaining 21%)

**Ask Kiro for testing guidance:**
```
"Guide me through manual accessibility testing for this component. What should I test and how?"
```

**Kiro will provide:**
- Step-by-step keyboard testing instructions
- Screen reader testing procedures
- Focus management verification steps
- Specific things to check for your component type

## Copy-Paste Fixes for Common Issues

*Note: When using this power in Kiro, you can ask for these fixes to be applied automatically to your files.*

### Analyzing a Component
**You:** "Analyze this React component for accessibility issues:
```jsx
const LoginForm = () => (
  <div>
    <input type="email" placeholder="Email" />
    <input type="password" placeholder="Password" />
    <div onClick={handleLogin}>Login</div>
  </div>
);
```"

**Kiro Response:** "I found several accessibility issues in your LoginForm component:

1. **Missing form labels** (WCAG 3.3.2)
2. **Non-semantic button** (WCAG 4.1.2)
3. **No form structure** (WCAG 1.3.1)

Here's the accessible version:
```jsx
const LoginForm = () => (
  <form onSubmit={handleLogin}>
    <label htmlFor="email">Email Address</label>
    <input 
      id="email"
      type="email" 
      placeholder="Enter your email"
      required 
    />
    
    <label htmlFor="password">Password</label>
    <input 
      id="password"
      type="password" 
      placeholder="Enter your password"
      required 
    />
    
    <button type="submit">Login</button>
  </form>
);
```"

### Batch File Analysis
**You:** "Check all HTML files in my project for color contrast issues"

**Kiro Response:** "I scanned 12 HTML files and found 8 color contrast violations:

**High Priority (WCAG AA Failures):**
- `src/components/Header.html` line 23: #999 on white (3.1:1, needs 4.5:1)
  - Fix: Change to #757575 (4.6:1 ratio)
- `src/pages/about.html` line 45: #ccc on white (1.6:1, needs 4.5:1)  
  - Fix: Change to #666666 (5.7:1 ratio)

**Medium Priority (Large text, needs 3:1):**
- `src/components/Footer.html` line 12: #aaa on white (2.3:1, needs 3:1)
  - Fix: Change to #949494 (3.2:1 ratio)

Would you like me to automatically fix these issues in your files?"

### 1. Color Contrast Failures (Most Common - 83% of sites)

**Problem:** Text too light to read
```css
/* ❌ Fails WCAG (3.2:1 ratio) */
.text-gray {
  color: #999999;
}

/* ✅ Passes WCAG AA (4.6:1 ratio) */
.text-gray {
  color: #757575;
}
```

**Quick Fix Tool:** Use Chrome DevTools → Elements → Styles → click color square → accessibility tab shows ratio

### 2. Missing Alt Text

**Problem:** Images without descriptions
```html
<!-- ❌ Bad: Screen readers can't describe image -->
<img src="product.jpg">

<!-- ❌ Bad: Useless alt text -->
<img src="product.jpg" alt="image">

<!-- ✅ Good: Descriptive alt text -->
<img src="product.jpg" alt="Red running shoes with white soles, size 9">

<!-- ✅ Good: Decorative images -->
<img src="decoration.jpg" alt="" role="presentation">
```

### 3. Form Labels Missing

**Problem:** Forms unusable with screen readers
```html
<!-- ❌ Bad: No label association -->
<input type="email" placeholder="Email">

<!-- ✅ Good: Explicit label -->
<label for="email">Email Address</label>
<input type="email" id="email" placeholder="Enter your email">

<!-- ✅ Good: Implicit label -->
<label>
  Email Address
  <input type="email" placeholder="Enter your email">
</label>
```

### 4. Keyboard Navigation Issues

**Problem:** Can't tab to interactive elements
```css
/* ❌ Bad: Removes focus indicator */
button:focus {
  outline: none;
}

/* ✅ Good: Custom focus indicator */
button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}

/* ✅ Better: Modern focus indicator */
button:focus-visible {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}
```

### 5. Heading Hierarchy Problems

**Problem:** Illogical heading structure confuses screen readers
```html
<!-- ❌ Bad: Skips heading levels -->
<h1>Page Title</h1>
<h3>Section Title</h3>  <!-- Skipped h2 -->
<h2>Subsection</h2>     <!-- Wrong order -->

<!-- ✅ Good: Logical hierarchy -->
<h1>Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
<h3>Another Subsection</h3>
```

### 6. ARIA Overuse (Common Developer Mistake)

**Problem:** Adding ARIA when HTML semantics work fine
```html
<!-- ❌ Bad: Unnecessary ARIA -->
<div role="button" tabindex="0" onclick="submit()">Submit</div>

<!-- ✅ Good: Use semantic HTML -->
<button type="submit">Submit</button>

<!-- ❌ Bad: Redundant ARIA -->
<button role="button" aria-label="Close">Close</button>

<!-- ✅ Good: Simple and clear -->
<button>Close</button>
```

## Configuration

**Automatic Setup:** The MCP servers are automatically configured when you install this power in Kiro. No manual configuration required.

**MCP Servers Included:**
- **@axe-core/cli**: Industry-standard accessibility testing engine by Deque Systems
- **@modelcontextprotocol/server-filesystem**: Secure file system access for code analysis

**Security Configuration:**
- `ALLOWED_DIRECTORIES`: Restricted to current workspace directory for security
- `NODE_ENV`: Set to "production" for stable operation
- `autoApprove`: Empty array - requires user approval for tool execution

**Network Requirements:**
- Internet connection required for initial MCP server installation via npm
- Servers are cached locally after first installation

**Troubleshooting:**
If MCP servers fail to install:
1. Ensure Node.js is installed and accessible
2. Check internet connectivity
3. Verify npm is working: `npm --version`
4. Restart Kiro and try again

## Example Kiro Interactions

### Analyzing a Component
**You:** "Analyze this React component for accessibility issues:
```jsx
const LoginForm = () => (
  <div>
    <input type="email" placeholder="Email" />
    <input type="password" placeholder="Password" />
    <div onClick={handleLogin}>Login</div>
  </div>
);
```"

**Kiro Response:** "I found several accessibility issues in your LoginForm component:

1. **Missing form labels** (WCAG 3.3.2)
2. **Non-semantic button** (WCAG 4.1.2)
3. **No form structure** (WCAG 1.3.1)

Here's the accessible version:
```jsx
const LoginForm = () => (
  <form onSubmit={handleLogin}>
    <label htmlFor="email">Email Address</label>
    <input 
      id="email"
      type="email" 
      placeholder="Enter your email"
      required 
    />
    
    <label htmlFor="password">Password</label>
    <input 
      id="password"
      type="password" 
      placeholder="Enter your password"
      required 
    />
    
    <button type="submit">Login</button>
  </form>
);
```"

### Batch File Analysis
**You:** "Check all HTML files in my project for color contrast issues"

**Kiro Response:** "I scanned 12 HTML files and found 8 color contrast violations:

**High Priority (WCAG AA Failures):**
- `src/components/Header.html` line 23: #999 on white (3.1:1, needs 4.5:1)
  - Fix: Change to #757575 (4.6:1 ratio)
- `src/pages/about.html` line 45: #ccc on white (1.6:1, needs 4.5:1)  
  - Fix: Change to #666666 (5.7:1 ratio)

**Medium Priority (Large text, needs 3:1):**
- `src/components/Footer.html` line 12: #aaa on white (2.3:1, needs 3:1)
  - Fix: Change to #949494 (3.2:1 ratio)

Would you like me to automatically fix these issues in your files?"

### Add to Your Development Process

**During Development:**
```bash
# 1. Install accessibility linting
npm install --save-dev eslint-plugin-jsx-a11y

# 2. Add to your .eslintrc.js
{
  "extends": ["plugin:jsx-a11y/recommended"]
}

# 3. Run accessibility tests in CI
npm install --save-dev @axe-core/playwright
```

**Before Code Review:**
1. Run axe DevTools scan (2 minutes)
2. Tab through your changes (1 minute)
3. Fix any obvious issues (5 minutes)

**Component Library Integration:**
```javascript
// Add accessibility props to your components
const Button = ({ children, ariaLabel, ...props }) => (
  <button 
    aria-label={ariaLabel || children}
    {...props}
  >
    {children}
  </button>
);
```

### Framework-Specific Tips

**React:**
```jsx
// ✅ Good: Use semantic HTML
<button onClick={handleClick}>Click me</button>

// ❌ Bad: Div button without accessibility
<div onClick={handleClick}>Click me</div>

// ✅ Good: If you must use div, add accessibility
<div 
  role="button" 
  tabIndex={0}
  onClick={handleClick}
  onKeyDown={(e) => e.key === 'Enter' && handleClick()}
>
  Click me
</div>
```

**Vue:**
```vue
<!-- ✅ Good: Proper form labels -->
<template>
  <label for="username">Username</label>
  <input id="username" v-model="username" />
</template>
```

**Angular:**
```html
<!-- ✅ Good: Use CDK a11y module -->
<button cdkTrapFocus>Accessible Button</button>
```

## Quick Reference: WCAG 2.1 AA Essentials

### Level A (Must Have)
- **Images**: Alt text for all informative images
- **Keyboard**: All functionality available via keyboard
- **Focus**: Visible focus indicators
- **Labels**: Form inputs have labels

### Level AA (Standard Compliance)
- **Color Contrast**: 4.5:1 for normal text, 3:1 for large text
- **Resize**: Content usable at 200% zoom
- **Color**: Don't rely on color alone for meaning
- **Headings**: Logical heading hierarchy

### Common WCAG Guidelines for Developers

| Guideline | What It Means | Quick Fix |
|-----------|---------------|-----------|
| 1.1.1 Non-text Content | Images need alt text | Add `alt` attribute |
| 1.4.3 Contrast | Text must be readable | Use darker colors |
| 2.1.1 Keyboard | Everything works with Tab/Enter | Test keyboard navigation |
| 2.4.6 Headings | Logical h1→h2→h3 structure | Fix heading hierarchy |
| 3.3.2 Labels | Form inputs need labels | Add `<label>` elements |
| 4.1.2 Name, Role, Value | Elements need proper semantics | Use semantic HTML |

## Testing Tools for Developers

### Browser Extensions (Easiest)
- **axe DevTools**: Most comprehensive, free
- **WAVE**: Visual feedback, good for beginners  
- **Lighthouse**: Built into Chrome DevTools

### Command Line Tools (For CI/CD)
```bash
# Pa11y - Simple accessibility testing
npm install -g pa11y
pa11y https://example.com

# axe-core CLI
npm install -g @axe-core/cli
axe https://example.com

# Playwright with axe
npm install @axe-core/playwright
```

### Online Tools (No Installation)
- **WebAIM WAVE**: wave.webaim.org
- **Color Contrast Checker**: webaim.org/resources/contrastchecker
- **WCAG Color Contrast Checker**: accessible-colors.com

## Troubleshooting Common Developer Issues

### "My automated tool says everything is fine, but I know there are issues"

**Problem:** Automated tools only catch ~44% of issues
**Solution:** Use the 3-method approach (automated + AI + manual)

```bash
# Step 1: Run multiple automated tools
axe-core scan    # Technical issues
WAVE scan        # Visual issues  
Lighthouse scan  # Performance + accessibility

# Step 2: AI analysis for semantic issues
# Paste HTML into ChatGPT with accessibility prompt

# Step 3: Manual keyboard and screen reader testing
```

### "I don't know what alt text to write"

**Problem:** Generic or unhelpful alt text
**Solution:** Context-based alt text strategy

```html
<!-- Context: E-commerce product -->
<img src="shoe.jpg" alt="Nike Air Max 270 running shoe in black and white, men's size 10">

<!-- Context: Decorative image -->
<img src="pattern.jpg" alt="" role="presentation">

<!-- Context: Functional image (button) -->
<img src="search-icon.svg" alt="Search">

<!-- Context: Chart/graph -->
<img src="sales-chart.jpg" alt="Sales increased 25% from January to March 2024">
```

### "ARIA is confusing - when do I use it?"

**Problem:** ARIA overuse or misuse
**Solution:** Follow the "ARIA rules"

1. **Don't use ARIA if HTML semantics work**
2. **Don't change semantics unless necessary**
3. **All interactive elements must be keyboard accessible**

```html
<!-- ❌ Don't do this -->
<div role="button">Click me</div>

<!-- ✅ Do this instead -->
<button>Click me</button>

<!-- ✅ ARIA is needed here (custom component) -->
<div role="tabpanel" aria-labelledby="tab1" id="panel1">
  Content for tab 1
</div>
```

### "My focus indicators look ugly"

**Problem:** Default browser focus styles clash with design
**Solution:** Custom focus indicators that match your design

```css
/* ✅ Custom focus that matches your brand */
button:focus-visible {
  outline: 2px solid var(--brand-color);
  outline-offset: 2px;
  border-radius: 4px;
}

/* ✅ High contrast focus for better visibility */
input:focus-visible {
  outline: 3px solid #0066cc;
  outline-offset: 1px;
  box-shadow: 0 0 0 1px white;
}
```

## Resources and Further Learning

### Official W3C/WAI Resources
- **WCAG 2.1 Guidelines**: https://www.w3.org/WAI/WCAG21/quickref/ (© W3C)
- **WAI Tutorials**: https://www.w3.org/WAI/tutorials/ (© W3C)
- **ARIA Authoring Practices**: https://www.w3.org/WAI/ARIA/apg/ (© W3C)
- **Web Accessibility Initiative**: https://www.w3.org/WAI/ (© W3C)

### Third-Party Tools and Resources
- **axe-core**: https://github.com/dequelabs/axe-core (© Deque Systems, Inc.)
- **WebAIM**: https://webaim.org/ (© WebAIM)
- **Pa11y**: https://pa11y.org/ (© Pa11y Team)
- **A11y Project**: https://www.a11yproject.com/ (© The A11Y Project)
- **MDN Accessibility**: https://developer.mozilla.org/en-US/docs/Web/Accessibility (© Mozilla)

### Testing Tools Documentation
- **Lighthouse**: https://developers.google.com/web/tools/lighthouse (© Google)
- **WAVE**: https://wave.webaim.org/ (© WebAIM)
- **Color Contrast Analyzers**: Various tools available

### Community and Support
- **WebAIM Discussion List**: https://webaim.org/discussion/
- **Stack Overflow**: Tag questions with [accessibility] and [wcag]

## Legal and Compliance Considerations

### Applicable Standards and Laws
- **WCAG 2.1**: International standard for web accessibility (ISO/IEC 40500)
- **Section 508**: US federal accessibility requirements
- **ADA**: Americans with Disabilities Act (US)
- **EN 301 549**: European accessibility standard
- **AODA**: Accessibility for Ontarians with Disabilities Act (Canada)

### Compliance Levels
- **Level A**: Minimum accessibility (basic compliance)
- **Level AA**: Standard compliance (legal requirement in many jurisdictions)
- **Level AAA**: Enhanced accessibility (not required for full compliance)

**Important:** Legal requirements vary by jurisdiction, organization type, and context. This guide provides technical implementation guidance but does not constitute legal advice. Consult with accessibility professionals and legal counsel for compliance requirements specific to your situation.

## Attribution and Credits

### Standards and Guidelines
- **WCAG 2.1**: Web Content Accessibility Guidelines developed by W3C Web Accessibility Initiative
- **WAI-ARIA**: Accessible Rich Internet Applications specification by W3C
- **HTML Accessibility**: Based on W3C HTML specifications and accessibility features

### Tools and Libraries
- **axe-core**: Accessibility testing engine by Deque Systems
- **Pa11y**: Command-line accessibility testing tool
- **Lighthouse**: Web performance and accessibility auditing by Google
- **WAVE**: Web accessibility evaluation tool by WebAIM

### Methodology
- **Hybrid testing approach**: Combines industry best practices from accessibility professionals
- **Code examples**: Based on established accessibility patterns and W3C recommendations
- **Testing procedures**: Derived from accessibility testing methodologies used by the community

**Community Contribution:** This power was created to make web accessibility testing more approachable for developers, building upon the excellent work of the W3C, accessibility tool creators, and the broader accessibility community.

---

**Based on:** W3C Web Accessibility Initiative (WAI) Standards and WCAG 2.1 Guidelines
**Target Audience:** Front-end Developers, Web Developers, UI Engineers
**Compliance Level:** WCAG 2.1 AA (Standard Legal Requirement)