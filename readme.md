tsconfig.json
"outDir": "app/js" -- where we want typscript to place our compiled files

.typingsrc
-- add the below if you need to use a proxy
{
	"proxy": "",
	"httpsProxy": ""
}

package.json:
  "scripts": {
	"preinstall": "npm i typings -g",
    "start": "tsc && concurrently \"npm run tsc:w\" \"npm run lite\" ",
    "lite": "lite-server",
    "postinstall": "typings install",
    "tsc": "tsc",
    "tsc:w": "tsc -w",
    "typings": "typings"
  },
  
  --- or ---
    "scripts": {
    "start": "tsc && concurrently \"tsc -w\" \"lite-server\" ",
    "lite": "lite-server",
    "tsc": "tsc",
    "tsc:w": "tsc -w"
  },



1. isntall node
2. create project dir
3. create package.json, tsconfig.json, systemjs.config.js and .typingsrc (if necessary)
4. install packages npm install
5. make app directory
6. Go, go, go!!!
7. start app with npm start


Other nice to know:
1. You may need to manually install typings using 'npm run typings install'


Resources:
http://blogs.msmvps.com/deborahk/angular-2-getting-started-problem-solver/
https://angular.io/docs/ts/latest/quickstart.html