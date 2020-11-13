# dropdownshowhide

This Repo contains a basic example of a conditional Dropdown within AEM page properties.  
The example was tested on a bare AEM 6.4 instance and should underline, that the dropdown is not working in page properties.

It seems that the dropdownshowhide.js is triggering on foundation-contentloaded event. Sadly, at this point the input field of the dropdown is still not being set.
Based on this empty value, the dropdownshowhide.js will trigger a wrong line of code.

To reproduce:
- install dropdownshowhide_not_working.zip into your AEM instance
- open the "Not Working foundation-contentloaded" Page
- go to page properties
- switch to the "Not working" Tab
- You will see one dropdown (should be another pathfield)
- in the console you will see this error:

dropdownshowhide.js:58 Uncaught TypeError: component.getValue is not a function
    at showHide (dropdownshowhide.js:58)
    at dropdownshowhide.js:33
    at coralui2.js:35278
