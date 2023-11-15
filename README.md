# default-typescript-project-template
A useful starting template for your new typescript project! Comes with playwright and jest typing preconfigured.

*tsconfig.json preset*
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
