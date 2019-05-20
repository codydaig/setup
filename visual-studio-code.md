# Visual Studio Code

We'll be using Visual Studio Code as our primary text editor of choice. While it comes with a great set of default settings, we'll want to make a few adjustments to help maximize our learning during the course.

## Configuration

### Settings

```javascript
{
  "editor.parameterHints.enabled": false,
  "editor.renderWhitespace": "all",
  "editor.snippetSuggestions": "none",
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "emmet.showExpandedAbbreviation": "never",
  "files.trimTrailingWhitespace": true,
  "javascript.suggest.enabled": false,
  "javascript.updateImportsOnFileMove.enabled": "never",
  "javascript.validate.enable": false,
}
```

### Install

* Live Share
  * Log in with your GitHub account when Live Share prompts you to do so.

### Disable

* Source Control from left Activity Bar sidebar
  * Right click the Git branch icon on the left Activity Bar sidebar, then `Hide`. This will prevent you from accidentally using non-terminal Git commands via Visual Studio Code.

![](.gitbook/assets/image.png)

### Banned 

* Prettier
* Quokka
* Using Git from within the Visual Studio Code GUI is prohibited. You may use Git functionality only from within the terminal. \(If you're using Git via integrated terminal, that's fine.\)

