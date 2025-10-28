# docker file mai set of instructions hote hai 
# jinki help se hamara application chalta hai 

# Docker images ke andar code , libraries ,
# jo OS use karna hai , jo repo,tools,package use
# karna hai voh hona chahiye 

# these Images is like a box and this is made with the help 
# of docker file : instructions to make an image and when 
# we run this it becomes a container

#SINCE WE ARE RUNNING JAVA AAP WE NEED AN ENV WHERE JAVA IS INSTALLED , FOR THAT WE WILL USE BASE IMAGE
# we need an env where java is installed TO RUN IT 
# imageName : imageVersion :Java is installed here
#pull a base image having all tools and libraries
FROM openjdk:17-jdk-alpine

#MAKE a folder into container where application code is present 
# Host jaha source code rakha hua hai 
#container : jaha code execute ho raha hai 
#container mai ek aisa folder jaha code rakha hua hai 
#create folder where app code is stored
WORKDIR /app

#copy everything present in source to working directory  of container
#copy the source code from host machine to the container
COPY src/Main.java  /app/Main.java

#Agar koi command chalani hoti hai then use run command
#java ke code ko compile karo 
#app > src > Main.java ko run karo 
#compile the appliation code
RUN javac Main.java

#run the application
CMD ["java","Main"]


# cmd vs all other lines : All other lines are used to create the container 
# whereas cmd use hoga when our container is made and then executed 
#agar cmd likhe ge then still container is made but agar CMD IS in the last then it is made and executed 
#CMD can be overwritten by ENTRYPOINT but 
#ENTRYPOINT Cannot be overwritten