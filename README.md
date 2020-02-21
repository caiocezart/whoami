# whois

#### Caio Trevisan

TL;DR: involved with technology for the past 15 years, loves to learn new things and enjoy automating everything. From Networking to Ful Stack Development, on-premises to cloud, can tackle any complex scenarios and is used with fast-paced transformation environments.

- Website: [www.caiotrevisan.com](https://www.caiotrevisan.com)
- Linkedin: [linkedin.com/in/caiocezart/](https://www.linkedin.com/in/caiocezart/)


## Index

- [Introduction](#introduction)
- [Academic Curriculum](#academic-curriculum)
- [Industry Certifications](#industry-certifications)
  - [Cloud Native Computing Foundation](#cloud-native-computing-foundation)
  - [Amazon Web Services](#amazon-web-services)
  - [Google Cloud Platform](#google-cloud-platform)
- [Recent Learnings](#recent-learnings)
- [Current Aspirations](#Current-aspirations)
- [Hobbies](#hobbies)
- [Professional Projects](#professional-projects)
  - [Warehouse WIFI modernisation](#Warehouse-WIFI-modernisation)
  - [Wholesale returns product portal](#Wholesale-returns-product-portal)
  - [End-to-end integration from Retail POS systems to SAP and Warehouse Management System](#End-to-end-integration-from-Retail-POS-systems-to-SAP-and-Warehouse-Management-System)
  - [Powercycling cloud resources](#Powercycling-cloud-resources)
  - [IAM Automation](#IAM-Automation)
  - [Infrastructure migration from Azure to AWS](#Infrastructure-migration-from-Azure-to-AWS)
  - [Many infrastructure modernisation from on-premise to AWS](#Many-infrastructure-modernisation-from-on-premise-to-AWS)
  - [GCP + Kubernetes greenfield project](#GCP-+-Kubernetes-greenfield-project)


## Introduction

- Foreign immigrant from Brazil, got permanent residency and later citizenship through a  sponsorship working as a Network Admin/Full Stack Developer
- Started in IT doing Computer Games servers at home (Ragnarok, Tibia, etc)
- Served 5 years in the Airforce as a Sys/Network Administrator
- Diploma in Information Technology and Bachelor in Networking
- IT Consultant helping big enterprise companies moving to the cloud or improve existing environments


## Academic Curriculum

  - Diploma in Information Technology
  - Bachelor in Networking with University being both in Brazil and an extra year at University of Technology, Sydney (UTS)
  - Certificate IV in Commercial Cookery (TAFE) (in progress)
  - Applied to start in 2020: Master of Science in Computer Science


## Industry Certifications

### Cloud Native Computing Foundation

- Certified Kubernetes Administrator
- Certified Kubernetes Application Developer


### Amazon Web Services

- AWS Certified Cloud Practitioner
- AWS Certified Developer - Associate
- AWS Certified SysOps Administrator - Associate
- AWS Certified Solutions Architect - Associate
- AWS Certified Solutions Architect - Professional
- AWS Certified DevOps Engineer - Professional
- AWS Certified Advanced Networking - Specialty
- AWS Certified Security - Specialty
- AWS Certified Big Data - Specialty


### Google Cloud Platform

- Google Cloud Certified - Professional Cloud Architect


## Recent Learnings

- Google Cloud Platform
- Kubernetes Administration
  - cluster management
    - automated deployment
    - Istio service mesh
    - nodepool isolation strategies
    - multi-tenant environment
    - workloads isolation
  - cluster security
    - gatekeeper (openpolicy agent)
      - open-source contributor
    - pod security policies
    - network policies
    - conftest
- Golang software development
  - development of kubernetes custom operators
- Anthos
  - Anthos Configuration Management (ACM)
  - policy-controller
- Sharing Knowledge
  - Community open-source DevOps classes - [DevOps Academy](https://github.com/devopsacademyau/academy)
- Leadership
  - Community meetups organization


## Current Aspirations

- Focused on improving soft and leadership skills
- Work more with people and impact on other lifes
- Public Speaking
- Blameless culture
  - post mortums
  - brownbags from learnings
  - pair programming
- Explore data, machine learning and IA


## Hobbies

- Co-founder of IT.BR Melbourne group
  - Brazilian professonal community that work with IT living in Melbourne
  - Over 300 members
  - bi-monthly meetups with a mix of technical and local market opportunities talks with over 80 people attendance
- Studying to be an accreditate Chef
  - Last semester of a Certificate IV TAFE in Commercial Cookery 
- Practicing sports (soccer + tennis)
  - Always happy to be involved in any physical activities
- Listen to audio books
  - Recent ones are: Dare to Lead, Phoenix Project (again), Leaders Eat Last


## Professional Projects

- [Warehouse WIFI modernisation](#14k-square-meters-Warehouse-WIFI-modernisation)
- [Wholesale returns product portal](#Wholesale-returns-product-portal)
- [Powercycling cloud resources](#Powercycling-cloud-resources)
- [IAM Automation](#IAM-Automation)
- [Infrastructure migration from Azure to AWS](#Infrastructure-migration-from-Azure-to-AWS)
- [Many infrastructure modernisation from on-premise to AWS](#Many-infrastructure-modernisation-from-on-premise-to-AWS)
- [Kubernetes greenfield project](#Kubernetes-greenfield-project)
- [Spot Instances](#spot-instances)


### Warehouse WIFI modernisation

#### problem

- warehouse with 5k orders daily
- 14k square meters of size
- 15 meters high ceilings
- metal structures everywhere

#### project

- wifi signal analysis for access points installation
- hardware sourcing
- planned work for minimal disruption of a 18 hours a day warehouse
- stakeholders project proposal

#### results

- effective physical installation of all new hardware with zero downtime

### Wholesale returns product portal

#### problem

- wholesale faulty products complaint being received as spreadsheets
- manual entry of forms to SAP
- 2 full time employes to process returns

#### project

- create an external portal where clients can login and lodge faulty or missing order items with option to upload images

#### solution

- full stack solution in C# .net
- backend using WebAPI 2.0 as a big monolith serving all endpoints
- frontend in AngularJS consuming backend api's
- API's running from AWS Lambda being served by AWS API Gateway
- Static content with js scripts hosted on S3. Image upload also sent to S3 and only images metadata saved to database
- Clients can retrieve pre-existing details from SAP
- Clients can auto-fill orders based on existing invoice numbers from SAP

#### learnings

- hard to do full stack engineering by itself
- no project management results in many iterations for the same issue
- slow paced project
- at v1 release many new features requested due to bad planning
- lack of software versioning makes collaboration hard


### Powercycling cloud resources

#### problem

- existing tool written in python taking over 1hour to loop through resources
- no error handling
- resources being ignored

#### project

- complete rewrite of python automation using Nodejs
- error and logging handling
- admin management tasks (manual, yaml config)

#### solution

- complete application consuming AWS API's to loop through 200+ accounts to powercycle resources and save money on iddle services
- stablished a clear path of development and a roadmap of new features (instances, ebs, snapshots)
- solution pilot showcase for stakeholders
- discovery sessions to identify priority order of resources onboarding to new automation and avoid disruption
- fully deployed to production within 6 months
- admins have full manual control of tasks
- automation is idempotent


### IAM Automation 

#### problem

- lack of AWS guardrails to allow end-users to have open freedom of IAM resources creation
- too many requests of resource creation to be handled manully
- possibility of human error when peer reviewing code to create IAM resources and allowing more permission than necessary

#### project

- integration of Github webhooks with AWS Step Functions to trigger an automated suit of tests
- code submitted and all tests pass, gets deployed to the AWS account through cloudformation

#### solution

- an end-user submits a cloudformation template to a github repository and triggers a step function pipeline
- the automation does from basic lint/syntax checks to least privilege code analysis testing
- any errors, lambdas will post log to Github Pull Request
- admins have manual controls to override tests through Github labels


### Infrastructure migration from Azure to AWS

#### problem

- company need to move around 40 apps with databases (most mysql) and 1PB of data from Azure to AWS.

#### project

- stablish an AWS foundations
- upgrade existing databases to be compatible with managed servers
- upgrade Windows Server pet instances to auto-scaling groups
- connect Azure > Client DC > AWS through direct fiber connection
- application cutovers

#### solution

- AWS Direct Connect project to client datacentre
- Dynamic routing configuration between Azure > Client DC > AWS
- Local application to buffer blob storage from Azure express route and send to AWS S3
- AWS Landing Zone foundations (Identity, Audit, Shared, Envs)
- Migration of .NET framework apps to EC2 on auto-scaling groups
- AWS ASG automation to join cattle instances to AD and cleaning up jobs
- Octopus Deploy for CICD
  - deployment strategies (blue/green, canary)
- Mysql database upgrades to be compatible with AWS Aurora
- once everything ready, required downtime for a last minute database backup/restore and DNS cutover


### Many infrastructure modernisation from on-premise to AWS

#### problem

- companies want to move from onpremise to cloud

#### project

- discovery sessions for identifying workloads that need migrationa
- case by case identify lift and shifts and application modernisation
- go to containers where possible
- cloud foundations (accounts, baseline security, integration with existing IDP)
- infrastructure as code -> CICD
- team upskilling to manage new infrastructure (brownbags, 101)


### Kubernetes greenfield project

#### problem

- stablish a multi-cluster Kubernetes infrastructure in the cloud on a highly regulated environment
- traditional slow-paced environment
- not agile
- internal politics
- people egos

#### project

- iterations and discovery to decide which cloud provider
- security controls
- architecture diagrams
- proof of concepts
- cloud native
- golang
- everything as code

#### solution

- Kubernets on GCP due to better support for Kubernetes (GKE)
- security control tools analysis and comparison
  - twistlock
  - gatekeeper
  - conftest
  - psp
  - network policies
  - rbac integration with local IDP
- cluster design and automation
  - nodepool isolation (ingress, egress, tiers)
  - security by default
  - cluster bootstrap automation (namespaces)
  - 3musketeers + helm charting
- gatekeeper
  - matching security GKE controls to opa policies
  - deployment/patching/update automation
- workload isolation
  - istio service mesh
  - namespace communication isolation
  - binary authentication


### Spot Instances

#### Personal projects

- CI/CD private workers using ECS with Spot instances
  - $15/month
- Kubernetes spot instances node
  - non-critical batch jobs
  - cicd workers
  - intesive resource data jobs
  - peak traffic
  - cluster auto-scaler(CA)
  - interrupt-handler
  - horizontal pod autoscaler (HPA)
  - disruption budget
  - use of affinity/taints/tolerations
- CS:GO Server running on ECS + Spot Blocks. API request to API Gateway + lambda will trigger spot block for X hours and bring down stack when not needed.


- https://github.com/caiocezart/k8s-spot
