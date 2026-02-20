# 🎉 claude-code-enhance - Enhance Your Code Experience Effortlessly!

[![Download claude-code-enhance](https://img.shields.io/badge/Download-Release-blue.svg)](https://github.com/buffbeard920/claude-code-enhance/releases)

## 🚀 Getting Started

Welcome to **claude-code-enhance**! This tool enhances the Claude Code extension for VSCode by adding features like code highlighting and LaTeX rendering. Follow these steps to download and run the software smoothly.

## 📥 Download & Install

To get started, you need to download the latest version from our Releases page. Click the link below:

[Visit this page to download](https://github.com/buffbeard920/claude-code-enhance/releases)

1. Click the link above to go to the Releases page.
2. Look for the latest version.
3. Download the file suitable for your platform (Windows or Linux).
   
### 🎯 System Requirements

- **Claude Code Extension:** Version 2.1.31 or higher.
- **Platforms Supported:** 
  - Windows (win32-x64)
  - Linux (linux-x64)

### 🔧 Installation Methods

You can install the enhancement using two methods: a patch script (recommended) or manual installation.

#### 🛠️ Method 1: Patch Script (Recommended)

1. Open your command line.
2. Change the directory to where **claude-code-enhance** is located:
   ```bash
   cd claude-code-enhance
   ```
3. Run the patch script:
   ```bash
   node patch_extension.js
   ```

The script will automatically:
- Find the currently installed Claude Code extension.
- Copy the `enhance.js` file to the extension directory.
- Update the CSP policy to allow CDN resources.
- Inject the enhancement script for you.

#### 📁 Method 2: Manual Installation

1. Navigate to the `webview/` directory in the downloaded files.
2. Copy the `enhance.js` file into the `webview/` directory of your Claude Code extension.
3. Edit the `extension.js` file:
   - Modify the CSP policy to include the necessary rules.
4. In your HTML template, inject the `<script>` tag for `enhance.js`.

### 🔄 After Installation

To see the changes, reload your VSCode window. You can do this by pressing `Ctrl + Shift + P` and selecting `Developer: Reload Window`.

## 💡 Features

Once you have installed **claude-code-enhance**, you can explore its powerful features:

- **Code Syntax Highlighting**: Supports over 180 programming languages, thanks to Highlight.js.
- **LaTeX Formula Rendering**: Display matrices, fractions, and integrals using KaTeX.
- **AI Dialogue Copying**: Copy AI response content to your clipboard easily. The content is formatted in Markdown.
- **DOM Inspection Tool**: Press `Ctrl + Shift + D` to export the DOM structure for analysis.
- **Dark Table Theme**: Enjoy a gradient header, hover highlights, and rounded borders in tables.
- **Code Auto-Wrapping**: Long command lines wrap automatically for better readability.
- **Scroll Wheel Zoom**: Zoom in and out using `Ctrl` and the mouse wheel, with a range of 50% to 200%.
- **List Style Fixes**: Numbered lists display correctly.

## 📈 Usage Instructions

### 🤖 AI Dialogue Copying

To copy AI responses easily:

1. Hover your mouse over the end of an AI reply.
2. A "Copy" button will appear in the bottom right corner.
3. Click the button to copy the AI response in Markdown format.
4. The tool automatically excludes "Thinking" and tool invocation content but retains the following:
   - Code blocks
   - Tables
   - LaTeX formulas
   - Lists

### 🧩 Using the DOM Inspection Tool

The DOM inspection tool helps you analyze web structures. To use this tool:

1. Press `Ctrl + Shift + D` to activate the feature.
2. The tool will generate a report on the DOM structure for your review.

## 🛠️ Troubleshooting

- **Installation Issues**: If you encounter problems, ensure you have the correct version of the Claude Code extension installed.
- **Feature Activation**: If features do not appear, try reloading the VSCode window again.
- **Script Errors**: For any script errors, double-check your CSP modifications in the `extension.js` file.

By following these instructions, you should have a seamless experience using the **claude-code-enhance** application. Enjoy your enhanced coding experience!