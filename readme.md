yarn init -y
yarn add typescript -D
yarn add express
yarn add cors
yarn add -d @types/node @types/typescript @types/express @types/cors ts-node-dev
yarn tsc --init


alterar tsconfig.json:
{
  "compilerOptions": {
    "target": "es2020",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}

criar pasta src

alterar package.json, e colocar scripts:
"scripts": {
    "dev": "ts-node-dev --respawn --transpile-only ./src/index.ts",
    "build": "tsc",
    "start": "node ./dist"
}

urlenconded 

# Criar os seguintes repositórios e iniciar projeto
-> growdev-scrapbook-api
-> growdev-scrapbook

# Primeira vez
git init
git add .
git commit -m "mensagem aqui"
git remote add origin ... (pegar no github)
git push --set-upstream origin master

# Demais vezes
git add .
git commit -m "mensagem aqui"
git push