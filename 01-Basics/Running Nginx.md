
### **Example: Running Nginx**

1. Pull the Nginx image from Docker Hub:
   ```bash
   docker pull nginx
   ```

2. Run the Nginx container:
   ```bash
   docker run -d -p 8085:80 nginx
   ```

3. Access the Nginx server in your browser at `http://localhost:8085`.

4. Stop and remove the container:
   ```bash
   docker stop <container_id>
   docker rm <container_id>
   ```

---