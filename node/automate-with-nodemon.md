We use `nodemon` to make the server restart automatically when we save the code.

First, install the `nodemon` dependence.

```bash
# install locally
pnpm add nodemon -D

# install globally
pnpm add nodemon -g
```

Then, add the script to `package.json`
```json
 "scripts": {
    "dev": "nodemon src/index.js"
  },
```

