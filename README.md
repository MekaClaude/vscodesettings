# Visual Studio Code Custom setting to speed up your workflow

A set of custom settings inspired from watching this video from [Grafikart](https://www.youtube.com/@grafikart)

[![Ma-configuration-Visual-Studio-Code-YouTube](https://user-images.githubusercontent.com/20024130/213687387-1e54e9ff-4a21-4891-8f82-040179c4a436.png)](https://www.youtube.com/watch?v=GFmE5_8xypY)

The video is in french but you can get a lot from just watching. 

## Here is the settings I use now : **settings.json**

````
{
    /* The zoom level is ajusted for the iMac 21 inches if you ar using a laptop 13", 14", 15", 16" or 17" your zoom level should be incrised */
    "window.zoomLevel": 0.25,
    /* When I need the menimap I show it but by default it is hidden */
    "editor.minimap.enabled": false,
    "editor.formatOnSave": false,
    "editor.formatOnPaste": false,
    "editor.renderWhitespace": "trailing",
    "editor.linkedEditing":true,
    "editor.suggest.insertMode": "replace",
    "editor.acceptSuggestionOnCommitCharacter": false,
    "files.autoSave": "onFocusChange",
    "files.defaultLanguage": "css",
    "explorer.autoReveal": false,
    "explorer.confirmDragAndDrop": false,
    "explorer.confirmDelete": false,
    "workbench.tree.indent": 15,
    "workbench.tree.renderIndentGuides":"always",
    "workbench.editor.enablePreview": false,
    "emmet.triggerExpansionOnTab": true,
    "git.confirmSync": false,
    "git.enableSmartCommit": true,
    /* you can change the default font for your editor. I suggest you look here https://fonts.google.com/?category=Monospace */
    "editor.fontFamily": "'Red Hat Mono',Menlo, Monaco, 'Courier New', monospace",
    "editor.fontLigatures":true,
    "editor.fontSize": 12,
    "editor.lineHeight": 18,
    "editor.guides.bracketPairs": true,
    "gitlens.hovers.currentLine.over": "line",
    /* You will first need to install the multi-command extension to create custom commands */
    "multiCommand.commands": [
        {
            "command": "multiCommand.hideBars",
            "sequence": [
                "workbench.action.toggleSidebarVisibility",
                "workbench.action.toggleActivityBarVisibility",
            ]
        }
    ]
}

````

## This is my keybindings : keybindings.json

````
// Placer vos combinaisons de touches dans ce fichier pour remplacer les valeurs par défaut
[
    /* hide the left bars quickly */
    {
        "key": "alt+1",
        "command": "multiCommand.hideBars"
    },
    /* select word and expand selection to the line */
    {
        "key": "ctrl+d",
        "command": "editor.action.smartSelect.expand",
        "when": "editorTextFocus",
    },
    /* select the same in the faster and modify in multiple lines  */
    {
        "key": "ctrl+shift+d",
        "command": "editor.action.addSelectionToNextFindMatch",
        "when": "editorFocus",
    },
    /* quick show the list of commandes */
    {
        "key": "ctrl+p",
        "command": "workbench.action.showCommands",
    },
    /* to show all the files open to quick open */
    {
        "key": "ctrl+o",
        "command": "workbench.action.quickOpen",
    },
      /* to reveal the file inside de OS */
    {
        "key": "ctrl+shift+o",
        "command": "revealFileInOS",
    },
    /* to naviguate into a file and check all the major function or selector  */
    {
        "key": "ctrl+r",
        "command": "workbench.action.gotoSymbol",
    },
    {
        "key": "ctrl+n",
        "command": "explorer.newFile",
    },
    {
        "key": "ctrl+alt+l",
        "command": "editor.action.formatDocument",
    },

]

````
