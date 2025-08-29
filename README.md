

```markdown
# Crossplane AWS Infrastructure as Code Labs

This repository contains **Crossplane** manifests, lab exercises, and supporting files to provision and manage AWS infrastructure using **Kubernetes-native Infrastructure as Code (IaC)**.  
It includes examples of VPC, Subnets, EC2, Security Groups, VPC Endpoints, IAM Roles, and Database resources.  

---

## 📂 Repository Structure

```

.
├── dynamodb/                 # Example manifests for DynamoDB
├── mongodb/                  # Example manifests for MongoDB
├── vpc.yaml                  # VPC definition
├── subnet.yaml               # Subnet definition
├── igw\.yaml                  # Internet Gateway
├── route.yaml                # Route table
├── routegw\.yaml              # Route table association
├── rta.yaml                  # Route Table attachment
├── sg.yaml                   # Security Group
├── sgingress.yaml            # Security Group ingress rules
├── keypair.yaml              # EC2 key pair
├── ec2.yaml                  # EC2 instance configuration
├── vpcendpoint.yaml          # VPC endpoint config
├── epsvc.yaml                # Endpoint service example
├── awsproviderconfig.yaml    # Crossplane AWS provider config
├── ec2provider.yaml          # Crossplane EC2 provider example
├── adminrole.yaml            # IAM admin role
├── dbadminrole.yaml          # IAM DB admin role
├── ami.yaml                  # Custom AMI definition
├── composite.yaml            # Crossplane Composition
├── crd.yaml                  # Crossplane CRD
├── crdvpc.yaml               # Custom VPC CRD
├── claim.yaml                # Composite Resource Claim
├── lab 9 providerconfig.txt  # Lab instructions
├── lab 10.txt                # Lab instructions
├── Lab 7 k8provider.txt      # Lab notes
├── Lab 8 secret.txt          # Secrets config for labs
├── k8s-intro.pptx            # Slides - Kubernetes intro
├── crossplane.pptx           # Slides - Crossplane overview
├── Infrastructure as Code-1.pptx  # Slides - IaC concepts

````

---

## 🚀 Getting Started

### Prerequisites
- Kubernetes cluster (Kind, Minikube, or managed cluster like EKS/GKE/AKS).
- [Crossplane](https://crossplane.io/) installed.
- AWS credentials with appropriate IAM permissions.
- `kubectl` CLI.

### Setup AWS Provider
```bash
kubectl apply -f awsproviderconfig.yaml
kubectl get providers
````

### Deploy Infrastructure

Example: Create a VPC and Subnet

```bash
kubectl apply -f vpc.yaml
kubectl apply -f subnet.yaml
```

Check created resources:

```bash
kubectl get managed
```

### Using Compositions

Apply CRDs and Composite definitions:

```bash
kubectl apply -f crd.yaml
kubectl apply -f composite.yaml
kubectl apply -f claim.yaml
```

---

## 🧪 Labs

* **Lab 7**: Kubernetes Provider setup
* **Lab 8**: Managing Secrets
* **Lab 9**: Provider Config for AWS
* **Lab 10**: Advanced Crossplane usage

---

## 📖 Documentation & Slides

* `k8s-intro.pptx` → Intro to Kubernetes
* `crossplane.pptx` → Crossplane deep dive
* `Infrastructure as Code-1.pptx` → IaC concepts

---

## 🤝 Contributing

Feel free to fork, raise issues, or submit PRs for enhancements.

---

## 📜 License

This project is for **educational and lab purposes**. Review IAM and AWS configurations before using in production.

```

---


