# Tinymce-mathjax-formula-editor

- Must  run the file from a Local Web Server like WAMP, XAMPP, etc
- tinymce6-formula-master was modified to not convert the formula to image but leave it as LaTex because the image quality was not clear enough
- tinymce-mathjax-master helps to show the LaTex properly in the editor and also allows editing of the inserted formula by clicking on it.
- MathJax must be added to the page where the code will be viewed. Cdn was used in the demo.
- The only file used from MathJax-master folder was only used to add "tex-mml-chtml.js" to the tinymce editor "library" like below
	```javascript
	mathjax: {
		lib: "plugins/MathJax-master/es5/tex-mml-chtml.js",
	}
	```
- Remove 'mathjax' from the below code if you want to remove 'Equation' from tinymce toolbar. This is for tinymce-mathjax-master and is not needed in the tinymce toolbar.
	```javascript
	toolbar: 'formula code mathjax'
	```


## CREDIT

https://github.com/dimakorotkov/tinymce-mathjax
https://github.com/umar221b/tinymce6-formula
