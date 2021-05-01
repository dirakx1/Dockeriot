## Dockeriot for things layer.
Dockeriot can be used for specific application on the "things layer" that
in an iot environment. 

For example, you are building an application that runs a webserver on an iot device.
locally, you could build your app and then run it f.e 
```
docker build -< Appcontainer/dockeriot.Dockerfile -t dockeriot
docker run -w /Appcontainer/ -t -i dockeriot 
```

Note: This example is using only an Appcontainer, but we could also define: Communication and Sensor-actuator containers, 
that are part of the "Things layer"

The same building/run procedure must be applied on all the iot devices you want to add
to the dockeriot environment. 


