# VS Code
VS Code is a great lightweight text editor that supports extensions.

# Dev Containers
Dev containers are a novel feature of Visual Studio Code that allow for consistent, repeatable, development environments.

Every developer has run into the issue of a node version being out of sync with the one required to run the project and therefore weird issues start appearing. Dev Containers solves this inconsistency by providing a Docker container in the .devcontainers folder that a developer can start and launch into an environment that is consistent with the setup of other developers on the team.

# Recommended Extensions

## Error Lens
This extension displays error messages inline of the editor. This is really nice for seeing what the compiler is complaining about without having to mouse hover over the squiggly line. I love this extension for increasing development speed.

## Markdown Preview Mermaid Support
Mermaid is quickly becoming the industry standard for UML Diagramming as Code. The extension adds the ability to display Mermaid diagrams in the Markdown Preview window of VS Code.

## Auto Rename Tag
Automatically renames the closing tag in an HTML or JSX file. This is a nice feature so you don't have to set up multi-cursor or write the same change in two different locations.

## Theming
Themes are personal preference and the themes I prefer can change depending on the time of day or how tired I am.

### Themes
1. Dracula
1. Monokai Ristretto
1. VS Code built in Themes
1. GitHub Themes
1. Red
1. Solarized light

### Icon Themes
1. Material Icon Theme
1. VS Code Icons

## Code Spell Checker
Bringing the power of spell check to the editor is great and increases the professional quality of your code. You can parlay this feature with the `settings.json` feature of VS Code to disable certain words from being flagged as misspelled.

Example `settings.json` to add words to the spell checker dictionary:

```json
{
    "cSpell.words": [
        "chakra",
        "zustand",
        "msal"
    ]
}

```

# Extension Recommendation
A nifty feature of VS Code is recommended extensions. It's a way to standardize the tools that developers of the project use to complete their work. When a developer opens the project in VS Code a popup will appear prompting the developer to install the recommended extensions. After agreeing to add the extensions, VS Code will figure out the ones you have not previously installed and install the missing extensions for you.

Below is an example of an `extensions.json` to recommend extensions to other developers.

```json
{
    "recommendations": [
        "dbaeumer.vscode-eslint",
        "esbenp.prettier-vscode",
        "rvest.vs-code-prettier-eslint",
        "streetsidesoftware.code-spell-checker",
        "bierner.markdown-mermaid",
        "usernamehw.errorlens",
        "formulahendry.auto-rename-tag",
        "eamodio.gitlens",
        "christian-kohler.path-intellisense",
        "ms-vscode.vscode-typescript-next",
        "PKief.material-icon-theme"
    ]
}
```
