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











https://storage.googleapis.com/34e09d96e9e9ef94-bucket-tfstate/index.html
