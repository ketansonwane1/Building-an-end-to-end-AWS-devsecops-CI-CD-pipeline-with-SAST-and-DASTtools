
# 🛠️ **End-to-End AWS DevSecOps CI/CD Pipeline with SAST & DAST Tools** 🔒

## 🚀 **Project Overview**

In today's fast-paced software development environment, security should be integrated at every stage of the DevOps pipeline. This project creates an **automated, secure CI/CD pipeline on AWS**, integrating essential **DevSecOps** tools like **SonarQube (SAST)**, **OWASP ZAP (DAST)**, and **Trivy (Container Security)**.

The goal of the project is to enhance **software security** and **efficiency** by embedding continuous security testing throughout the software development lifecycle. This project showcases how security testing can be seamlessly incorporated into the **DevOps workflow** for more secure applications.

---

## 📌 **Key Features**

- **Automated Code Analysis**: Uses **SonarQube** for **Static Application Security Testing (SAST)** to detect vulnerabilities early.
- **Runtime Vulnerability Scanning**: **OWASP ZAP** for **Dynamic Application Security Testing (DAST)**.
- **Container Security**: **Trivy** scans **Docker containers** for vulnerabilities before deployment.
- **CI/CD Pipeline**: Fully automated pipeline leveraging **AWS CodePipeline**, **AWS CodeBuild**, **AWS CodeDeploy**, and **Jenkins**.
- **Security Reports**: Continuous security monitoring and detailed reports to ensure compliance with best practices.

---

## 🛠️ **Tools and Technologies**

- **AWS Services**: EC2, S3, IAM, VPC, CodePipeline, CodeBuild, CodeDeploy
- **SonarQube** (SAST) - Static Code Analysis for Vulnerabilities
- **OWASP ZAP** (DAST) - Dynamic Runtime Security Testing
- **Trivy** - Container Security Scanner
- **Jenkins** - Automation Server for CI/CD Pipelines
- **Docker** - Containerization

---

## 🌐 **Architecture Overview**

