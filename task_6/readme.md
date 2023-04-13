# task 6
## the aim was to learn *what Infrastructure as a Code is*, *to write scripts that automate resource creation in GCP* and how to *create resources in GCP with a few commands* 🤓📚
1. first of all I opened the Cloud Shell and checked the version of Terraform using the command:
```
terraform version
```
2. in the next step I have created a *main.tf*, where I pasted the code:
```
provider "google" {

  project = "mindful-hall-377614"

  region  = "us-central1"

  zone    = "us-central1-c"

}





resource "google_compute_instance" "dare-id-vm" {

  name         = "dareit-vm-tf"

  machine_type = "e2-medium"

  zone         = "us-central1-a"



  tags = ["dareit"]



  boot_disk {

    initialize_params {

      image = "debian-cloud/debian-11"

      labels = {

        managed_by_terraform = "true"

      }

    }

  }



  network_interface {

    network = "default"



    access_config {

      // Ephemeral public IP

    }

  }

}
```
3. where in above code the line with *project name* is individual and depends on our project name in Google Cloud 😄
4. after that, I wrote the below code in my terminal in Cloud Shell:
```
terraform init
```
5. next one was: 
```
terraform plan
```

to check the plan of the terraform
6. after that, it asked me to *authorize Cloud Shell to perform actions using your credentials* (thank’s to this terraform will now rely on your credentials in your project in order to be able to create resources)
7. next, I have used the command:
```
terraform apply
```
where terraform once again showed me the plan (as in previous step with the command *terraform plan*, I confirmed it by **yes** becasue I wanted it to apply)
8. and 🎉 it worked
9. in the next step I went to *Compute Engine* --> **VM Instances** in the navigation panel in Google Cloud 









https://storage.googleapis.com/34e09d96e9e9ef94-bucket-tfstate/index.html
