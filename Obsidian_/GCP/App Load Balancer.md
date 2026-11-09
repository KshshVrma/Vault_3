
create vm instances
create a load balancer template
managed instance group based on template
create fire wall rule to allow health check

gcloud compute firewall-rules create fw-allow-health-check \

create address that the end users will use to access the lb
create a health check for the load balancer to ensure that the health backends are sent the traffic.
create a backend service
add instance group as backend oto the backend service
create a url map to route the intcomming request to the service
create a target http proxy to route to url map
create a global forwarding rule

  