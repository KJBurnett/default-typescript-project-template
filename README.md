# default-typescript-project-template
A useful starting template for your new typescript project! Comes with playwright and jest typing preconfigured.

*tsconfig.json presets*
```json
{
  "include": [
    "src/**/*.ts",
    "types/**/*.d.ts",
    "index.ts",
    "src/api/exceptions/*.json"
  ],
  "exclude": [
    "node_modules"
  ],
  "compilerOptions": {
    "types": [
      "node",
      "jest"
    ],
    "typeRoots": [
      "types",
      "node_modules/@types"
    ],
    "moduleResolution": "node",
    "alwaysStrict": true,
    "module": "commonjs",
    "outDir": "build",
    "sourceMap": true,
    "target": "es2019",
    "declaration": true,
    "noUnusedLocals": true,
    "experimentalDecorators": true,
    "strict": true,
    "allowSyntheticDefaultImports": true,
    "resolveJsonModule": true
  }
}
```

*package.json presets*
```json
{
  "name": "default-typescript-project-template",
  "version": "1.0.0",
  "description": "A template project to easily start from scratch with your new typescript project because it often is very confusing!...",
  "main": "build/index.js",
  "license": "MIT",
  "scripts": {
    "build:ts": "tsc",
    "build": "yarn build:ts"
  },
  "dependencies": {
    "playwright": "^1.39.0",
    "@types/jest": "^29.2.4",
    "@types/node": "14.0.14",
    "typescript": "^5.2.2"
  }
}
```

*.vscode/launch.json presets*
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "[DEBUG] main index.js",
            "skipFiles": [
                "<node_internals>/**"
            ],
            "program": "./build/index.js",
            "preLaunchTask": "${defaultBuildTask}"
        }
    ]
}
```

*.vscode/tasks.json presets*
```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "type": "typescript",
            "tsconfig": "tsconfig.json",
            "option": "watch",
            "problemMatcher": [
                "$tsc-watch"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "label": "tsc: build - tsconfig.json"
        }
    ]
}
```
