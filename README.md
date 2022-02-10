# VSCode command client

This directory contains client code for communicating with the [VSCode command server](https://marketplace.visualstudio.com/items?itemName=pokey.command-server).

## Usage

Example using [Cursorless](https://marketplace.visualstudio.com/items?itemName=pokey.cursorless):

```python
run_vscode_command(
    'cursorless.command',
    {
        'version': 1,
        'spokenForm': 'take near',
        'action': 'setSelection',
        'targets': [{
            'type': 'primitive',
            'mark': {'type': 'decoratedSymbol', 'symbolColor': 'default', 'character': 'n'}
        }],
        'extraArgs': [],
        'usePrePhraseSnapshot': False
    },
    wait_for_finish=True,
)
```
