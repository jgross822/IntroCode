### CHARTS FOR 2017 SHORTWAVE RADIATION IN UPWARDS AND DOWNWARDS FACING
##as.vector(netR$doy)
setwd("~/Documents/Loranty Lab Code/2019/Data")
netR <- read.csv("netR.csv")
as.vector(netR$doy)

##SUBSETTING
#ss1 = SRUp, high density, 100
#ss2 = SRUp, high density, 800
#ss3 = SRUp, low density, 100
#ss4 = SRUp, low density, 800
ss1 <-subset(netR,sensorZ==100&year==2017&site=="hd")
ss2 <-subset(netR,sensorZ==800&year==2017&site=="hd")
ss3 <-subset(netR,sensorZ==100&year==2017&site=="ld")
ss4 <-subset(netR,sensorZ==800&year==2017&site=="ld")

ss1
ss2
ss3
ss4

##AGGREGATING
#shortwave first and then day
agg1<-aggregate(SRUp~doy,ss1,mean)
agg2<-aggregate(SRUp~doy,ss2,mean)
agg3<-aggregate(SRUp~doy,ss3,mean)
agg4<-aggregate(SRUp~doy,ss4,mean)

agg1
agg2
agg3
agg4

#PLOTTING
plot(agg1,type="l",main="Upwards Facing Shortwave Radiation in 2017",
     xlab="doy (day of year)",
     ylab="SRUp (w/m^2)",
     cex.axis=0.6,
     xlim=c(88,230),
     ylim=c(0,600),
     col="red")
lines(agg2,type="l",col="pink")
lines(agg3,type="l",col="blue")
lines(agg4,type="l",col="lightblue") 
legend(88,600,
       legend=c("High Density, 1m","High Density, 8m", "Low Density, 1m","Low Density, 8m"),
       col=c("red","pink","blue","light blue"), 
       lty=1:2,
       cex=0.8,
       title="Site",
       text.font=2)

##Key
#Red= SRUp, high density at 100
#Pink= SRUp, high density at 800
#Blue= SRUp, low density at 100
#Light Blue= SRUp, low density at 800

#######################################
##REPEATING ALL WITH DOWNWARDS FACING##
#######################################
#ss5 = SRDn, high density, 100
#ss6 = SRDn, high density, 800
#ss7 = SRDn, low density, 100
#ss8 = SRDn, low density, 800
ss5 <-subset(netR,sensorZ==100&year==2017&site=="hd")
ss6 <-subset(netR,sensorZ==800&year==2017&site=="hd")
ss7 <-subset(netR,sensorZ==100&year==2017&site=="ld")
ss8 <-subset(netR,sensorZ==800&year==2017&site=="ld")

ss5
ss6
ss7
ss8

##AGGREGATING
#shortwave first and then day
agg5<-aggregate(SRDn~doy,ss5,mean)
agg6<-aggregate(SRDn~doy,ss6,mean)
agg7<-aggregate(SRDn~doy,ss7,mean)
agg8<-aggregate(SRDn~doy,ss8,mean)

agg5
agg6
agg7
agg8

#PLOTTING
plot(agg5,type="l",main="Downwards Facing Shortwave Radiation in 2017",
     xlab="doy (day of year)",
     ylab="SRDn (w/m^2)",
     cex.axis=0.6,
     xlim=c(88,230),
     ylim=c(0,250),
     col="black")
lines(agg6,type="l",col="grey")
lines(agg7,type="l",col="dark green")
lines(agg8,type="l",col="light green")
legend(180,250,legend=c("High Density, 1m","High Density, 8m", 
                        "Low Density, 1m","Low Density, 8m"),
       col=c("black","grey","dark green","light green"),
       lty=1:2,
       cex=0.8,
       title="Site",
       text.font=2)

##Key
#Black= SRDn, high density at 100
#Grey= SRDn, high density at 800
#Green= SRDn, low density at 100
#Light Green= SRDn, low density at 800

