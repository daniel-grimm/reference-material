# VS Code
VS Code is a great lightweight text editor that supports extensions.

# Dev Containers
Dev containers are a novel feature of Visual Studio Code that allow for consistent, repeatable, development environments.

Every developer has run into the issue of a node version being out of sync with the one required to run the project and therefore weird issues start appearing. Dev Containers solves this inconsistency by providing a Docker container in the .devcontainers folder that a developer can start and launch into an environment that is consistent with the setup of other developers on the team.

# Recommended Extensions

## Error Lens
Shows error messages inline of the editor.

## Markdown Preview Mermaid Support
Adds the ability to display Mermaid diagrams in the Markdown Preview window.

## Auto Rename Tag
Automatically renames the closing tag.

## Dracula official
Dark (but not too dark) theme. This is very popular and supported by other tooling like Warp (terminal) and Visual Studio.

## Material Icon Theme
Nice Visual flair for the Explorer view.

## Code Spell Checker

# Extension Recommendation
VS Code supports a JSON format to recommend extensions to be used in the repo.

```json
{
    "recommendations": [
        "dbaeumer.vscode-eslint",
        "esbenp.prettier-vscode",
        "rvest.vs-code-prettier-eslint",
        "esbenp.prettier-vscode",
        "streetsidesoftware.code-spell-checker",
        "bierner.markdown-mermaid"
    ]
}
```