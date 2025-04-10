First, create the `.env` file and `src/config/index.ts` file

```bash
touch .env 
cd src/config && touch index.ts
```

install the `donenv` dependence

```bash
pnpm add dotenv
```

The `dotenv` package is used to read environment variables from a `.env` file.

```ts
// src/config/index.ts
import dotenv from 'dotenv';

dotenv.config();

interface Config {
  port: number;
  nodeEnv: string;
}

const config: Config = {
  port: Number(process.env.PORT) || 3000,
  nodeEnv: process.env.NODE_ENV || 'development',
};

export default config;
```

```toml
# .env
PORT=3000
NODE_ENV=development
```
