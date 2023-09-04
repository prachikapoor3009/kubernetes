- Rolling Update
- Recreate
- Canary
- Blue Green
- Alternate back end

CANARY
release new version of application only to a percentage of users.
10% traffic to new app
90% traffic to old app
gradually inc the %, check for stability of app and roll out for all.
ingress controller(nginx example) - that this app can be accessed by these users only.

ROLLOUT - default

BLUE-GREEN
high infra cost
fast roll back
two versions of apps running at a time
switch from v1 to v2 if not accessible and vice versa
pointing load balancer to that particular version


