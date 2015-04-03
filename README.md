![](drop.png) 

# rDrop2 - Dropbox interface from R



This package provides programmatic access to Dropbox from R. The package provides a full suite of file operations, including directory listing, copy/move/delete operations, account information and the ability to upload and download files from any Dropbox account. 


__Installation__  

```r
devtools::install_github('karthik/rDrop2')
```

__Basic Usage__


```r
library(rDrop2)
drop_auth()
# This will launch your browser and request access to your Dropbox account. Once completed, close your browser window and return to R to complete authentication.
```

__Directory listing__


