# Biblioteca de Componentes Com TSDX

fonte: https://tsdx.io/#code-npm-run-build-code-or-code-yarn-build-code

Apesar de todo o entusiasmo recente, configurar uma nova biblioteca TypeScript (x React) pode ser difícil. Entre Rollup, Jest, tsconfig, resoluções Yarn, TSLint e fazer com que o VSCode funcione bem... há um monte de coisas para fazer (e coisas para estragar).

**TSDX é uma CLI sem configuração que ajuda você a desenvolver, testar e publicar pacotes TypeScript modernos** com facilidade, para que você possa se concentrar em sua nova biblioteca incrível e não perder mais uma tarde com configuração.
## [Início rápido](https://tsdx.io/#quick-start)

Com o [TSDX](https://tsdx.io), você pode inicializar rapidamente um novo projeto TypeScript em segundos, em vez de horas. Abra o Terminal e digite:


``` bash
npx tsdx create mylib # substitua `mylib` pelo nome de sua escolha
```

ou

``` bash
yarn create tsdx mylib # substitua `mylib` pelo nome de sua escolha
```


| Template               | Description                                                                                                                                                                                                         |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `basic`                | Uma configuração de projeto TypeScript simples que você pode usar para qualquer tipo de módulo.                                                                                                                     |
| `react`                | Um pacote React com as dependências de desenvolvimento necessárias e `@types` instalados. Além disso, há um playground React com tecnologia [Parcel](https://parceljs.org/) que você pode usar enquanto desenvolve. |
| `react-with-storybook` | Igual ao modelo básico do React, mas com o [React Storybook](https://storybook.js.org/) já configurado.                                                                                                             |

Depois de selecionar um, o TSDX criará uma pasta com o modelo de projeto e instalará todas as dependências. Feito isso, você estará pronto para arrasar! TypeScript, Rollup, Jest, ESlint e todos os outros encanamentos já estão configurados com as melhores práticas. Basta começar a editar `src/index.ts` (ou `src/index.tsx` se você escolheu um dos modelos React) e pronto!

## [Comandos úteis](https://tsdx.io/#useful-commands)

Abaixo está uma lista de comandos que você provavelmente achará úteis:

### [`npm start` ou `yarn start`](https://tsdx.io/#code-npm-start-code-or-code-yarn-start-code)

Executa o projeto no modo de desenvolvimento/observação. Seu projeto será reconstruído mediante alterações. TSDX possui um registrador especial para sua conveniência. As mensagens de erro são impressas e formatadas para compatibilidade na guia Problemas do VS Code.

![](https://user-images.githubusercontent.com/4060187/52168303-574d3a00-26f6-11e9-9f3b-71dbec9ebfcb.gif)

Sua biblioteca será reconstruída se você fizer edições.

### [`npm run build` ou `yarn build`](https://tsdx.io/#code-npm-run-build-code-or-code-yarn-build-code)

Agrupa o pacote na pasta `dist`. O pacote é otimizado e agrupado com Rollup em múltiplos formatos (CommonJS, UMD e ES Module).

![](https://user-images.githubusercontent.com/4060187/52168322-a98e5b00-26f6-11e9-8cf6-222d716b75ef.gif)

### [`npm test` ou `yarn test`](https://tsdx.io/#code-npm-test-code-or-code-yarn-test-code)

Executa seus testes usando Jest.

### [`npm run lint` ou `yarn lint`](https://tsdx.io/#code-npm-run-lint-code-or-code-yarn-lint-code)

Executa o Eslint com Prettier em arquivos .ts e .tsx. Se você quiser personalizar o eslint, pode adicionar um bloco `eslint` ao seu package.json, ou pode executar `yarn lint --write-file` e editar o arquivo gerado `.eslintrc.js`.

### [`prepare` script](https://tsdx.io/#code-prepare-code-script)

Agrupa e empacota na pasta `dist`. Executa automaticamente quando você executa `npm publish` ou `yarn publish`. O script `prepare` executará o equivalente a `npm run build` ou `yarn build`. Ele também será executado se seu módulo for instalado como uma dependência do git (ou seja: `"mymodule": "github:myuser/mymodule#some-branch"`), para que possa ser dependente sem que o código transpilado seja verificado no git.

## [Melhores Práticas](https://tsdx.io/#best-practices)

O TSDX inclui melhores práticas e otimizações para pacotes NPM modernos. Isso inclui coisas como a capacidade de ter diferentes builds de desenvolvimento e produção, múltiplos formatos de pacote, otimizações adequadas do lodash, treeshaking e minificação, para citar alguns. Todas essas funcionalidades vêm prontas para uso com o TSDX. Embora você provavelmente não precise configurar nada, [você pode fazer isso com tsdx.config.js](https://tsdx.io/customization).

