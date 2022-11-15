AWS deployment with Terraform and Ansible

Exercises:

1. Setup Terraform, AWS IAM User Account & Permissions, AWS CLI and Ansible on a control VM
2. Create Terraform State File in S3 with backend.tf
3. Network Setup Part 1: Deploy VPC, Internet GWs and Subnets
4. Network Setup Part 2: Deploy Multi-Region VPC Peering
5. Network Setup Part 3: Deploy Security Groups
  - ALB SG (us-east-1): (Traffic from the Internet)
    - Inbound: 
      - TCP/80 -> 0.0.0.0/0
      - TCP/443 -> 0.0.0.0/0
    - Outbound: ALL TCP -> 0.0.0.0/0 

  - Jenkins Master SG (us-east-1): (Traffic and health checks for Jenkins Master)
    - Inbound: 
      - TCP/80 -> 0.0.0.0/0
      - TCP/443 -> 0.0.0.0/0
    - Outbound: ALL TCP -> 0.0.0.0/0 

  - Jenkins Worker SG (us-east-1): (TCP/22 SSH traffice between Jenkins Master and Worker)
    - Inbound: 
      - TCP/80 -> 0.0.0.0/0
      - TCP/443 -> 0.0.0.0/0
    - Outbound: ALL TCP -> 0.0.0.0/0 
