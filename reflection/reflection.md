Which cloud provider did you choose, and why?
I chose AWS Bucket because I had terraform already set up from a prior assignment and it is very easy to make on aws. it is also free.

What resource did you create?
S3 bucket named anguun-terraform-lab-bucket in us-west-2 (Oregon) and a public access block that keeps the bucket private.

What does the provider block do in Terraform?
tells Terraform which cloud to work with and how to connect to it. Sets the provider to AWS and the region to us-west-2, and terraform init downloads the AWS plugin for it.

What is the purpose of the resource block?
It defines the thing I want Terraform to create. My resource block describes the S3 bucket and its name, and Terraform works out how to make it.

Why should you review terraform plan before running terraform apply?
The plan previews what Terraform is about to create, change, or delete. This allows you to double check to prevent error updates.

What happened when you ran terraform destroy?
Terraform showed the 2 resources it would delete, I typed yes, and it removed the bucket and the public access block. I refreshed the S3 console and the bucket was gone.

What error or challenge did you encounter, if any, and how did you troubleshoot it?
My first terraform plan said “No changes” even though I expected 2 resources. I ran dir and saw main.tf was 0 bytes, so my code never saved. I wrote the file again from PowerShell, confirmed it with Get-Content main.tf, and the plan then showed 2 to add.

What is one benefit of using Infrastructure as Code instead of manually creating cloud resources?
I created, deleted, and recreated the same bucket with the same commands and got the same result every time, and the code can go in GitHub
