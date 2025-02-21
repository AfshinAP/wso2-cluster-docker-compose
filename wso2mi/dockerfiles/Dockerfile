FROM 10.1.20.108:8087/wso2/wso2mi:latest
LABEL maintainer="WSO2 Docker Maintainers <dev@wso2.org>"

COPY capps ${WSO2_SERVER_HOME}/repository/deployment/server/carbonapps/
COPY postgresql-42.7.4.jar ${WSO2_SERVER_HOME}/repository/components/dropins/
