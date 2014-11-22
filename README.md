smartStart
==========

This is an application that should be placed in the startup of the system. Configure this application by going to config.properties to suit your need. It will help you set up a list of programs that should be started depending on whether it is office time or home time (or neither [only applicable during holidays]). 


Sample Configuration file(config.properties)

#<code>allTimePrograms</code> are always started regardless of the time the program is started.
allTimePrograms =skype,gedit

#<code>officeTimePrograms</code> are started if it is not holiday and lies between <code>officeStartTime</code> and <code>officeEndTime</code>.
officeTimePrograms =google-chrome

#<code>homeTimePrograms</code> are started if time lies between <code>homeStartTime</code> and <code>homeEndTime</code>. These programs are also started if <code>stayHomeDuringHolidays</code> is true and starting time is holiday
homeTimePrograms =nautilus

#office first hour
officeStartTime =10:00

#office last hour
officeEndTime =18:00


#home start hour
homeStartTime =18:00

#home end hour
homeEndTime =10:00


#<code>holidays</code>. These are the days during which you do not go to office(It doesn't mean that you will stay in home however.
# Set <code>stayHomeDuringHolidays</code> to true/false whichever preferred
holidays =SATURDAY,SUNDAY

#not staying home during holidays means neither in home nor in office.
#If it is true <code>homeTimePrograms<code> are started during <code>holidays</code> regardless of the time  but only <code>allTimePrograms</code> are started if it is false
stayHomeDuringHolidays=true


