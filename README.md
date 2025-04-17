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
![Screenshot 2025-04-17 131340](https://github.com/user-attachments/assets/4d85d562-c067-4428-9a9e-2eb060ffaf84)
![Screenshot 2025-04-17 131323](https://github.com/user-attachments/assets/779ce68a-00e3-4abc-9e20-014ed9c44e2b)

