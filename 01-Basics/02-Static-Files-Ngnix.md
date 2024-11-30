# Serve static files using an Nginx server

---

### **1. Prepare Your Static Files**
1. Create a directory to hold your static files:
   ```bash
   mkdir static-site
   cd static-site
   ```
2. Add your `index.html` file and other assets:
   - **index.html**:
     ```html
     <!DOCTYPE html>
     <html lang="en">
     <head>
         <meta charset="UTF-8">
         <meta name="viewport" content="width=device-width, initial-scale=1.0">
         <title>Static Site</title>
     </head>
     <body>
         <h1>Welcome to My Static Site!</h1>
         <p>This site is served using Nginx and Docker.</p>
     </body>
     </html>
     ```

---

### **2. Pull the Nginx Docker Image**
Make sure you have Docker installed. Pull the official Nginx image:
```bash
docker pull nginx
```

---

### **3. Run the Nginx Container**
Run the Nginx container and bind your static site directory to the container’s default web root `/usr/share/nginx/html`.

```bash
docker run -d -p 8080:80 -v $(pwd):/usr/share/nginx/html nginx
```

- **`-d`**: Runs the container in detached mode.
- **`-p 8080:80`**: Maps port 8080 on your host to port 80 in the container.
- **`-v $(pwd):/usr/share/nginx/html`**: Mounts your current directory as the container’s web root.

---

### **4. Access Your Static Site**
- Open your browser and navigate to `http://localhost:8080`.
- You should see your static website with the message:
  > Welcome to My Static Site!  
  > This site is served using Nginx and Docker.

---

### **5. Stop and Remove the Container (Optional)**
If you want to stop the container:
1. List running containers:
   ```bash
   docker ps
   ```
2. Stop the container:
   ```bash
   docker stop <container_id>
   ```
3. Remove the container:
   ```bash
   docker rm <container_id>
   ```

---