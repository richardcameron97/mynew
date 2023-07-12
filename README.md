# mynew
{
  "customizations": {
    "vscode": {
      "extensions": [
        "dbaeumer.vscode-eslint",
        "esbenp.prettier-vscode",
        "freeCodeCamp.freecodecamp-dark-vscode-theme"
      ]
    }
  },
  "dockerFile": "Dockerfile",
  "forwardPorts": [3000, 8000, 27017],
  "portsAttributes": {
    "8000": {
      "label": "Learn",
      "onAutoForward": "openPreview"
    }
  },
  "postCreateCommand": "cp sample.env .env && npm ci",
  // It is more reliable to start these processes oneself
  // "postStartCommand": "mongod &",
  // "postAttachCommand": "npm run develop",
  "workspaceFolder": "/workspaces/${localWorkspaceFolderBasename}"
}
