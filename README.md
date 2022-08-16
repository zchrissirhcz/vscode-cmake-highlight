# CMake Syntax Highlighting

This extension provides [CMake](http://www.cmake.org/) syntax highlighting for [Visual Studio Code](https://code.visualstudio.com/).

## Install
Search and install **`cmake-highlight`** in VSCode extension marketplace:

![search-and-install](images/search-and-install.png)

![screencast](images/cmake1.gif)

## Features

- Colorization
- Completion Lists 

![completion](images/cmake2.gif)

- Code comments

![comment](images/cmake3.gif)

- Snippets

![find_package](images/cmake5.gif)

![include](images/cmake6.gif)

- Quick Help

![tooltip](images/cmake4.gif)

- Access To Online Help


## Options

The following Visual Studio Code settings are available for the Cmake extension. These can be set in user preferences (cmd+,) or workspace settings (.vscode/settings.json).

```json
{
    "cmake.cmakePath": "/path/to/cmake"
}
```

## Commands

- `CMake: Online Help` to go to the CMake online documentation (according to the current cmake version). 

## Local build
```bash
git clone https://github.com/zchrissirhcz/vscode-cmake-highlight.git
cd vscode-cmake-highlight

npm install -g vsce
npm install typescript -g
npm install
...
vsce package # generate the .vsix file
```

```js
<reference lib="es2015" />
```
to
```
<reference lib="es2015" >
```

## Acknowledgements

This extension is based on [CMake For VisualStudio Code](https://github.com/twxs/vs.language.cmake).

## License

[MIT](LICENSE)
