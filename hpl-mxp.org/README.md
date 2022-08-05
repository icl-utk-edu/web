# NewtonCMS - a lightweight CMS for mostly static content

This is not a sophisticated content management system, but it is sufficient in scale for many websites.  It is very easy to deploy and modify as needed.  

## Installation

Copy the files "doc" and "tmpl.html" into the document root of the website and set the permissions to allow the webserver to read and execute the files as required.  
The "htaccess" file is provided file as an example of how to configure the Apache web server to execute the "doc" script as a CGI.

Copy the directory "docs" and all contents into the document root.  This directory will eventually contain all the static web pages for the site.  
Web page files under this directory should end in the ".md" extension (for "Markdown" format).

Use a web browser to visit the test page http://domain.com/doc/test . 
This corresponds to the markdown source file "test.md" in the "docs" directory.
If you see a minimally formatted test page, then you have completed initial installations.

## Theory of operation

When a web page is request (e.g., /doc/test), the following the accomplished:

   * the CGI script "doc" is executed
   * the script reads in a file "test.md" under the "docs" directory
   * the file is parsed for MarkDown syntax and converted to an HTML snipit
   * the script reads the file "tmpl.html"
   * HTML from "test.md" is inserted into the content of "tmpl.html" in place of "CONTENT"
   * the title of the web page is parsed from the "H1" HTML tag and inserted in place of "TITLE"
   * the document is returned to the requesting web browser

## Customization

   * You may create new files with the "md" extensions under the "docs" directory. 
   * You may create new subdirectories under "docs".
   * You may customize the template file "tmpl.html" as needed.
   * You may reference other resource files like javascript, css, and images from the main template
   * You may use the "tmpl.html" file to template other CGI script to unify the website appearance across different scripts and content management systems
   
   
   
