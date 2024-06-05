# Appendix B: Disabling Small Messages

In BlazeDS, the small messages optimization mechanism can be disabled by setting the channel definition's `enable-small-messages` sterilization property to `false` in the following configuration file:

```
install_root\tomcat\webapps\samples\WEB-INF\flex\services-config.xml
```

The following example disables small messages on the `pooling-amf` channel:

```xml
<channel-definition id="my-polling-amf" class="mx.messaging.channels.AMFChannel">
    <endpoint url="http://{server.name}:{server.port}/{context.root}/messagebroker/amfpolling" class="flex.messaging.endpoints.AMFEndpoint"/>
    <properties>
        <serialization>
            <enable-small-messages>false</enable-small-messages>
        </serialization>
        <polling-enabled>true</polling-enabled>
        <polling-interval-seconds>4</polling-interval-seconds>
    </properties>
</channel-definition>
```