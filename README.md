[![Travis-CI Build Status](https://travis-ci.org/karthik/rDrop2.png?branch=master)](https://travis-ci.org/karthik/rDrop2)  


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
# This will launch your browser and request access to your Dropbox account. 
# Once completed, close your browser window and return to R to complete authentication.
```

__Directory listing__


```r
library(dplyr)
acc_info() %>% 
    select(uid, name_details.given_name)
```

```
#>       uid name_details.given_name
#> 1 2223411                 Karthik
```

Retrieve only pngs


```r
drop_dir() %>% 
    .$contents %>% 
    filter(mime_type == "image/png")
```

