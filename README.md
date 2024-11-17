# DevOps Upskill Challenge
DevOps Upskill Challenge: From "Hello World" to Kubernetes

If you are in Github, there's a nicer layout at [DevOpsUpskillChallenge.com](https://devopsupskillchallenge.com/)

## What

A curriculum or roadmap that covers basic DevOps/Backend/SRE concepts and technologies. Aimed at students, technical people from other fields wanting to learn or move into DevOps or Backend development (sysadmins, software developers, IT professionals etc) and junior DevOps.  

As a positive extra outcome, people working through this roadmap will end up with a Git **DevOps project repository that they can use in their resume**.

Characteristics:
- Objective-based. Each challenge will have clear conditions of victory.
- Practical, hands-on for the most part (derived from above).
- Not a "step-by-step" guide of the "follow the text and copy-paste" type. Not for passive consumers but more like "learning the hard way".
- Starting with the "why" in each section.
- There will be often many different ways of accomplishing the objective.
- There will be a bias towards skills needed in jobs and job interviews.

The DevOps Upskill Challenge project can be abbreviated as "DOUC".

(Douc is also a cute monkey)

<img src="douc.jpg" alt="douc" width="300"/>


# How

- Pick one challenge and try to accomplish its objectives. You can use a different order (but there are dependencies) or skip the challenges you are already familiar with.
- If you get stuck or have comments, you can ask in the `#devops_upskill_challenge` channel of the [Hangops Slack](https://hangops.slack.com/) or in the Reddit [/r/DevOpsUpskill](https://www.reddit.com/r/DevOpsUpskill/) community.

# What is DevOps?

<img src="devops.png" alt="devops" width="600"/>

There is no one definition of "DevOps". For our purposes we'll use a practical definition: _"DevOps is the set of skills that companies ask for in jobs labeled as DevOps Engineer"_.  

Those skill areas are mostly: CI/CD, (for the most part cloud) infrastructure and operations (monitoring, troubleshooting).  

There's also a "DevOpsyness" component as a way of doing things, primarily _Infrastructure as Code (IaC)_ and _automation_ – which is another way of saying "doing infrastructure with the tooling and workflow of a software engineer.  

And there are also some good practices typically mentioned like frequent and continous deployments, short feedback loops, (see DORA metrics for example), as well as some more vague good intentions that could be as well be part of any (software) engineering project or practice, not just DevOps, like continuous improvement or collaboration.

For a longer discussion of what is DevOps in practice, see this [blog post](https://docs.sadservers.com/blog/what-the-f-is-devops/).

# Challenges

## [1. Linux Server](1.%20Linux%20Server/)

- 1.1 Objective: characterize a server: what’s its purpose, is it busy, does it have errors?
- 1.2 Objective: parsing logs and metrics (find/grep/cut/uniq etc )

## [2. HTTP](2.%20HTTP/)

- 2.1 Objective: create code that responds to HTTP requests (eg browser http://localhost:8080) with "Hello World". Examples with: Code (Java, Python, Golang, Java) and Web servers (Nginx, Apache)
Concepts:
    - HTTP protocol, header/body, response codes, curl
    - Golden metrics concepts
    - APIs concepts, REST, json 
    - "Architecture" types of applications (request/response / batch / streaming)

## 3. Git & GitHub
- 3.1 Objective: create your own private Github repository and commit previous HTTP exercise. Create PR.
- 3.2 Objective: (GitHub Actions) run parser test. Run code test.

## 4. Cloud Instance
- 4.1 Objective: get an AWS account.
- 4.2 Objective: get an ec2 instance, put the code from HTTP objective and see “Hello World” in a public hostname (should survive a reboot: systemd, Docker).

## 5. Infrastructure as Code - Ansible
(depends on HTTP code and Cloud instance)
- 5.1 Objective: deploy code / linux packages (eg web server) to ec2 instance

## 6. Docker
(depends on HTTP code and Cloud instance)
- 6.1 Objective: put the HTTP code in a Docker image, build and push to Docker registry.
- 6.2 Objective: run with Docker Compose in the ec2 instance
- 6.3 Objective: push everthing using Ansible

## 7. Cloud
(depends on HTTP code and Cloud instance)
- 7.1 Objective: add DNS with Route 53
- 7.2 Objective: create an AMI of the web server, deploy two servers behind ELB
- 7.3 Objective: create an autoscale group. Add the name of the instance to the output "hello world $instance_id". Test with a stress tool (objective is to see more than one instance).

## 8. Continous Integration (CI)
(depends on HTTP code and Cloud instance)
- 8.1 Objective: using Github actions, on push/merge changing the message (eg to “Hello Universe”), it gets deployed to cloud server(s) automatically

## 9. Infrastructure as Code - Terraform
(depends on AWS account)
- 9.1 Objective: create ec2 instance and requirements (VPC, subnet, sec group)
- 9.2 Objective: create all elements in the Cloud section

## 10. Observability & Alerting
(depends on HTTP code and Cloud instance)
- 10.1 Objective: add Prometheus/Grafana to count number of web requests
- 10.2 Objective: push web (application) logs to Loki or ElasticSearch
- 10.3 Objective: add Prom alerts on number/frequency of HTTP requests

## 11. Kubernetes
(Depends on Docker)
- 11.1 Objective: create a K8Scluster in the cloud (EKS for ex)
- 11.2 Objective: push web app Docker image to cloud repo (ECR for ex)
- 11.3 Objective: create Deployment manifest to create web app pod in k8s
- 11.4 Objective: add Prometheus/Grafana
- 11.5 Objective: add app log collection
- 11.6 Objective: automate (CI/CD) creation and deployment of new Docker images to K8S cluster upon code change & push.










