# Assignment details and instructions

**DevOps take-home problem statement:**

Some tools we use for monitoring at Getaround are Prometheus and Grafana.
Please provide a script or set up in a framework. e.g. Terraform, SaltStack, Puppet, etc. to automate the installation of a Prometheus server configured to scrape itself, and a Grafana installation that consumes this Prometheus datasource.  Please also configure Grafana to have a username and password login with administrator permissions. The desired output is an automated, repeatable process, with nothing manual required with the exception of having to change some parameters.
A local Minikube or Docker installation with Kubernetes is an easy way to run several things locally in isolation.  Both AWS and GCP have free tiers which should be sufficient if wishing to run a long-running server.  The focus is on the installations, not the platform on which they run.
Please provide details of how to replicate whatever setup you utilize and a tarball of whatever automation (script, etc.) you create, with instructions on how to run it. These should be emailed to devops@getaround.com.



**Prerequisites**:

1. An active kubernetes cluster. Solution will work for any platform like minikube, GKE, EKS etc as long as .kube.config is updated.
2. Kubectl installed and configured to connect to the desired cluster. 
3. helm installed and stable repo updated:

    a. `helm repo add stable https://kubernetes-charts.storage.googleapis.com`
    
    b. `helm repo update`
4. Terraform installed




**Solution details:**

Git repo :  https://github.com/BlueMaverick/getaround-assignment




**Instructions:**

1. Clone repo
    `git clone https://github.com/BlueMaverick/getaround-assignment.git`
2. Execute the terraform plan:

`terraform init`

`terraform plan`

`terrafor apply`




**Result**: Installs Prometheus & Grafana clusters atop Kubernetes.


**View Grafana Dashboard:** Execute `./grafana_dashboard_local.sh`


**View prometheus UI:** Execute `./prometheus_ui_local.sh`