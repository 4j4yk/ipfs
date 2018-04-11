# I P F S 

<img src="https://upload.wikimedia.org/wikipedia/commons/1/18/Ipfs-logo-1024-ice-text.png" style="align:center;">

## Introduction to IPFS

InterPlanetary File System (IPFS) is - 
* Open source project :heavy_check_mark: 
* Protocol :heavy_check_mark: 
* Network :heavy_check_mark:
* Peer-to-peer distributed file system :heavy_check_mark:
* Modular :heavy_check_mark:
* encrypted :heavy_check_mark:

and so on !! 

Take a deep dive [here](https://github.com/ipfs/ipfs) !! 

In short, it is Git like version control system which works like BitTorrent and provides security like bitcoin !!!! Wow !!! 
There is more though, it can work as web and even has its own name service called IPNS .... 

## Why would we use it ?

To make web faster, safer and more open. but how ? 

Look at this [Stanford Seminar - IPFS and the Permanent Web](https://www.youtube.com/watch?v=HUVmypx9HGI)

Or just look here - ![The web](https://ipfs.io/ipfs/QmNhFJjGcMPqpuYfxL62VVB9528NXqDNMFXiqN5bgFYiZ1/images/centralized-decentralized-distributed.jpg "IPFS")
*Source ipfs.io*

* Centralized 
   - One place stores everything and everyone access the files from this place ! 
   - (Imagine One StarBucks :coffee: in town and Everyone wants :coffee: !)
   - I won't get coffee soon :(
* Decentralized 
   - One place stores everything and everyone access the files from this place ! 
   - (Imagine Main StarBucks :coffee: in town and Everyone wants :coffee: !)  
   - I will get coffee in sometime :|
* Distributed
   - One place stores everything and everyone access the files from this place ! 
   - (Imagine Everyone can sell StarBucks :coffee: and Everyone wants :coffee: !)
   - I will get coffee right away :D
   
### Okay !! I think you can figure out things now and will proceed to some hands on -- 

# Installation 
* Download [ipfs](https://dist.ipfs.io/#go-ipfs) for desired os
> For unix based os 
```shell
tar xvfz go-ipfs.tar.gz && cd go-ipfs && ./install.sh
```
> For windows `unzip and run ipfs.exe`
    
* `ipfs help` will list all cmds and subcommands with direction to use, at this point I assume you all are familier with command line utilities like git or any other.

### Okay , lets dive into ipfs world ! 

#### setup the repo
> create a folder for name ipfs 
    navigate to that folder
        and initialize a repository ! 

```bash
mkdir ipfs && cd ipfs && ipfs init
```

![init repo](./imgs/initrepo.png)

> ipfs init will initilize the repository similar to `git init`. This generates an RSA keypair and peer identity hash ! files with this peer can be seen using cat cmd

```bash
ipfs cat ipfs/hash/name
```

![init repo](./imgs/cat.png)

Now we will create a file and add it to our ipfs repository 

```bash
echo 'Hello ipfs world !' >> hello.txt
```
![init repo](./imgs/add.png)

After adding this file to ipfs we can see that it generates a hash to address file, and the content can be seen using this file hash.

If change this file and add it again, we will have two versions of the same files with different hash.

```bash
echo 'Hello again !' >> hello.txt
```
you can see now we have two different version with different hash indentity.

![init repo](./imgs/addagain.png)

> This how ipfs provides verions of same file over time and we can keep track when the files have 
been changed.
 
I will leave it upto you to explore ipfs ls and refs cmds which shows the file list and references and move on to the swarm part !! 

We have added the files to ipfs repo which is local and ready to become a peer in ipfs network.
    
### ctd .....