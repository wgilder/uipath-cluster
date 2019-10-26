Note that this is very much a work in project! Much of what's described below is a wish-list and not currently available. Things that are done:
- Base JDK image
- Elasticsearch

Next steps:
- Finish ELK stack
- See about porting SQL Server and IIS (this may prove pipe-dreamy)
- Decide between docker-compose and Vagrant

Root project for creating a fully-working UiPath cluster, including:
- ELK stack
- SQL Server
- IIS
- Orchestrator
- Studio and Robot

This is designed to run on Windows Server Containers, so leverages MicroSoft-produced Docker images for this purpose. Dev Windows version is 1903. 

Most of the cluster runs on Docker images, except for Studio and the Robot which run on a VirtualBox VM. Docker for Windows doesn't play well with VB (the former requires Hyper-V, the latter conflicts with Hyper-V). Windows Server Containers runs sans Hyper-V, so allows both to coexist.