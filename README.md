# Variables Builder

![Cover](https://github.com/miguelsolorio/figma-variables-builder/blob/main/assets/cover.png?raw=true)

A [Figma plugin](https://www.figma.com/community/plugin/1319728928151105267) for generating local variables using JSON

## How to use

Use the format below and always include a mode for each variable. Colors must be in a hex format and can support alpha channels via 8 digits.

```json
{
  "$CollectionName": {
    "$VariableName": {
      "$Mode": "$Hex",
      "$Mode": "$Hex"
    },
    "$VariableName": {
      "$Mode": "$Hex",
      "$Mode": "$Hex"
    },
    "$VariableName": {
      "$Mode": "$Hex",
      "$Mode": "$Hex"
    }
  }
}
```

If you only have a single mode, you can use the short format below and they will be added to the default mode:

```json
{
  "$CollectionName": {
    "$VariableName": "$Hex",
    "$VariableName": "$Hex",
    "$VariableName": "$Hex"
  }
}
```

- `$CollectionName` is the name of your collection
- `$VariableName` is the name of your variable
- `$Mode` is the name of your mode, each variable must contain the same modes
- `$Hex` is the hex code of your color, supports 8-digit hex codes for transparency

### Example

```json
{
  "Tokens": {
    "tab-activeBackground": {
      "Dark": "#1f1f1f",
      "Light": "#ffffff",
      "Monokai": "#272822"
    },
    "tab-activeBorder": {
      "Dark": "#1f1f1f",
      "Light": "#f8f8f8",
      "Monokai": "#00000000"
    },
    "tab-activeBorderTop": {
      "Dark": "#0078d4",
      "Light": "#005fb8",
      "Monokai": "#00000000"
    },
    "tab-activeForeground": {
      "Dark": "#ffffff",
      "Light": "#3b3b3b",
      "Monokai": "#ffffff"
    },
    "tab-border": {
      "Dark": "#2b2b2b",
      "Light": "#e5e5e5",
      "Monokai": "#1e1f1c"
    },
    "tab-hoverBackground": {
      "Dark": "#1f1f1f",
      "Light": "#ffffff",
      "Monokai": "#00000000"
    },
    "tab-inactiveBackground": {
      "Dark": "#181818",
      "Light": "#f8f8f8",
      "Monokai": "#34352f"
    },
    "tab-inactiveForeground": {
      "Dark": "#9d9d9d",
      "Light": "#868686",
      "Monokai": "#ccccc7"
    },
    "tab-lastPinnedBorder": {
      "Dark": "#cccccc33",
      "Light": "#d4d4d4",
      "Monokai": "#414339"
    },
    "tab-unfocusedActiveBorder": {
      "Dark": "#1f1f1f",
      "Light": "#f8f8f8",
      "Monokai": "#00000000"
    },
    "tab-unfocusedActiveBorderTop": {
      "Dark": "#2b2b2b",
      "Light": "#e5e5e5",
      "Monokai": "#00000000"
    },
    "tab-unfocusedHoverBackground": {
      "Dark": "#1f1f1f",
      "Light": "#f8f8f8",
      "Monokai": "#00000000"
    }
  }
}
```

## Run Plugin Locally

1. Clone this repository
2. Install dependencies with `npm install`
3. Build the plugin with `npm run build` or `npm run watch`