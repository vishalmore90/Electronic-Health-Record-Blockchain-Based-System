# Electronic Health Record Blockchain Based Platfrom - Project

## Tech stack

    - Hyperledger Fabric blockchain (Node SDK JavaScript)
    - Node.js
    - Next.js
    - IPFS

<!-- ADD github access 

$ eval "$(ssh-agent -s)"
$ ssh-add ~/ssh/github -->

# Steps to setup project

## Download fabric binarys and fabric sample repo

    $ ./install-fabric.sh 

## To test network 

    $ cd fabric-samples/test-network
    $ ./network.sh up

    $ docker ps    // to check running container or check in docker desktop
    
    $ ./network.sh down     // to down network

 ## to run network with ca and create mychannel 

    $ cd fabric-samples/test-network
    
    Create network with ca cert: 
    
    $ ./network.sh up createChannel -ca -s couchdb

    ### Chain code deployment command

 - Deploy chain code
	    
    $ ./network.sh deployCC -ccn ehrChainCode -ccp ../asset-transfer-basic/chaincode-javascript/ -ccl javascript

    *Down Network - only if you want to stop network or close system
	
    $ ./network.sh down
    
### Register Admin

    $ cd server-node-sdk/
    $ node cert-script/registerOrg1Admin.js
    $ node cert-script/registerOrg2Admin.js

