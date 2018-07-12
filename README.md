# OpenResty Reverse Proxy

**fork author:** captaincode0

**notes:** this reverse proxy is based on NGINX used for one Amazon EC2 container.

**author:** octoberswimmer

**repository:** `https://github.com/octoberswimmer/heroku-reverse-proxy`

## Installation

```bash
heroku login #register localy throw heroku toolbet
git clone https://github.com/captaincode0/openresty-reverse-proxy.git
cd openresty-reverse-proxy
git remote add heroku heroku-repo.gits

heroku apps #list applications

# Change application stack from cedar-16 to cedar-14
heroku config:set stack="cedar-14" --app app-name

# Deploy reverse proxy
git push heroku +HEAD:master #use +HEAD pointer refers to last commit and master branch
git config:set UPSTREAM_SERVER="rest-api.com" --app app-name

#test the proxy
heroku open --app app-name
```

