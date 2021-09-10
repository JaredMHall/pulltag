pulltag
=======
Easily and quickly scrape html tags by name, id, and class. Return full tag text, id name, class name, or just src or href links. 

Dependencies
============
Python 2.7  
BeautifulSoup (to get it run this command: ```pip install BeautifulSoup```)

Installation
============
Can be added to usr/local/bin like so (for calling straight from the command line regardless of current folder):  
  ```cd /usr/local/bin``` (command below must be called from within this folder)  
  ```sudo ln -s <path_to_pulltag/pulltag>```  (add symbolic link to pulltag)  
  ```chmod +x pulltag``` (make pulltag executable)  

Examples with a website as input
================================
```pulltag doge4.us``` (minimum required argument is the name of the website, this returns the source code for said page)  
```pulltag doge4.us p``` (return all of the ```<p>``` tags in the page.. returns each tag in it's entirety)  
```pulltag doge4.us -id``` (return all tags with an id in their entirety)  
```pulltag doge4.us -id specific_tag_name``` (pull a specific tag id by name and view it in it's entirety)  
```pulltag doge4.us -id -names``` (return all tag id names ONLY)  
```pulltag doge4.us img -src``` (return img src address ONLY.. leave off the -src to view img tags in their entirety)  
```pulltag doge4.us a -href``` (you guessed it, return all the href addresses)


Examples with a pipe as input
=============================
Same as above except we leave off the website name.

```curl doge4.us | pulltag img -src```  

Help
====
```pulltag -h```  
