# Netdata Monitoring - Task 7

## Objective
Monitor system and Docker container metrics using Netdata.

## Tools Used
- Netdata (Docker)
- AWS EC2 (Amazon Linux 2)
- Docker

## Setup Summary
1. Launch EC2 instance and allow port 19999 in the security group.
2. Install Docker:
    ```bash
    sudo yum update -y
    sudo amazon-linux-extras install docker -y
    sudo service docker start
    ```
3. Run Netdata container:
    ```bash
    docker run -d --name=netdata -p 19999:19999 --cap-add=SYS_PTRACE --security-opt apparmor=unconfined netdata/netdata
    ```
4. Access Dashboard:  
   `http://100.27.230.8:19999`

## Screenshots

