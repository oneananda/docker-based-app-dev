
### **Example: Running Nginx**

1. Pull the Nginx image from Docker Hub:
   ```bash
   docker pull nginx
   ```

2. Run the Nginx container:
   ```bash
   docker run -d -p 8085:80 nginx
   ```

3. Access the Nginx server in your browser at `http://localhost:8085`. [Nginx server Screenshot](https://github.com/oneananda/docker-based-app-dev/blob/main/01-Basics/Images/01-running-nginx-server.png)

4. Stop and remove the container:
   ```bash
   docker stop <container_id>
   docker rm <container_id>
   ```

---