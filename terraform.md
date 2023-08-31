# Terraform 

### Remove state wildcard
```
terraform state rm $(terraform state list | grep <key word>)
```
