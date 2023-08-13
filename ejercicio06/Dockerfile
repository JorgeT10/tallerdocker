# Use this only as a workaround for containers in M1
FROM --platform=linux/amd64 registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.15-7

#Resource https://stackoverflow.com/questions/68984133/error-failed-to-solve-with-frontend-dockerfile-v0-failed-to-create-llb-defini

# FROM registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.15-7

COPY passwordapi.jar /home/jboss/passwordapi.jar
CMD ["java","-jar","/home/jboss/passwordapi.jar"]
