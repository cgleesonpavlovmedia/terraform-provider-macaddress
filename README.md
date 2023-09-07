# terraform-provider-macaddress
Generates random locally administered unicast MAC address

# Use case (Under development)
```hcl
// Provider block coming soon...

resource "macaddress" "addr_001" {
        name = "foo"
}

output "generated_mac_addr_001" {
  value = macaddress.addr_001.address
}
output "generated_mac_addr_001_name" {
  value = macaddress.addr_001.name
}


```
