# Azure 204

for virtual machine to connect to web server, we need to add a rule to network security group that allow traffic on port 80

click networking => add inbound security rule,
choose serive to http, and name changed to Port_80

## deploy .net app to azure vm

-   assign a dns name to vm
    Click vm overview, click dns name, put myiis1(example) in dns name label
-   add a rule for port 8172 to the network security group
    Click networking, add inbound security rule (choose destination port ranges 8172 and name port_8172)
-   check the configuration for management service in iis
    go to virtual machine iis, choose add roles and features, go to web server=> management tools, tick management service
    after installation, go to iis, choose management service, tick enable remote connection, check ipaddress has port 8172
-   install .net core hosting bundling. this allow .net app to be hosted on iis
    search .net download, choose download asp.net core runtime, find windows hosting bundle and install

-   install the web deploy 3.6 tools
    search web deploy 3.6 and install

-   install azure setting in vs application
    tools==> options=> search azure, choose account selection
    project => choose deployment => choose more actions => click edit=> connection=> validate=> click save and publish


##  Deploy app to linux vm

    go to all resource
