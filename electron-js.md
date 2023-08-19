# 📝 ElectronJS Notes 📝

`Official Documentation:` 
<a href="https://www.electronjs.org/docs/latest/">
    ElectronJS Docs
</a>
<br>

`First Application Tutorial:`
<a href="https://www.electronjs.org/docs/latest/tutorial/tutorial-prerequisites">
    Build your first Electron App
</a>

## 📢 Introduction 📢

<details>
    <summary>
        What is ElectronJS and what is it used for?
    </summary>
    <br>
    <blockquote>
        <p>
            <strong>ElectronJS</strong>, often referred to simply as Electron, is an open-source framework for building <strong>cross-platform desktop applications</strong> using web technologies such as HTML, CSS, and JavaScript. It was initially developed by GitHub and has since gained widespread popularity in the software development community. Electron allows developers to create desktop applications for Windows, macOS, and Linux without having to learn platform-specific programming languages or frameworks.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Common examples of applications built with Electron
    </summary>
    <br>
    <blockquote>
        <p>
            Common examples of desktop applications built with Electron include code editors like Visual Studio Code, communication apps like Slack, and streaming platforms like Spotify.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Running Examples with Electron Fiddle
    </summary>
    <br>
    <blockquote>
        <p>
            <a href="https://www.electronjs.org/fiddle">Electron Fiddle</a> is a sandbox app written with Electron and supported by Electron's maintainers. It is highly recommended installing it as a learning tool to experiment with Electron's APIs or to prototype features during development.
        </p>
        <p>
            Fiddle also integrates nicely with electron's documentation. When browsing through examples in electron's tutorials, you'll frequently see an "Open in Electron Fiddle" button underneath a code block. If you have Fiddle installed, this button will open a fiddle.electronjs.org link that will automatically load the example into Fiddle, no copy-pasting required.
        </p>
    </blockquote>
</details>

## 🌱 Getting Started 🌱

### 💻 Building a test application 💻

<details>
    <summary>
        What you will need to begin with
    </summary>
    <br>
    <blockquote>
        <p>
            First, navigate to the <a href="https://www.electronjs.org/docs/latest/tutorial/tutorial-prerequisites">Prerequisites</a> page, to see what you will need to install on your machine in order to begin with using ElectronJS.
        </p>
        <p>
            The most important prerequisites to have are:
        </p>
        <ul>
            <li>
                Github
            </li>
            <li>
                (Optional) Visual Studio Code
            </li>
            <li>
                (Optional) Github Desktop
            </li>
            <li>
                NodeJS and NPM/NPX/NVM Installed
            </li>
        </ul>
        <blockquote>
            <p>
                <strong>
                    ⚠️ CAUTION ⚠️
                </strong>
            </p>
            <p>
                Although you need Node.js installed locally to scaffold an Electron project, Electron does not use your system's Node.js installation to run its code. Instead, it comes bundled with its own Node.js runtime. This means that your end users do not need to install Node.js themselves as a prerequisite to running your app.
            </p>
            <p>
                To check which version of Node.js is running in your app, you can access the global process.versions variable in the main process or preload script. You can also reference https://releases.electronjs.org/releases.json.
            </p>
        </blockquote>
    </blockquote>
</details>

<h4>
    Setting up the project
</h4>
<br>

<blockquote>
    <p>
        <strong>
            ⚠️ AVOID WSL ⚠️
        </strong>
    </p>
    <p>
        If you are on a <strong>Windows</strong> machine, please <strong>do not</strong> use <strong>Windows Subsystem for Linux (WSL)</strong> when following this tutorial as you will run into issues when trying to execute the application.
    </p>
</blockquote>
<br>

<h4>
    Initializing the project
</h4>

Electron apps are scaffolded using `npm`, with the `package.json` file as an entry point. Start by creating a folder and initializing an npm package within it with `npm init`.

<strong>
    npm
</strong>
<br>

```bash
    mkdir my-electron-app && cd my-electron-app
    npm init
```

<strong>
    Yarn
</strong>
<br>

```bash
    mkdir my-electron-app && cd my-electron-app
    yarn init
```

This command will prompt you to configure some fields in your `package.json`. There are a few rules to follow for the purposes of this tutorial:

<ul>
    <li>
        entry point should be <strong>main.js</strong> (you will be creating that file soon).
    </li>
    <li>
        author, license, and description can be any value, but will be necessary for packaging later on.
    </li>
</ul>

Then, install Electron into your app's **devDependencies**, which is the list of external **development-only** package dependencies **not required in production**.
<br>

<strong>
    npm
</strong>
<br>

```bash
    npm install electron --save-dev
```

<strong>
    Yarn
</strong>
<br>

```bash
    yarn add electron --dev
```

Your `package.json` file should look something like this after initializing your package and installing **Electron**. You should also now have a node_modules folder containing the `Electron executable`, as well as a `package-lock.json` lockfile that specifies the exact dependency versions to install.

`package.json`
<br>

```json
    {
        "name": "my-electron-app",
        "version": "1.0.0",
        "description": "Hello World!",
        "main": "main.js",
        "scripts": {
            "test": "echo \"Error: no test specified\" && exit 1"
        },
        "author": "Jane Doe",
        "license": "MIT",
        "devDependencies": {
            "electron": "23.1.3"
        }
    }
```
<br>    

<h4>
    Adding a .gitignore file
</h4>

The `.gitignore` file specifies which files and directories to avoid tracking with **Git**. You should place a copy of <a href="https://github.com/github/gitignore/blob/main/Node.gitignore">GitHub's Node.js gitignore template</a> into your project's root folder to avoid committing your project's `node_modules` folder.
<br>

<h4>
    Running an Electron App
</h4>

The `main` script you defined in `package.json` is the entry point of any Electron application. This script controls the main process, which runs in a `Node.js` environment and is responsible for **controlling your app's lifecycle**, **displaying native interfaces**, **performing privileged operations**, and **managing renderer processes**.

Before creating your first Electron app, you will first use a trivial script to ensure your main process entry point is configured correctly. Create a `main.js` file in the `root` folder of your project with a single line of code:

`main.js`
<br>

```javascript
    console.log('Hello from Electron 👋')
```