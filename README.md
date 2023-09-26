# runProyect

start a proyect run ->
```
npm init -y
npm install -D typescript
npm install -D ts-node
npm install -D nodemon
```
EXPRESS
--
- Those are the dependencies for node.js express
    - if fist does not work try with the secon option

    ```
    npm install express
    npm i --save-dev @types/express

    npm i cors
    npm i --save-dev @types/cors

    npm i dotenv
    ```

JSON CONFIGs
--
- then create tsconfig.json

    - this will be the configuration:
    ```
    {
        "compilerOptions": {
            // "module":"CommonJS",
            "module": "NodeNext",
            "moduleResolution": "node",
            "baseUrl": "src",
            "outDir": "dist",
            "sourceMap": true,
            "noImplicitAny": true,
        },
        "include": ["src/**/*"]
    }
    ```

- Now you need to create nodemon.json file
    - this will be the configuration:
    ```
    {
    "watch":["src"],
    "ext": ".ts,.js",
    "exec": "ts-node ./src/index.ts"
    }   
    ```
- Do not forget to add start into package.json
    - this will be the configuration:
    ```
    "scripts": {
        "start": "nodemon",
    }   
    ```
