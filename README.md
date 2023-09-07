# terraform-provider-macaddress
Generates random locally administered unicast MAC address

# Use case (Under development, the code below is not corrrect for this repo)
```hcl
terraform {
  required_providers {
    macaddress = {
      source = "ivoronin/macaddress"
      version = "0.3.0"
    }
  }
}

resource "macaddress" "example_address" {
}

// Terraform Mikrotik Provider - https://github.com/ddelnano/terraform-provider-mikrotik
resource "mikrotik_dhcp_lease" "example_lease" {
  address    = "10.0.0.10"
  macaddress = upper(macaddress.example_address.address)
  comment    = "Example DHCP Lease"
}
```
