Step 1. install the dependences

```bash
pnpm add --save-dev eslint @eslint/js typescript typescript-eslint
```

Step 2. create `eslint.config.mjs`

```js
// @ts-check

import eslint from '@eslint/js';
import tseslint from 'typescript-eslint';

export default tseslint.config(
  eslint.configs.recommended,
  tseslint.configs.recommended,
);

```

Step 3. add the script

```json
 "scripts": {
    "lint": "eslint src",
  },
```

## integrate the prettier

```bash
pnpm add --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier
```

```js
// @ts-check

import eslint from '@eslint/js';
import tseslint from 'typescript-eslint';
import eslintConfigPrettier from 'eslint-config-prettier';

export default tseslint.config(
  eslint.configs.recommended,
  tseslint.configs.recommended,
  eslintConfigPrettier,
);

```

