A CLOUD GURU COURSE: AWS deployment with Terraform and Ansible

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
    - Outbound: 
      - ALL TCP -> 0.0.0.0/0 

  - Jenkins Master SG (us-east-1): (Traffic and health checks for Jenkins Master)
    - Inbound: 
      - ALB -> TCP/80
      - TCP -> Jenkins Worker
    - Outbound: 
      - ALL TCP -> 0.0.0.0/0 

  - Jenkins Worker SG (us-east-1): (TCP/22 SSH traffice between Jenkins Master and Worker)
    - Inbound: 
      - TCP -> Jenkins Master
    - Outbound: 
      - ALL TCP -> 0.0.0.0/0 

6. **LAB** - Creating a Multi-Region Network with VPC Peering Using SGs, IGW, and RTs

7. Fetch AMI IDs using Data Source 

8. Deploying Key Pairs to App Nodes

9. Deploy Jenkins Master and Worker Instances

10. Configure Terraform Provisioner for Config Management via Ansible

11. Creating ALB and Routing Traffic to EC2 App Nodes

![image](https://user-images.githubusercontent.com/93227818/202896381-4e4925a0-b71a-42a9-93f8-3da73c4e6311.png)

12. **LAB** - Deploying Jenkins Master and Worker Nodes in AWS Behind an ALB Using Terraform and Ansible

![image](https://user-images.githubusercontent.com/93227818/202844262-951f4307-0a34-44c2-bd2d-a3398199bf17.png)

13. Putting It All Behind DNS: Setting up HTTPS and a Route 53 Record

14. **LAB** - Creating Route 53 Records (Alias) to Route Traffic to an ALB Using Terraform

![image](https://user-images.githubusercontent.com/93227818/202844419-c61eb6b0-fbb9-4019-bd3f-747c40865481.png)

15. Terraform Outputs and Terraform Graph

![image](https://user-images.githubusercontent.com/93227818/202845619-643135ab-e9af-4ffa-b851-19dd05b2c389.png)

