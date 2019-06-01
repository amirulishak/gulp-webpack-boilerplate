**Gulp Webpack Boilerplate** 

<br/>
<br/>

![header](../assets/header.png?raw=true)

<br/>
<br/>

## :tada: Overview
<br/>

A modern JavaScript starter toolkit for web-development using Gulp task runner and Webpack bundler. 
  
Ideal for fast building static HTML sites or templates. It speeds up the proccess of delevelopment, 
testing and deploy in a front-end project. Also it can be extended in a simple way when project 
require some extra functionality provided by thirdparty packages.
  
All the tasks are done via Gulp. Webpack is just used for Javascript (especially for ES6 
Import/Export as Gulp can't do it in a proper way) and not for rest because it's a little bit 
overhed to translate all static assets and styles through js using Webpack.

<br />
<br />
<br />

## :link: Demo of projects using this boilerplate 
<br/>

- [Supreme site repo](https://github.com/noth8/supreme-site)
- [Downhill site repo](https://github.com/noth8/downhill-site)
- [Maxgold site repo](https://github.com/noth8/maxgold-site)

<br />
<br />
<br />

## :wrench: Features
<br/>

| Feature         | Description                                                                                                                                                                          |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Javascript      | Full support of javascript latest features using Babel loader and Webpack. Also, there is a lot of code optimization while building in production mode.                              |
| HTML            | Pug templates provide an opportunity to make a better structure and code readability and then compiling it to HTML.                                                                  |
| Styles          | Stylus support with compiling to css and doing minification with concatenation.                                                                                                      |
| Autoprefixier   | Parse CSS and add vendor prefixes(-wbkit, -moz, -o, -ms) to rules in production build.                                                                                               |
| Sourcemaps      | Css and js source maps in development mode.                                                                                                                                          |
| Bootstrap       | You can specify what part of Bootstrap do you need and then compile it to get the low size files.                                                                                    |
| Live Reload     | Automatic reloading of the browser on code modification and cross-platform syncing of all actions between connected devices. This depends on Gulp-watch, Webpack-watch, BrowserSync. |
| Google Fonts    | Auto-downloads Google fonts specified in fonts list then generates css with them and finally moves them to the build dir.                                                            |
| Images          | Compressing images to desired quality and size through Mozjpeg or Guetzli.                                                                                                           |
| Hashed names    | File names contain smart hashes in production mode. Hash will change on file modifications. This helps to avoid browser long term caching.                                           |
| Code linting    | Eslint checks js code according to AirBnb rules and notify if something wrong.                                                                                                       |
| Code formatting | Prettier auto-formats js code that doesn't satisfy Eslint styles rules.                                                                                                              |
| Cached files    | Gulp tasks configured to process only new files in development mode.                                                                                                                 |
| Error notifier  | You get a desktop notification when errors occur.                                                                                                                                    |

<br />
<br />
<br />

## :department_store: Project Structure
<br/>

```
├── dist/                          # Static version of the website
│   ├── css/                       # Folder for concatenated css file
│   ├── fonts/                     # All fonts files
│   ├── img/                       # Images
│   ├── js/                        # Folder for bundle js file
│   └── index.html                 # Can be any page and more than one
├── src/                           # Source files
│   ├── fonts/                     # Fonts
│   │   └── fonts.list             # Google Fonts config
│   ├── img/                       # Site images
│   ├── js/                        # Javascript files
│   │   ├── bootstrap.js           # Uncomment module that you need
│   │   ├── entry.js               # Webpack entry point
│   │   └── main.js                # All user scripts
│   ├── styles/                    # Styles
│   │   ├── bootstrap/             # Bootstrap sass config
│   │   │   ├── bootstrap.scss     # Uncomment module that you need
│   │   │   └── _variables.scss    # Change what you want
│   │   └── main.styl              # Main stylesheet file
│   ├── templates/                 # Site templates (Pug)
│   │   ├── pages/                 # Pug only looks for this dir
│   │   │   └── index.pug          # You can create any amount of pages in this dir
│   │   ├── navigation.pug         # Site navigation
│   │   ├── header.pug             # Site header
│   │   ├── footer.pug             # Site footer
│   │   └── layout.pug             # Main layout
│   └── vendor/                    # Appears if CUSTOM_SOURCE options specified or fonts enabled.
│       ├── bootstrap/             # Change source files to whatever you want
│       └── googleFonts/           # Storage for downloaded fonts
├── temp/                          # Temporary folder
│   └── manifest/                  # Manifests for the production build
│       └── rev-images.json        # Hashed images names
├── .babelrc                       # Babel presets for latest js features
├── .eslintrc.js                   # ESLint config
├── .gitignore                     # List of files ignored by git
├── .prettierrc                    # Prettier formatter config
├── gulpfile.babel.js              # Gulpfile config and tasks
├── license                        # Project license
├── package.json                   # Node.js dependencies and scripts
└── readme.md                      # Description of the project
```
