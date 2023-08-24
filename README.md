# Project configuration with NODE.js, Typescript and Jest 

## :green_book: Typescript installation and configuration
1. After starting the NODE.js project with ``npm init`` command, you can install typescript by printing in the console ``npm install -D typescript``. :arrow_right:[read](https://www.npmjs.com/package/typescript)
2. To instal node types use command ``npm install -D @types/node ``:arrow_right:[read](https://www.npmjs.com/package/@types/node)
3. Next type in the console ``tsc --init`` - generate tsconfig.json
   Acording to options description, I have choosen following custom configurations:
   - "rootDirs": ["./server/src", "./server/__tests__"]
   - outDir: './dist'
   - noEmitonError: false,
   - "removeComments": true, 
   - "sourceMap": true 
               
   
## :microscope: ESLint installation and configuration
4.  ``npm install -D eslint`` :arrow_right:[read](https://www.npmjs.com/package/eslint)
5.  ``npm init @eslint/config`` - to generate configuration file for eslint.
   I put following answers:</br>
√ How would you like to use ESLint? :white_check_mark: ``To check syntax and find problems`` </br>
√ What type of modules does your project use? :white_check_mark: ``JavaScript modules (import/export)`` </br>
√ Which framework does your project use? :white_check_mark: ``None of these`` </br>
√ Does your project use TypeScript? :white_check_mark: ``Yes`` </br>
√ Where does your code run? :white_check_mark: ``NODE`` </br>
√ What format do you want your config file to be in? :white_check_mark: ``JavaScript`` </br>
√ Would you like to install them now? :white_check_mark: ``Yes`` </br>
√ Which package manager do you want to use? :white_check_mark:  ``npm`` </br>

:beginner: In ``.eslintrs.js`` I have added the following custom configuration:
- to ``env`` added ``"node": true``
- to ``rules`` added ``"@typescript-eslint/no-var-requires": "off"`` - for use imports instead of require
- added module ``"ignorePatterns": ['dist/**']`` - to exclude .js files in dist folder to be checked by eslint

### :rocket: You can add in VS extensions ESLint - it indicates errors in the code before runing eslint with command ``npx eslint .``

## :test_tube: Jest installation and configuration
You can performed installation according to descriprion here :arrow_right: [read](https://www.npmjs.com/package/ts-jest)

For mocking, I have installed ``jest-mock`` :arrow_right: [read](https://github.com/jestjs/jest).
