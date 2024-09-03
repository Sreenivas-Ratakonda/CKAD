kubernetes core concepts consist of the following.

    1. k8s Architecture 
    2. configuration and creation of pods 



# K8S Architecture: 

Node is where our container runs...

multiple nodes form a cluster i.e k8s cluster 



k8s will contains following components.

        1. api server 
        2. scheduler 
        3. controller 
        4. etcd datastore 
        5. kubelet agent 
        6. container runtime. 


**1. API Server** 

    its a kind of front-end to interact with k8s cluster


**2. etcd keyvalue store (highly available)**

    its a higly available key-value store that stores data across the nodes it basically store all nodes in cluster  related info state..etc 

    make sure there are no conflicts between the Master and nodes. (is it >?>>)

**3. Scheduler** 

    basically it looks for newly created conatiners and assigns them to the nodes. (conatiner and load distro across cluster)

**4. Controller**

    brain behind orchestration its very imp component... it basically monitors if there are any nodes or conatiner are down and if they are down it brings new ones up. 


**5. Kubelet Agent**

    it runs on the worker nodes along side of the container runtime , its resp for making sure that containers are running on the worker node. 

**6. container Runtime**

    its where our conatiners runs on the node. 


**A proper look at the k8s architecure**

![alt text](image.png)

**refer:** https://luludansmarue.github.io/kubernetes-docker-lab/k8s/architecture

# Master minion side of k8s :

    in K8S we have master node and slave nodes (minions )

    Master

        1. kube-api server 
        2. etcd
        3. scheduler
        4. controller 

    
    minion

        1. container runtime (container-d | crio |  rkt )
        2. kube-agent (kubelet)


# Kubectl 

`kubectl run hello-minikube`

`kubectl get ns`

`kubetcl cluster-info`

`kubectl get nodes`




# Docker VS Container-D:






