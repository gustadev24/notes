# Process to init the commit lint in a project
- Install husky
```bash
pnpm add -D husky
```
- Init husky
```bash
pnpm husky init
```
- On package.json, add the following script
```json
"scripts": {
  "commitlint": "commitlint --edit"
}
```
- Create a commit-msg hook
```bash
touch .husky/commit-msg
```
- Put the following content in the commit-msg file
```bash
pnpm commitlint ${1}
```
