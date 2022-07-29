# Install Apache Skywalking Backend + UI / Apache Skywalking Agent 

- download the agent from [here](https://skywalking.apache.org/downloads/)
- check all configuration options for agent [here](https://skywalking.apache.org/docs/skywalking-java/v8.10.0/en/setup/service-agent/java-agent/configurations/#table-of-agent-configuration-properties)
- use the agent in tomcat with catalina opts `set CATALINA_OPTS=-javaagent:C:\Agents\skywalking-agent.jar`
- or java opts `JAVA_OPTS=%JAVA_OPTS% -javaagent:C:\Agents\skywalking-agent.jar`

- start the containers with `docker-compose up -d`
- stop the containers with `docker-compose down`