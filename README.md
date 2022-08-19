# Install Apache Skywalking Backend + UI / Apache Skywalking Agent 


## Apache Skywalking Backend + UI

```bash
# create a custom directory
mkdir -p /docker/apache-skywalking
cd /docker/apache-skywalking

# get the docker-compose.yml file and the .env file
wget -O docker-compose.yml https://raw.githubusercontent.com/concosminx/apache-skywalking-dc/master/docker-compose.yml

wget -O .env https://raw.githubusercontent.com/concosminx/apache-skywalking-dc/master/.env

# start the containers
docker-compose up -d && docker-compose logs -f

# to stop the containers, run 
docker-compose down
```

# Apache Skywalking Agent
- download the agent from [here](https://skywalking.apache.org/downloads/)
- check all configuration options for agent [here](https://skywalking.apache.org/docs/skywalking-java/v8.10.0/en/setup/service-agent/java-agent/configurations/#table-of-agent-configuration-properties)
- use the agent in tomcat with catalina opts `set CATALINA_OPTS=-javaagent://docker/apache-skywalking/agent/skywalking-agent.jar` or with java opts `JAVA_OPTS=%JAVA_OPTS% -javaagent:docker/apache-skywalking/agent/skywalking-agent.jar`