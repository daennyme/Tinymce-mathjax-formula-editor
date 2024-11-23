# Tinymce-mathjax-formula-editor

- Extract the `plugins.zip` to the same directory as `index.html`. It contains `tinymce`, `mathjax`, modified `tinymce6-formula-master` and `tinymce-mathjax-master`
- The file must be run from a local web server such as WAMP, XAMPP, or similar.  
- The `tinymce6-formula-master` plugin has been modified to retain formulas in LaTeX format instead of converting them to images due to concerns about image quality.  
- The `tinymce-mathjax-master` plugin ensures proper rendering of LaTeX in the editor and enables editing of inserted formulas by clicking on them.  
- MathJax must be included on the page where the content will be displayed. In the demo, a CDN was used for this purpose.  
- From the `MathJax-master` folder, only the file `tex-mml-chtml.js` is utilized. This file is added to the TinyMCE editor's "library" configuration as shown below:  
	```javascript
	mathjax: {
		lib: "plugins/MathJax-master/es5/tex-mml-chtml.js",
	}
	```
- Remove `mathjax` from the code below to exclude the `Equation` option from the TinyMCE toolbar. Note that this feature is part of the `tinymce-mathjax-master` plugin and removing it will not stop the plugin from working
	```javascript
	toolbar: 'formula code mathjax'
	```


## CREDIT

- https://github.com/dimakorotkov/tinymce-mathjax
- https://github.com/umar221b/tinymce6-formula
