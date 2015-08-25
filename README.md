Docker build for Apache TrafficServer (SPDY enabled)
================================

This repository provides Dockerfile for [Apache TrafficServer][0]
built with [SPDY][1] enabled.

### Status
- Debian: latest
- TrafficServer: 5.3.1

### Usage:

 - Execute
 `docker run -d --name TrafficServer -p 8080:8080 chadlyon/trafficserver`
 - Browse [http://&lt;your server ip address&gt;:8080/][2]
 - Stop and start again
   - `docker stop TrafficServer`
   - `docker start TrafficServer`

### Configuration:

This build comes with the standard configuration as provided by TrafficServer, configuration are under the following path: `/etc/trafficserver`

You can use docker volumes mount feature to run TrafficServer with your specific configuration, for example:

`docker run -d --name TrafficServer -p 8080:8080 /MY-CONFIGS/trafficserver/:/etc/trafficserver/ shaker/trafficserver`

You need to change `/MY-CONFIGS/trafficserver/` to your configuration path.

  [0]: http://trafficserver.apache.org/
  [1]: https://developers.google.com/speed/spdy/
  [2]: http://127.0.0.1:8080/
