# Macaddress Provider

Generates MAC addresses

## Example Usage

```hcl
resource "macaddress" "addr_001" {
        name = "foo" // optional
}

output "generated_mac_addr_001" {
  value = macaddress.addr_001.address
}
output "generated_mac_addr_001_name" {
  value = macaddress.addr_001.name
}
```
