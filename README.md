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

6. Print things with names in order

for(i in 1:3){
  assign( paste("country", i, sep=""), 10) #countryi = 10
  print(i)
  print( get( paste("country", i, sep="") ) ) #print(countryi)
}

####################

country1 = list(P=10, data=c(1,2,3,4))

country2 = list(P=09, data=c(1,2,3,1000))


sum(country1$data)

for(i in 1:2){
   print ( sum( get( paste("country", i, sep="") )$data ) )
}

6. Time data: Create a sequence of time by days, years, quarters...

seq(as.Date("2020/01/22"),as.Date("2020/06/30"),"days")

7. Make a seuquence of last 10 days up to 04/30/2020

rev(seq(as.Date("2020-04-30"), length =  10, by = "-1 day"))

8. download .Rdata and check which variables available in *.Rdata

load("file1.Rdata")
ls()

9. Ifelse nested

for(i in 1:inp$duration)
{
if (i<inp$changepoint[1]){
  print(paste("This 1"))
} else if (inp$changepoint[1]<= i & i< inp$changepoint[2]) {
  print(paste("This 2"))
  } else if (inp$changepoint[2]<= i & i<inp$changepoint[3]) {
  print(paste("This 3"))
} else if (inp$changepoint[3]<= i & i<inp$changepoint[4]) {
  print(paste("This 4"))
} else {
  print(paste("This 5"))
}
}

10. Check the status of main packages of our current Rversion
     
     Info.System()


