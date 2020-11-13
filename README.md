# dropdownshowhide

This Repo contains a basic example of a conditional Dropdown within AEM page properties.  
The example was tested on a bare AEM 6.4 instance and should underline, that the dropdown is not working in page properties.

It seems that the dropdownshowhide.js is triggering on foundation-contentloaded event. Sadly, at this point the input field of the dropdown is still not being set.
Based on this empty value, the dropdownshowhide.js will trigger a wrong line of code.
