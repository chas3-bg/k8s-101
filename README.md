This repo serves as a k8s 101 study room.
Software of choice to keep notes is joplin.
Setup:
    podman-desktop - probably not necessary, but helps visualise stuff. It should help.
    kind cluster - I read somewhere it was faster than minikube and doesn't start VMs  -it's a container that runs the kubernetes control plane.One is good as the other, this one didn`t error out on the first try. Good enough.

I. Flask-hello deployment
    Objectives: 
    1. Run a pod with a single container in it with port 5000 (flask default) exposed, so it's accessible from the outside (local network in this case) DONE
    1.1 Add Health checks - DONE
    1.2 Create service 
    2. Break the container inside the pod and watch k8s bring a new pod up.

II. Flask ToDo app (persistent storage)
    1. Develop a todo-app. DB will be sqlite and data stored in the container.
    1.1 Create deployment, service and route 
    1.2 Break the container and watch the data dissapear (probably if I understand how it should work)

    2. Create a storage for the data outside of the container. 
III. Complete steps I and II before flooding myself with bright ideas. 

Notes will be shared once each stage is complete.

In case you want to follow along:
Flask-101 app:
https://github.com/chas3-bg/flask-hello
https://hub.docker.com/repository/docker/chas3bg/flask-hello

ToDo app:
https://github.com/chas3-bg/py-todo-app
https://hub.docker.com/repository/docker/chas3bg/flask-todo

Notes:
I. 
    1.  Pretty much boiler plate, can be done by a trained monkey or AI. Good to understand the basic structure of a deployment.
    1.1 Need those for the cluster to know when a container is broken.
    