# Rtips
Rtip
1. Save Rdata file in R the variable want to say and the file name should match.

2. Print string vector in 1 line

 print(paste(c("Hello",outj),collapse="\t"))


3. Remove and install from git

remove.packages("CONETTravel")

library(devtools)

install_github("leminhthien2011/CONETTravel", dependencies=TRUE)

library(CONETTravel)

4. Search all objects in a package

lsf.str("package:CONETTravel") #This gives all function and argument

ls("package:CONETTravel") # This gives all names only

help(package = "CONETTravel") # This gives a complete picture

5. loop of list
countries = list()
countries[[1]] = country1
countries[[2]] = country2
countries[[3]] = country3
for (i in 1:length(countries)){
  tmp = countries[[i]]
  pop = popfunc(tmp)
  countries[[i]] = list.append(countries[[i]], pop = pop)
}