![AWS DevSecOps Architecture](https://link-to-your-image.com)

**This diagram illustrates the flow of the CI/CD pipeline, integrating security checks and continuous deployment**.

---

## 🏗️ **Setup Instructions**

### Prerequisites

Ensure the following before setting up the pipeline:

- **AWS Free Tier Account** (12-month free access)
- **Ubuntu (20.04+)** or **Amazon Linux**
- **Minimum Hardware**: 8GB RAM, Dual-Core Processor

---

### 1️⃣ **Setting Up AWS EC2 Instance**

1. **Create an AWS Free Tier Account** (if not already done).
2. **Launch EC2 Instance**:
   - Choose **Ubuntu Server 22.04 LTS** (or Amazon Linux).
   - Use a **t2.micro** instance (Free Tier eligible).
   - Open necessary ports: **SSH, HTTP, HTTPS**.
3. **Access the EC2 instance** via SSH using the private key.

---

### 2️⃣ **Installing and Configuring Security Tools**

#### 🔐 **SonarQube (SAST)**

- **Purpose**: Scans the source code for bugs, vulnerabilities, and code smells.
- **Installation**: Follow [SonarQube Setup Guide](https://docs.sonarqube.org/).

#### 🕵️ **OWASP ZAP (DAST)**

- **Purpose**: Scans the application during runtime for security vulnerabilities.
- **Installation**: Follow [OWASP ZAP Setup Guide](https://www.zaproxy.org/).

#### 🛡️ **Trivy (Container Security)**

- **Purpose**: Scans Docker containers for known vulnerabilities.
- **Installation**: Follow [Trivy Setup Guide](https://github.com/aquasecurity/trivy).

---

### 3️⃣ **Setting Up Jenkins**

- **Installation**: Follow the [Jenkins Setup Guide](https://www.jenkins.io/doc/book/installing/).
- **Pipeline Setup**:
  - Install **SonarQube**, **OWASP ZAP**, and **Trivy** plugins in Jenkins.
  - Configure the Jenkins pipeline to trigger **SonarQube** for static analysis and **OWASP ZAP** for runtime scanning.

---

### 4️⃣ **Building the CI/CD Pipeline**

- **AWS CodePipeline** automates the build and deployment process.
- Integrate **SonarQube** analysis as part of the build process.
- **OWASP ZAP** runs automated security scans post-deployment.
- **Trivy** scans Docker images during the build process to ensure secure containers.

---

## 🖼️ **Screenshots**

#### 🖥️ **Infrastructure Diagram**
![image](https://github.com/user-attachments/assets/639655b7-bdbd-415a-b613-33226e548fba)
![image](https://github.com/user-attachments/assets/24c8e064-4a8e-49f7-8c09-205a32d9a7ea)


#### 🖥️ **EC2 Instance**

![image](https://github.com/user-attachments/assets/bac6d7a3-5283-46c9-837a-91a7ccef0a7b)
![image](https://github.com/user-attachments/assets/3352ad8c-cf60-4cf8-a2b8-a5900bf71d33)
![image](https://github.com/user-attachments/assets/0e6122dc-aed7-45d0-833e-ac2b07fd5e3d)


#### ⚙️ **SonarQube Dashboard**

![image](https://github.com/user-attachments/assets/b5feaecc-4969-4186-a48b-0ade262075c6)
![image](https://github.com/user-attachments/assets/cec974b1-5725-4d28-9e7f-e4056f870926)

#### 🔍 **OWASP ZAP Security Scan**

![OWASP ZAP](https://link-to-your-image.com)

#### ⚡ **Jenkins Pipeline**

![image](https://github.com/user-attachments/assets/e4898409-0112-4174-8f93-a93473e1cd05)
![image](https://github.com/user-attachments/assets/c2e593c8-a189-4a15-88e5-768cc3bf1843)
![image](https://github.com/user-attachments/assets/af6177c0-2f57-47a0-8af9-6524858d26a0)
![image](https://github.com/user-attachments/assets/30bb753d-a05e-4bb8-a5b7-a6be106b696d)


#### ⚡ **Final Result**

![image](https://github.com/user-attachments/assets/9b396846-8d60-4fb2-ac9c-8dd580e10e0f)


---

## 🚀 **CI/CD Pipeline Flow**

1. **Push Code**: Developers commit code to **GitHub**.
2. **SonarQube Scan**: Code is analyzed for vulnerabilities.
3. **Build & Test**: Code is compiled and tested with **AWS CodeBuild**.
4. **OWASP ZAP Scan**: Application is scanned for runtime security issues.
5. **Trivy Scan**: Docker containers are scanned for vulnerabilities.
6. **Deployment**: **AWS CodeDeploy** ensures a secure deployment to production.

---

## 🔒 **Security and Compliance**

1. **Continuous Monitoring**: Implement continuous security monitoring to detect vulnerabilities as soon as they arise.
2. **Compliance Reports**: Automatically generate security reports for compliance and auditing.
3. **Tool Updates**: Regularly update security tools to reduce risk.

---

## 🔧 **Future Enhancements**

- **Automated Rollbacks**: Roll back to a safe state if critical vulnerabilities are found.
- **AI-based Detection**: Integrate AI/ML tools for real-time threat detection.
- **Multi-cloud Support**: Extend the pipeline to support **multi-cloud environments** for enhanced resilience.

---

## 📜 **References**

1. [AWS Official Documentation](https://aws.amazon.com/)
2. [SonarQube Documentation](https://docs.sonarqube.org/)
3. [OWASP ZAP GitHub](https://github.com/zaproxy/zaproxy)
4. [Trivy GitHub](https://github.com/aquasecurity/trivy)
5. [DevSecOps Overview](https://medium.com/@pardhikhush/devsecops-end-to-end-cicd-project-devops-engineer-github-sonarqube-owasp-trivy-docker-8fe72265f7ea)

---

## 📄 **License**

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
