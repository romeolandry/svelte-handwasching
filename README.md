## Project hand wasching with svlet

Read th oficial documentation [hier](./official-docs.md).

## Bootstrap integration

### **Using Sveltestarp**

this integration don't require the installation of Bootstrap in the project. 

```
npm install --save sveltestrap svelte
```
- Integrate all bootstrap components in to the Project using into `app.svlete`
```
<script>
  import { Styles } from 'sveltestrap';
</script>
<Styles />
```
and it into devdependancie of node. open `package.json`.

```
"devDependencies": {
    "sveltestrap": "*.*.*",
    ...
  },
```
**Note:** This integration support only the bootstrap version supported by [Svletestrap](https://sveltestrap.js.org/?path=/story/components--get-started)

### **Install Bootstrap via npm or inclur Url in index.html**



    