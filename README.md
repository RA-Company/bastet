# Bastet

List of additional CSS styles to extend @ng-bootstrap/ng-bootstrap library.

## Installation

Get clone of project into your local machine.

Add the following lines to your `angular.json` file:

```json
{
  "projects": {
    "<your-project-name>": {
      "architect": {
        "build": {
          "options": {
            "styles": [
              "node_modules/bootstrap/dist/css/bootstrap.min.css",
              "<bastet folder>/styles.css",
              "src/styles.css"
            ]
          },
          "configurations": {
            "production": {
              
              "assets": [
                {
                  "glob": "**/*",
                  "input": "src/assets/",
                  "output": "/assets"
                },
                {
                  "glob": "**/*",
                  "input": "<bastet folder>/assets/",
                  "output": "/assets/bastet"
                }
              ]
            },
            "development": {

              "assets": [
                {
                  "glob": "**/*",
                  "input": "src/assets/",
                  "output": "/assets"
                },
                {
                  "glob": "**/*",
                  "input": "<bastet folder>/assets/",
                  "output": "/assets/bastet"
                }
              ]
            }
          }
        }
      }
    }
  }
}
```