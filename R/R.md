- This R command lists all packages installed by the user and the package versions.
```
ip <- as.data.frame(installed.packages()[,c(1,3:4)])
rownames(ip) <- NULL
ip <- ip[is.na(ip$Priority),1:2,drop=FALSE]
print(ip, row.names=FALSE)
```
- R package book: http://r-pkgs.had.co.nz/

- read STDIN in R
  ```
  ## read file
  f<-file("stdin")
  open(f)
  on.exit(close(f))
  
  data=c()
  while(length(line<-readLines(f, n=1, warn=FALSE))>0)
        data<-c(data, line)
  #print(data)

  ## chop up the big line of data
  data=strsplit(data, " ")
  #print(data)
  ```
- Output STDOUT:
  ```
  write(result, stdout())
  ```
  
  
