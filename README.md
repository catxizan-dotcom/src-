# src-


{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Executar app",
      "program": "${workspaceFolder}/src/index.js",
      "env": { "NODE_ENV": "development" },
      "console": "integratedTerminal",
      "skipFiles": ["<node_internals>/**"]
    },
    {
      "type": "node",
      "request": "attach",
      "name": "Anexar ao processo",
      "port": 9229
    }
  ],
  "compounds": [
    { "name": "Servidor + Cliente", "configurations": ["Executar app", "Anexar ao processo"] }
  ]
}