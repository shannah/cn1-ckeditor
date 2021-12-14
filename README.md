# Codename One CKeditor Component

IMPORTANT: This module is no longer maintained, and it may have problems working on some Codename One platforms.  The CKeditor version is out of date also.

A WYSIWYG HTML Editor component for Codename One

![CKeditor Widget in CodenameOne Simulator](https://github.com/shannah/cn1-ckeditor/raw/master/screenshots/ckeditor-iphone4.png)

## Synopsis

The CKeditor widget wraps the Javascript [CKeditor](http://ckeditor.com/) widget inside a [BrowserComponent](https://codenameone.googlecode.com/svn/trunk/CodenameOne/javadoc/com/codename1/ui/BrowserComponent.html) and exposes
a subset of the functionality as a Java API.  It can easily be improved to add additional
functionality also, but just putting up the bare-bones necessary features right now to
get it working.


## License

[LGPL](http://www.gnu.org/licenses/lgpl.html)

## Installation Instructions (Using Netbeans)

1  Add the [CodenameOneCKeditorComponent.cnlib](https://github.com/shannah/cn1-ckeditor/blob/master/CodenameOneCKeditorComponent.cn1lib?raw=true) library to your project's lib directory.
3. Right click on your project in the netbeans project explorer, and select "Refresh Libs" (so that Netbeans will recognize your libs).

## Usage

1. Create a new CKeditor object:
    
        CKeditor editor = new CKeditor();
    
2. Initialize the editor.  You can either do this asynchronously with initLater(), or synchronously with initAndWait().  Your choice will
depend on whether you want to start interacting with it right away.

        editor.initLater();
        
        // or editor.initAndWait();
    
3. Add editor to your form.

        form.setLayout(new BorderLayout());
        form.addComponent(BorderLayout.CENTER, editor);
    
### Getting current contents:

    String content = editor.getData();
    
### Setting current contents:

    editor.setData("<p>Some HTML to set as the content</p>");
    
    // or set content as text
    editor.setText("Hello world\n This is a new line\n another new line");
        // This will be converted to appropriate HTML.
        
## To Do:

Lots of things to do.  This is basically just a quick and dirty proof of concept right now.  One of the most important things that needs to be done is to add the ability to
set [configuration options](http://docs.ckeditor.com/#!/api/CKEDITOR.config) so that you can, e.g. change the options in the toolbar.

Potentially, wrappers can be created for any [property, method, or event](http://docs.ckeditor.com/#!/api/CKEDITOR.editor) in CKeditor.

## Contact:

[@shannah78](http://www.twitter.com/shannah78)
