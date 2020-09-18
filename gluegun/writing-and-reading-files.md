# Writing and reading files

To manipulate files in **gluegun**, use the *filesystem* module.

To create and write in an file, use the `write` command:

```typescript
  const {  filesystem} = toolbox;
  const myName = 'Renan';
  filesystem.write("myname.txt", passwords);
```
To read an file, use the `read` command:

```typescript
  const { filesystem } = toolbox;
  const myName = filesystem.read("myname.txt");
```

> Replace {cli-name} with your cli name

Thank you!
