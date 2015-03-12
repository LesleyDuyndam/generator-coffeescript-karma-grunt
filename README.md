# Generator | CoffeeScript & Karma
A generator for Yeoman to scaffold CoffeeScript projects, test it with karma (Jasmine), run tasks with Grunt.

## Installation
First you need to install the generator on your machine. Run the next command in the terminal;

```
npm install -g generator-coffeescript-karma
```


Run yo inside the project root directory and select the 'Coffee Karma' generator.

```
yo
```

Yeoman will create a project with the following structure:

    .
    ├── dist
    │   └── projectName.min.js ( Will be generated when run 'grunt uglify' )
    ├── src
    |   └── coffee
    │       ├── projectName.coffee
    │       └── classes
    │           └── main.class.coffee
    ├── test
    |   └── coffee    
    │       ├── projectName.test.coffee
    │       └── classes
    │           └── main.class.test.coffee
    ├── .gitignore
    ├── bowerrc
    ├── bower.json
    ├── package.json
    ├── gruntfile.coffee
    ├── karma.config.coffee
    └── README.md

That's all there is to it! You can start coding, testing and building right out of the box!


## Usage

### Testing
Great, you are ready to write awesome code! But off course, you want to run tests, lots and lots of tests. Start Karma by running the 'grunt karma' command in the terminal.

```
grunt karma
```

Karma outputs the test reports directly in the terminal. If you prefer a html based test report go to 'server/port/debug.html' while 'grunt karma' is running. Most likely this url is;

```
http://localhost:9876/debug.html
```

> It is possible you have to refresh to get the last report

### Compiling
If you would like to compile coffeeScript automatically on file change, activate the watcher. This is easily done by running the 'grunt watch' command in the terminal.

```
grunt watch
```

Otherwise, you could run 'grunt coffee' in the terminal to compile the CoffeeScript files manually.

```
grunt coffee
```

> Compiled coffeeScript files are stored in the 'src/javascript' folder.

### Building
If your code is ready for production, simply run 'grunt uglify' in your terminal. This will uglify the most recent compiled coffeeScript files in the 'src/javascript' directory.

```
grunt uglify
```
