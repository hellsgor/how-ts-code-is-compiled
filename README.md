# 4.2 How TS code is compiled

## Packages

- typescript - сам TypeScript
- ts-node-dev - запускает TS-код в режиме разработки

## Commands

- `npx tsc ./src/index.ts` - компиляция;
- `node ./dist/index.js` - запуск скомпилированного кода;
- `npx tsc ./src/index.ts --outDir ./dist` - указываем директорию в которую хотим компилировать ts-файлы;
- `npx ts-node-dev ./src/index.ts` - запускает ts-код в режиме разработки;
- `npx ts-node-dev --respawn ./src/index.ts` - флаг `--respawn` перезапускает ts-код при его изменении

## tsconfig parameters

- `target` - версия ES под которую хотим компилировать TS-код. По-умолчанию - es5. Для последний последних браузеров - `esnext`;
- `lib` - если разрабатываем приложение для браузера - `"dom", esnext`; если для NodeJS - опустить параметр или `esnext`;
- `module` - указывается в зависимости от используемой платформы, определяет системы модулей, которые будут сгенерированы в итоговом бандле. `"commonjs"` - для NodeJS; `esnext`- для браузеров;
- `outDir` - в какую директорию необходимо скомпилировать TS-код, например, `"./dist/"`;
- `strict` - важно следить, чтобы его значение всегда было `true` - строгий режим TypeScript;

## NodeJS types

Разрабатывая приложение для NodeJS, можно столкнуться с тем, что TypeScript не может подтянуть типы для NodeJS. Например:

```TypeScript
import {} from 'fs';
```

Чтобы это исправить необходимо установить тайпинги для NodeJS с помощью команды `npm install @types/node`.
