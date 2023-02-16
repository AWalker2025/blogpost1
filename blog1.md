# Autumn's Blog Post

Sick of wasting your time creating a new project file that contains basic styles everytime you want to start a new project? 

While I argued with Eric that it wasn't faster, I guess I will admit I was wrong - but *only* this one time and **no one** is allowed to tell anyone.

So for this blog post assingment, I created a shell script file that when it is selected, will open and run the basic  folders and files I created including a **js**, **css**, **norm.css**, and **read.me** file and an **img** folder that contain basic styles. 

For starters, in my script.sh, I created a new folder on my desktop called new-project, and inside of that folder I created directories including css, js, img, as such:

```bash
#!/bin/bash
# scaffolds my project
mkdir new-project
cd new-project
touch index.html
mkdir css js img
``` 

Next, in those folders, I created the files:

```bash
touch css/style.css
touch css/norm.css
touch js/page.js
touch readme.md
```

Then I wrote some general code within my HTML file including a link to my stylesheets, a header with sample text, paragraph tags, and a footer:

```bash
echo "<!DOCTYPE html>" >> index.html
echo "<html lang=\"en\">" >> index.html
echo "<head>" >> index.html
    echo "<meta charset=\"utf-8\">" >> index.html
    echo "<meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">" >> index.html
    echo "<link rel=\"stylesheet\" href=\"css/norm.css\">" >> index.html
    echo "<link rel=\"stylesheet\" href=\"css/style.css\">" >> index.html
    echo "<script src=\"js/page.js\" defer ></script>" >> index.html
    echo "<title>Document</title>" >>index.html
echo "</head>" >> index.html
echo "<body>" >> index.html
    echo "<h1> This is my sample text</h1>" >> index.html
echo "<footer>" >>index.html
    echo " <p>&copy; 2023 Autumn Walker</p>" >> index.html
echo "</footer>" >> index.html
echo "</body>" >> index.html
echo "</html>" >> index.html
```
After this, I added my modern normalize reset which I found from by clicking on this link (https://github.com/sindresorhus/modern-normalize), and then *Minified* at the bottom of the page or by following this link (https://cdn.jsdelivr.net/npm/modern-normalize/modern-normalize.min.css): 
```bash
echo "/**
 * Minified by jsDelivr using clean-css v4.2.3.
 * Original file: /npm/modern-normalize@1.1.0/modern-normalize.css
 *
 * Do NOT use SRI with dynamically generated files! More information: https://www.jsdelivr.com/using-sri-with-dynamic-files
 */
/*! modern-normalize v1.1.0 | MIT License | https://github.com/sindresorhus/modern-normalize */
*,::after,::before{box-sizing:border-box}html{-moz-tab-size:4;tab-size:4}html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0}body{font-family:system-ui,-apple-system,'Segoe UI',Roboto,Helvetica,Arial,sans-serif,'Apple Color Emoji','Segoe UI Emoji'}hr{height:0;color:inherit}abbr[title]{text-decoration:underline dotted}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace,SFMono-Regular,Consolas,'Liberation Mono',Menlo,monospace;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit}button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;line-height:1.15;margin:0}button,select{text-transform:none}[type=button],[type=reset],[type=submit],button{-webkit-appearance:button}::-moz-focus-inner{border-style:none;padding:0}:-moz-focusring{outline:1px dotted ButtonText}:-moz-ui-invalid{box-shadow:none}legend{padding:0}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}
/*# sourceMappingURL=/sm/b8ae781793ee4eb86edef3f2a2ac43a5575d063ed8cd287d7553f9f1b2776616.map */" >> css/norm.css
```
Then I styled my header and footer text in my style.css file:

```bash
echo "h1 {text-align: center;} footer {
    display: block;
    text-align: center;
    margin: auto;
    bottom: 0;
    position: absolute;
    width: 100%;
}" >> css/style.css
```

Lastly, I told my script.sh file to open my index.html up in a browser upon opening:

```bash
open index.html
```

All in all, creating this basic shell script will save time when creating a new project and includes basic styling needed to help you get started. 



Below is my entire script.sh file for reference:

## Full script.sh File
```bash
#!/bin/bash
# scaffolds my project
mkdir new-project
cd new-project
touch index.html
mkdir css js img 
touch css/style.css
touch css/norm.css
touch js/page.js
touch readme.md
echo "<!DOCTYPE html>" >> index.html
echo "<html lang=\"en\">" >> index.html
echo "<head>" >> index.html
    echo "<meta charset=\"utf-8\">" >> index.html
    echo "<meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">" >> index.html
    echo "<link rel=\"stylesheet\" href=\"css/norm.css\">" >> index.html
    echo "<link rel=\"stylesheet\" href=\"css/style.css\">" >> index.html
    echo "<script src=\"js/page.js\" defer ></script>" >> index.html
    echo "<title>Document</title>" >>index.html
echo "</head>" >> index.html
echo "<body>" >> index.html
    echo "<h1> This is my sample text</h1>" >> index.html
echo "<footer>" >>index.html
    echo " <p>&copy; 2023 Autumn Walker</p>" >> index.html
echo "</footer>" >> index.html
echo "</body>" >> index.html
echo "</html>" >> index.html
echo "/**
 * Minified by jsDelivr using clean-css v4.2.3.
 * Original file: /npm/modern-normalize@1.1.0/modern-normalize.css
 *
 * Do NOT use SRI with dynamically generated files! More information: https://www.jsdelivr.com/using-sri-with-dynamic-files
 */
/*! modern-normalize v1.1.0 | MIT License | https://github.com/sindresorhus/modern-normalize */
*,::after,::before{box-sizing:border-box}html{-moz-tab-size:4;tab-size:4}html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0}body{font-family:system-ui,-apple-system,'Segoe UI',Roboto,Helvetica,Arial,sans-serif,'Apple Color Emoji','Segoe UI Emoji'}hr{height:0;color:inherit}abbr[title]{text-decoration:underline dotted}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace,SFMono-Regular,Consolas,'Liberation Mono',Menlo,monospace;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit}button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;line-height:1.15;margin:0}button,select{text-transform:none}[type=button],[type=reset],[type=submit],button{-webkit-appearance:button}::-moz-focus-inner{border-style:none;padding:0}:-moz-focusring{outline:1px dotted ButtonText}:-moz-ui-invalid{box-shadow:none}legend{padding:0}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}
/*# sourceMappingURL=/sm/b8ae781793ee4eb86edef3f2a2ac43a5575d063ed8cd287d7553f9f1b2776616.map */" >> css/norm.css
echo "h1 {text-align: center;} footer {
    display: block;
    text-align: center;
    margin: auto;
    bottom: 0;
    position: absolute;
    width: 100%;
}" >> css/style.css
open index.html
```