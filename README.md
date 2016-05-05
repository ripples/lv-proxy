#lv-proxy
##A front-facing component to the lecture-viewer compositional suite

###Purpose of this repository
####Ownership and Creation
This repository sits as a [git submodule](https://git-scm.com/docs/git-submodule) to the lecture-viewer application, developed by the [ripples team at UMass Amherst](https://github.com/ripples). The proxy should work specfically with the lv-client and lv-server submodules.

####Seperation of Concerns
This proxy will pipe the requests to and from the client and server node applications in a way that allows for all requests to uniformally be received through the default HTTP Protocol (i.e. port 80). This normalization of a given DNS address decreases the data coupling of the frontend application to the backend. Without this component, the server and the client may have to use strange port numbers to both concurrently communicate out of the same DNS address. For this reason, requests and responses are piped through this component of the lecture-viewer suite.

####Use and modification
The proxy itself is barebones without something to proxy to. Short of modifying default.conf (in your own branch!) for other purposes, there is very little reason to have this repository by itself.

####Reference and credit
Dockerfile was written originally by [Gary White](https://github.com/GaryPWhite) and developed with the [nginx Docker build guide](https://www.nginx.com/blog/deploying-nginx-nginx-plus-docker/). If you're interested in contributing to the repository or making changes, please reference this guide to get started.
