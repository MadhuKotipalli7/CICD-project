
---

## 📌 Technologies Used

| Category       | Tools & Services                                       |
|----------------|--------------------------------------------------------|
| CI/CD          | Git, GitHub, Jenkins, Maven                            |
| Configuration  | Ansible                                                |
| Containerization | Docker, Docker Hub                                   |
| Orchestration  | Kubernetes (EKS), kubectl, eksctl                      |
| Web Server     | Apache Tomcat                                          |
| Cloud Provider | AWS (EC2, EKS, ELB, Route 53, IAM, Security Groups)    |

---

## 🔧 Pipeline Stages

### 1. 🔹 Source Code Management
- Git installed on EC2.
- Cloned a sample form-filling web app repo from GitHub.
- Made changes and committed back to GitHub.

### 2. 🔹 Jenkins Setup & Maven Build
- Jenkins installed on EC2 (Java 21 + Maven).
- Configured GitHub integration, Maven jobs, environment variables.
- Jenkins polls GitHub for changes and builds `.war` files.

### 3. 🔹 Tomcat Deployment on EC2
- Tomcat installed and configured for GUI management.
- Jenkins job deployed `.war` to Tomcat automatically.
- SCM polling ensures automatic deployment on every Git push.

### 4. 🔹 Docker Integration
- Docker installed on EC2.
- Created custom Dockerfile for Tomcat with webapps content.
- Jenkins deploys `.war` inside a Docker container on port 8083.

### 5. 🔹 Ansible + Docker Hub
- Ansible configured on EC2 (also used as K8s master).
- Playbooks created to build, tag, and push Docker images to Docker Hub.
- Jenkins CI job triggers Ansible post-build.

### 6. 🔹 Kubernetes Deployment (EKS)
- EKS cluster provisioned via `eksctl` and `kubectl`.
- Kubernetes manifests written (`deployment.yml`, `service.yml`).
- Jenkins CD job triggers Ansible to deploy updated Docker images to EKS.

### 7. 🔹 Route 53 DNS Mapping
- Load Balancer DNS mapped to a custom domain via Route 53.
- Application successfully accessible via friendly domain name.

---

## ✅ Final Workflow


---

## 💡 Key Takeaways

- Built a full CI/CD pipeline with modern DevOps tools.
- Automated container builds, image pushes, and K8s deployments.
- Implemented real-time integration between GitHub, Jenkins, Docker, and AWS.
- Gained hands-on experience with provisioning, scripting, and debugging.
- Understood production-level deployment and automation strategies.

---

## 📸 Screenshots & Architecture Diagram

> (Add screenshots of Jenkins pipelines, Docker images, K8s dashboard, and Route 53 DNS here.)

---

## 🌐 Live Access

> (Add your Route 53-based domain name or public IP here if accessible)

---

## 🤝 Connect with Me

If you're interested in DevOps, CI/CD, or want to collaborate on similar cloud-native projects, feel free to connect!

**LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/your-profile)

---

## 📁 Folder Structure (Optional)


---

## 🏁 Conclusion

This project demonstrates my ability to design, automate, and deploy scalable applications using modern DevOps and cloud technologies. It serves as a blueprint for production-grade CI/CD pipelines and cloud-native deployment on AWS.

---

