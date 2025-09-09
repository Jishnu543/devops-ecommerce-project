🐳 Run Locally with Docker

Clone the repo and start services with Docker Compose:

git clone https://github.com/Jishnu543/devops-ecommerce-project.git
cd devops-ecommerce-project/source
docker-compose up -d


Access the app at 👉 http://localhost:8080

☁️ Deploy on AWS with Terraform + EKS

Initialize and apply Terraform:

cd terraform
terraform init
terraform plan
terraform apply


Configure kubectl for your new cluster:

aws eks update-kubeconfig --region ap-south-1 --name devops-eks


Apply Kubernetes manifests:

kubectl apply -f k8s-manifests/


Access via LoadBalancer or Route53 custom domain.

🔄 CI/CD Pipeline

GitHub Actions handles build/test/deploy of microservices.

ArgoCD continuously syncs Kubernetes cluster with GitHub repo.

Example pipeline (ci-cd/ci.yaml) includes:

Build Docker image

Push to DockerHub

Deploy to EKS

📘 Credits

Source code: ultimate-devops-project-demo-source-code

Documentation: ultimate-devops-project-aws

Customized and implemented by Jishnu ✨

📌 Roadmap

 Add monitoring with Prometheus + Grafana

 Add logging with ELK stack

 Expand CI/CD to multi-service workflows

⭐ If you like this project, don’t forget to star the repo!


---

⚡ This will instantly make your repo look professional — anyone visiting will know:  
- App source is inside `source/`.  
- You implemented **infra + automation**.  
- How to run locally & deploy on AWS.  

👉 Do you want me to also generate the **GitHub Action workflow (`ci.yaml`)** so your repo has a 
