# Reach App Structure

### Set up instructions

#### Prerequisites
- Node
- Ruby
- Compass
- Bower

#### Install
- Run **npm install** and **bower install** in the project root directory
  - This will install GulpJS and Bower dependencies

#### Folder Structure
The source folder contains source files that have not been run through gulp tasks yet.

```
_html
-> _css
-> _js
_source
-> css
-> js
-> sass
```
#### GulpJS
- SASS & CSS
	- sass-dev: compile css and send it to **_source/css** and **_html/_css**
	- sass-prod: compiles and compresses css files and sends it to  **_source/css** and **_html/_css**

- JAVASCRIPT
	- js-vendors: copies vendor files to **_html/_js/_vendors**
	- js-dev: concatenates js files into **app.min.js** and sends it to **_html/_js**
	- js-prod: concatenates js files, and compresses them into **app.min.js** and sends it to **_html/_js**

- IMAGES
	- imagemin: minifies all images in the **_source/assets** directory and subdirectories and sends it to **_html/_assets/**

- FONTS
	- fonts: copies fonts in the **_source/assets/fonts** directory and copies them to **_html/_assets/fonts**
