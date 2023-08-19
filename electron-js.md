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

<h5>
    Setting up the project
</h5>
<br>

<blockquote>
    <p>
        <strong>
            ⚠️ AVOID WSL ⚠️
        </strong>
    </p>
    <p>
        If you are on a Windows machine, please do not use Windows Subsystem for Linux (WSL) when following this tutorial as you will run into issues when trying to execute the application.
    </p>
</blockquote>

<h5>
    Initializing the project
</h5>

Electron apps are scaffolded using `npm`, with the `package.json` file as an entry point. Start by creating a folder and initializing an npm package within it with `npm init`.