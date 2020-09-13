# Creating command

Create an file in commands folder with the command name. Example:

```bash
touch foo.ts
```
Add a code like this in to created file;

```typescript
import { GluegunCommand, GluegunToolbox } from 'gluegun';

const CommandsConfig: GluegunCommand = {
    name: 'foo',
    description:"Foo bar command",
    run: async (toolbox: GluegunToolbox) => {
      const { success } = toolbox.print;

      return success('bar');
    }
}

module.exports = CommandsConfig;
```
#### Properties:

- `name` : Command name
- `description` : Add an description to command
- `run` : Function that's run the command

Now, put it in your terminal:
```bash
{cli-name} foo
```

> Replace {cli-name} with your cli name

Congratulations, you created your first command!
