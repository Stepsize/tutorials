# Overview

[Electron](http://electron.atom.io) is a cross platform framework built by GitHub (based on the shell used for GitHubs hackable editor [Atom](https://atom.io)). It allows you to create applications with pure JavaScript by providing a runtime with native APIs.

Electron uses web pages as it's GUI, since its built on top of the minimal [Chromium](https://www.chromium.org/Home) browser.

# Basics

Once you start up an application using Electron, there will be a `package.json` that is read, this `package.json` will define a `main` file (typically called `main.js`), this script is called the **main process**.  

### [Main Process](http://electron.atom.io/docs/latest/tutorial/quick-start/#main-process) - The link to the native GUI of your OS
The *main process* is responsible for interacting with the native GUI of your OS and creates all of your application windows (web pages).

### [Renderer Process](http://electron.atom.io/docs/latest/tutorial/quick-start/#renderer-process) - The windows of your application
Each application window spawned by the main process will have its own individual process we call this the *renderer process*.

<img src="https://cdn-images-1.medium.com/max/800/1*EJETq7XOPz5RVY5IfF6NIg@2x.png" style="width: 300px;"/>

### [BrowserWindow](http://electron.atom.io/docs/v0.37.7/api/browser-window/) - The module to create application windows
The *BrowserWindow* is used to create all application windows within the main process. The renderer process will then take the usual HTML, CSS and JS files and render it in the window.

Note: The web pages are rendered with Chromium.

### [Electron App Structure](http://electron.atom.io/docs/v0.37.7/tutorial/quick-start/#write-your-first-electron-app)
`your-app/`
`&nbsp;&nbsp;├── package.json`
`&nbsp;&nbsp;├── main.js`
`&nbsp;&nbsp;└── index.html`

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Basic package.json example](http://gist.github.com/3d7efcd4ded630718e7514f80cb09eeb)
- [main.js example](http://gist.github.com/4cd160ec48fdcd28b1af74f7c987bdf5)
- [index.html example](http://gist.github.com/879387356072e51dffb37075bdd3ed7a)

### [Starting Electron App Template](https://github.com/electron/electron-quick-start)
To download a template electron app, in the terminal run the following
- Clone the Quick Start repository `git clone https://github.com/electron/electron-quick-start`
- Go into the repository `cd electron-quick-start`
- Install the dependencies and run `npm install && npm start`

### Communication between the main process and renderer process
The [ipcMain](http://electron.atom.io/docs/v0.37.7/api/ipc-main) and [ipcRenderer](http://electron.atom.io/docs/v0.37.7/api/ipc-renderer) are used for communication between the processes, we will run through some examples below.

#### main -> renderer
[webContents.send](http://electron.atom.io/docs/v0.37.7/api/web-contents/#webcontentssendchannel-arg1-arg2-) can be used to send an asynchronous message from the main process to the renderer process via a `channel`, you can also send arbitrary arguments.

The renderer process will need to be setup to receive these messages on the other end, this can be done using [ipcRenderer.on](http://electron.atom.io/docs/v0.37.7/api/ipc-renderer/#ipcrendereronchannel-listener) which listens on specific channels the message will be sent down.

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Main process sending a message to the renderer process](http://gist.github.com/fd7738d9d5e0e1c9cf414687ebdd1bce) - search for `electron webcontents send`
- [HTML used by the renderer process to receive messages]() - search for `electron ipcrenderer on`

#### renderer -> main
[ipcRenderer.send](http://electron.atom.io/docs/v0.37.7/api/ipc-renderer/#ipcrenderersendchannel-arg1-arg2-) can be used to send an asynchronous message  from the renderer process to the main process via a `channel`, you can also send arbitrary arguments.

The main process then handles this by listening to a specific channel using [ipcMain.on](http://electron.atom.io/docs/v0.37.7/api/ipc-main/#ipcmainonchannel-listener).

The relevant code snippet which can be retrieved via the [Stepsize](http://stepsize.com/?ref=hacksussex) app is:
- [Renderer process sending a message to the main process](http://gist.github.com/e526ac4b2c7f092200a22dbdf0cd8ca2) - search for `electron ipcrender send`
- [Main processes receiving the message from the renderer](http://gist.github.com/3deea7d0357ea1c419ab6fefc2347b3c) - search for `electron ipcmain on`

# Resources
[Documentation](http://electron.atom.io/docs/v0.37.7/) - Latest documentation as of 22.04.16

[Quick Start](http://electron.atom.io/docs/latest/tutorial/quick-start/) - Official documentation guide

[Building a desktop application with Electron](https://medium.com/developers-writing/building-a-desktop-application-with-electron-204203eeb658#.8i5jtae3w)
