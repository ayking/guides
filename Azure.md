### List all assigned roles

```sh
$resource = (Get-AzureRmResource | Select-Object ResourceId).ResourceId 

foreach($item in $resource){
    $role += Get-AzureRmRoleAssignment -Scope $item 
}

$role | Export-CSV role.csv
```sh
