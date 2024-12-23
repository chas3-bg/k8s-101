This repo serves as a k8s 101 study room.
Software of choice to keep notes is joplin.
Setup:
    podman-desktop - probably not necessary, but helps visualise stuff. It should help.
    kind cluster - I read somewhere it was faster than minikube and doesn't start VMs  -it's a container that runs the kubernetes control plane.One is good as the other, this one didn`t error out on the first try. Good enough.

App to run: A python flask hello-world.
Objectives: 
1. Run a pod with a single container in it with port 5000 (flask default) exposed, so it's accessible from the outside, in this case my private network (don' forget firewall-d). Probably will need to code some health checks. 
2. Break the container inside the pod and watch k8s bring a new pod up.
3. Code a todo-app with backend and a simple front end. Conteinerize it in 2 containers (BE and FE). DB will be sqlite and data stored in the BE container. Repeat step 1 and 2 and repeat. 
3.1 Watch data dissapear.
4. Create a storage for the data outside of the container. 
5. Complete steps 1 and 2 before flooding myself with bright ideas. 

Notes will be shared once the project is complete.