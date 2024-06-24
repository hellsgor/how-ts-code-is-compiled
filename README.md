# 4.2 How TS code is compiled

## Packages

- typescript - сам TypeScript
- ts-node-dev - запускает TS-код в режиме разработки

## Commands

- `npx tsc ./src/index.ts` - компиляция;
- `node ./dist/index.js` - запуск скопмпилированного кода;
- `npx tsc ./src/index.ts --outDir ./dist` - указываем директорию в которую хотим компилировать ts-файлы;
- `npx ts-node-dev ./src/index.ts` - запускает ts-код в режиме разработки;
- `npx ts-node-dev --respawn ./src/index.ts` - флаг `--respawn` перезапускает ts-код при его изменении
