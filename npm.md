---
title: npm commands
---

# npm commands

## Short Contents

- [Getting Started](#getting-started)
- [How do I stop a command?](#how-do-i-stop-a-command)
- [npm start [command]](#npm-start-command)
- [npm install [command]](#npm-install-command)
- [npm uninstall [command]](#npm-uninstall-command)
- [package.json](#packagejson)
- [file system](#file-system)
- [References](#references)

## Contents

- [npm commands](#npm-commands)
  - [Short Contents](#short-contents)
  - [Contents](#contents)
  - [Getting Started](#getting-started)
    - [What's inside this document?](#whats-inside-this-document)
      - [How to use](#how-to-use)
      - [Audience](#audience)
      - [Content](#content)
    - [More Commands?](#more-commands)
    - [npm CLI](#npm-cli)
  - [How do I stop a command?](#how-do-i-stop-a-command)
  - [npm start [command]](#npm-start-command)
  - [npm install [command]](#npm-install-command)
    - [npm install](#npm-install)
      - [shorthand](#shorthand)
      - [Just, npm install?](#just-npm-install)
      - [When to use?](#when-to-use)
      - [How can I check?](#how-can-i-check)
      - [What are packages?](#what-are-packages)
    - [npm install \<package-name\>](#npm-install-package-name)
      - [shorthand](#shorthand-1)
      - [When to use?](#when-to-use-1)
    - [npm install -S \<package-name\>](#npm-install--s-package-name)
      - [What does the -S flag mean?](#what-does-the--s-flag-mean)
      - [How to use -S flags here?](#how-to-use--s-flags-here)
      - [How do I check?](#how-do-i-check)
      - [Differences between `npm install` and `npm install -S`](#differences-between-npm-install-and-npm-install--s)
    - [npm install -D \<package-name\>](#npm-install--d-package-name)
      - [What does the -D flag mean?](#what-does-the--d-flag-mean)
      - [How to use -D flags here?](#how-to-use--d-flags-here)
      - [How do I check?](#how-do-i-check-1)
      - [Differences between `npm install` and `npm install -D`](#differences-between-npm-install-and-npm-install--d)
  - [npm uninstall [command]](#npm-uninstall-command)
  - [package.json](#packagejson)
    - [What is JSON?](#what-is-json)
      - [Basic JSON rules](#basic-json-rules)
  - [file system](#file-system)
  - [References](#references)
    - [npm commands](#npm-commands-1)
    - [package.json](#packagejson-1)

## Getting Started


### What's inside this document?

#### How to use

This document is used only as a reference, it's not expected for any student to know all of this material here. 

It's meant for you to refer back to and help you understand the use of specific npm commands.

#### Audience
It primarily relevant to  both students and mentors that are using **npm** at their current stage in the course.

#### Content

This document only goes through the commands you may need in this course, however it doesn't go into the what, why and the history of **npm**. The decision to teach you all this, will be on the mentors. 

> Note that this document has been simplified to be used by both students and mentors

### More Commands?

Yes! More commands to learn. It's important that as software developers, that you can expand your the toolbox of skills you already have. To learn more useful tools that professional developers may use on a daily basis. 

Even if you don't use **npm** in your future development job, you will have gained additional experience on how CLI tools (Command Line Interface Tools) work.

### npm CLI
Just like **git**. **npm** comes with it different commands option and many accompanying option flags meaning.

```shell
npm <command-option> - -<option-flag> <parameter>
```

- `npm` : is the **command prefix**
- `<command option>` - is the **command option**
- `-<option-flag>` - is the **command option flag**
- `<parameter>` - is the **command parameter**
  
An example

```shell
npm install -S bootstrap
```

Here

- `npm` : is the **command prefix**
- `install` - is the **command option**
- `-S` - is the **command option flag**
- `boostrap` - is the **command argument** passed to the command parameter `<parameter>`

## How do I stop a command?

Stopping any command can be done by using the shortcut of `ctrl + c` together.

## npm start [command]

```shell
$ npm start
```

A default npm command that can run a script. The script ran is used startup the development of your application.

## npm install [command]

```shell
$ npm install
$ npm install <package-name>
$ npm install -D <package-name>
$ npm install -S <package-name>
```

All `npm install` commands will either update or create a package-lock.json file that will appear in the root of your project.

### npm install

```shell
$ npm install
```

This command is used when you install all your packages from the beginning, this means in your project there is no `./node_modules/`  directory in your project. npm install can will create a `./node_modules/`.

#### shorthand

```shell
$ npm i
```

#### Just, npm install?
Remember it is only npm install, with nothing at the end. This means no `<package-name>` and option flags like `-D` and `-S`.

Just `npm install`

#### When to use?

`npm install` is usually used after you’ve cloned a JavaScript, React or NodeJS project. To install the package dependencies you will need for your project.

The project MUST command a [package.json](#packagejson) file in its own root directory. If it doesn't contain this a package.json file, the installation of dependencies will not be possible.

#### How can I check?

You know you that running your command was successful when

1. The following message will be given. Don't be alarm if any of the numbers are not the same.

```shell
added <amount> packages from <amount> contributors and audited <amount> packages in <seconds>s
```

```shell
added 1641 packages from 773 contributors and audited 1641 packages in 26.332s
```

2. `npm install` will have created an `./node_modules/` directory in the root of your directory


#### What are packages?
Package is a directory that contains a separate JavaScript or CSS project that you will use as a **dependency**. When using `create-react-app`, to use any package, you will need to import it using the `import` syntax - ask your mentor if you have not yet come across the `import` syntax.

For more information on `packages`. Please see the official npm documentation - [About packages and modules [npm]](https://docs.npmjs.com/about-packages-and-modules)

There are 2 types, you can find in your project `dependencies` and `devDependencies`

For more information on the differences between `devDependencies` and `dependencies`. Please read this Medium article - [dependencies vs devDependencies | Artem Zekov](https://medium.com/@stalonadsl948/dependencies-vs-devdependencies-926e096a3dee)

### npm install \<package-name\>

```shell
$ npm install <package-name>
```

More examples:

```shell
$ npm install bootstrap
$ npm install prettier
```

This command installs _new_ depedencies to add to your current dependency listing - more accurately a dependency tree.

Another thing to remember, is that it will include the `latest` dependency, meaning the newest version of that dependency in your application

#### shorthand

```shell
$ npm i <package-name>
```

More examples:

Instead of 

```shell
$ npm i bootstrap
$ npm i prettier
```

You can write the dependencies you need to install one after the other.

```shell
$ npm i bootstrap prettier
```

#### When to use?

This command is used after you have installed all the dependencies. Meaning

1. First you need to install all dependencies in your [package.json](#packagejson), by doing [npm install](#npm-install)
2. After you installed all your project dependencies, you can then install _newer_ packages using the `npm install <package-name>` command.

### npm install -S \<package-name\>

```shell
$ npm install -S bootstrap
$ npm install -S react
```

#### What does the -S flag mean?
`-S` this option flag is shorthand for `--save-prod` meaning the dependency you installed will be used in production.

Production in it's simplest definition, is the final code that will part of your application, that end users will experience using. 

Production dependencies are labelled as `dependencies` in your [package.json](#packagejson). This means the code in your production dependencies for example `react` and `react-dom` will be inside your final application that is ran on a server, not locally on your computer.

#### How to use -S flags here?

`-S` this option flag is used in conjunction with part of the command `npm install`, to give `npm install -S`.

Finally you will need pass in the package name as an argument, that you intend to install.

```shell
$ npm install -S <package-name>
```

```shell
$ npm install -S bootstrap
```

#### How do I check?

Go to your **package.json** file in the root of your directory and find the key `dependencies` you should have a new dependency added.

For example;

```shell
$ npm install -S bootstrap
```

Should give a similar, not exactly the same numbers as the bootstrap example below;

```JSON
{
  "dependencies": {
    "bootstrap": "^4.4.0"
  }
}
```

#### Differences between `npm install` and `npm install -S`

There is no impactful difference between `npm install` and `npm install -S`. As both packages are shown inside the `package.json` under `dependencies` key (of the JSON).

### npm install -D \<package-name\>

```shell
$ npm i -D prettier
$ npm i -D husky 
```

#### What does the -D flag mean?
`-S` this option flag is shorthand for `--save-dev` meaning the dependency you installed will be used in development.

The word **Development** here, in it's simplest definition, is the code you will be running to help you develop your application.

Development dependencies are labelled as `devDependencies` in your [package.json](#packagejson). This means the code in your development dependencies for example `prettier` and `husky` will only be ran during development and will NOT be part of your final code in your application, that your end users will experience using.

#### How to use -D flags here?

`-D` this option flag is used in conjunction with part of the command `npm install`, to give `npm install -D`

Finally you will need pass in the package name as an argument, that you intend to install.

```shell
$ npm install -S <package-name>
```

```shell
$ npm install -S bootstrap
```

#### How do I check?

Go to your **package.json** file in the root of your directory and find the key `devDependencies` you should have a new dependency added.

For example;

```shell
$ npm install -D prettier
```

Should give a similar, not exactly the same numbers as the bootstrap example below;

```JSON
{
  "devDependencies": {
    "prettier": "^2.0.5"
  }
}
```

#### Differences between `npm install` and `npm install -D`

Both `npm install` and `npm install -S` update the `dependencies` section of the [package.json](#packagejson).

Where as `npm install -D` update update the `devDependencies` section of the [package.json](#packagejson).

## npm uninstall [command]

```shell
$ npm uninstall <package-name>
```

The command will uninstall both development and production dependencies in your [package.json](#packagejson)

```
$ npm uninstall react
$ npm uninstall prettier
```

npm website
https://www.npmjs.com/ - install different packages you might need
https://www.npmjs.com/package/npx

## package.json

Is the manifest that contains all the information about the dependencies you will need for you project.

### What is JSON?

JSON is a globally recognised file format standard, that consist of strings, numbers, object and other JavaScript types as values.

Examples

```JSON
{
  "brand": "",
  "model": "",
  "amount"
}
```

#### Basic JSON rules

JSON starts with an object or an array. Objects inside the 

## file system
Note that these commands work across all operating systems.

One of the major differences between Windows and Unix Operating systems (i.e. Mac OSX and Linux). Is the file system

## References
### npm commands
- [npm cli commands [npm]](https://docs.npmjs.com/cli-documentation/cli)

### package.json
- [About packages and modules [npm]](https://docs.npmjs.com/about-packages-and-modules)
- [dependencies vs devDependencies | Artem Zekov [Medium]](https://medium.com/@stalonadsl948/dependencies-vs-devdependencies-926e096a3dee)