
DevOps Task 7: Monitoring System Resources with Netdata on Windows
Keep an eye on system performance using Netdata inside a Docker container on Windows. With real-time metrics such as CPU usage, memory consumption, disk I/O, and container activity, this setup offers a powerful way to visualize system health.
Tools Required
- Netdata – A free, open-source monitoring tool
- Docker Desktop – Runs Netdata in a containerized environment

Installation & Setup
1. Install Docker Desktop
- Download Docker Desktop from Docker's official site.
- Follow installation steps and ensure Docker is running.

2. Deploy Netdata Using Docker
- Open Command Prompt (cmd) or PowerShell and execute:docker run -d --name=netdata -p 19999:19999 netdata/netdata


3. Access the Netdata Dashboard
- Open a browser and visit:
http://localhost:19999
- You’ll be able to view real-time system metrics, including:- CPU & RAM usage
- Disk I/O performance
- Network activity
- Running Docker container statistics


4. Monitor Alerts & Charts
- Click the bell icon (top-right) to view system alerts.
- Use the search bar or sidebar to navigate different monitoring panels:- System Overview
- Memory
- Network Interfaces
- Applications (Docker, etc.)


5. Access Logs from Inside the Container
- Open a terminal (cmd, PowerShell, or Windows Terminal).
- Execute:docker exec -it netdata bash

- Navigate to the logs folder:cd /var/log/netdata

- View log files:cat error.log
cat health.log


Deliverables
- Capture a screenshot of the Netdata dashboard displaying system metrics (CPU, memory, disk, etc.).
- Confirm alert panel access and log visibility.

Additional Notes
- Ensure Docker is running before launching Netdata.
- To stop the Netdata container:docker stop netdata

- To remove the container completely:docker rm -f netdata



This version keeps the same information but improves clarity and formatting while giving it a fresh look. Let me know if you need any further refinements! 🚀
