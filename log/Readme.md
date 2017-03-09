# Logs:

##2017/03/08
Docker swarm running with a manager node and one worker.

Tested it with a ping service ( docker service create --replicas 5 --name pingu hypriot/rpi-alpine-scratch ping google.com )

ID            NAME      IMAGE                              NODE            DESIRED STATE  CURRENT STATE               ERROR  PORTS
5qi1id72mp88  pingu.1   hypriot/rpi-alpine-scratch:latest  resilioworker1  Running        Running about a minute ago
v3kdczysbx6j  pingu.2   hypriot/rpi-alpine-scratch:latest  resilioadm      Running        Running 2 seconds ago
q2azhsiplpgk  pingu.3   hypriot/rpi-alpine-scratch:latest  resilioadm      Running        Running 4 seconds ago
fju8ksu3yi58  pingu.4   hypriot/rpi-alpine-scratch:latest  resilioworker1  Running        Running 18 seconds ago
l5p5aa2cofhc  pingu.5   hypriot/rpi-alpine-scratch:latest  resilioworker1  Running        Running 18 seconds ago

We are updating wiki with the steps we followed to get here.

##2017/03/02
Changed root password for our "la de sempre" password.

Granted access to the raspberry via ssh configuring a port forwarding on the router, a dhcp for an static IP for the raspberry and using a DynDNS (noip.com), tomorrow I'll make some changes on the ssh service to make this access more secure, for now I'm shutting down the raspberry.

##2017/02/22

###Waiting for IP access.

Please, sort it ASAP.

As soon as we have all 3 raspberrys working with docker swarm, we will start to develop our web service.

Our objective is to have it running at the end of march.

##2017/02/17

###Definition of the project

Finally we decided that we are going to use docker swarm instead of pacemaker or any other cluster software.
