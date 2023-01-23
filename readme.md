# After creating the main.tf and variables.tf proceed to the
# steps below

# Refresh service-account's auth-token for this session
gcloud auth application-default login

# Initialize state file (.tfstate)
terraform init 

# Check changes to new infra plan
terraform plan -var="project=hw1terraform" -var="service_account=hw1terraform-a5f48a64ab1e.json"

# apply
terraform apply -var="project=hw1terraform" -var="service_account=hw1terraform-a5f48a64ab1e.json"

# Delete infra after your work, to avoid costs on any running services
terraform destroy -var="project=hw1terraform" -var="service_account=hw1terraform-a5f48a64ab1e.json"