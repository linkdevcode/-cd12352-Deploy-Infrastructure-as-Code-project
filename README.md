# Udagram Infrastructure as Code Project

---
## Project Overview
This project uses AWS CloudFormation to set up the entire infrastructure for the Udagram application. The project includes network setup and server deployment designed to support scalability and high availability.

![Udagram Architecture](/diagram/Infrastructure-Diagram.png)

## Architecture
The infrastructure is defined across several CloudFormation scripts:
- **Network Stack**: Network resources: VPC, subnets, Internet Gateway, NAT Gateways
- **Server Stack**: EC2 resources: Autoscaling group with EC2 instances, Load Balancer, Security Groups
- **Static Content**: S3 bucket.

## Directory Structure

- `diagram/`: Infrastructure Diagram.
- `starter/`: Contains all the CloudFormation YAML templates, JSON files for template parameters and shell scripts to automate the deployment (*.sh/)

## Setup Instructions

### 1. Clone the Repository
Clone this repository to your local machine:
```bash
git clone https://github.com/linkdevcode/-cd12352-Deploy-Infrastructure-as-Code-project.git
```

### 2. Create the Network Infrastructure
Run the network setup script:
```bash
./create.sh networkstack network.yml network-parameters.json
```

### 3. Create the S3 bucket
Run the network setup script:
```bash
./create.sh s3stack s3.yml s3-parameters.json
```

### 4. Deploy the Servers
Run the network setup script:
```bash
./create.sh udagramstack udagram.yml udagram-parameters.json
```

Load Balancer Url: http://udagra-WebAp-CKCyiQ5SP7OL-534417365.us-east-1.elb.amazonaws.com

## License

[License](LICENSE.txt)
