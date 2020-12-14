## About Repositoty-Pipeline

basel/repository-pipeline is a Laravel Package That make repository layer for each model and target QueryFilters/ModelName Folder to get pipelines filters and apply filters in repository.

## Requirements

- PHP >= 8.0.0
- Laravel >= 8.0

## Code Examples

```php
use Basel\RepositoryPipeline\Repository;

$filters = ['id'=>3,'active'=>true];

$products = Repository::get(Product::class, $filters, $perPage = 1);

$product= Repository::find(Product::class, $filters);

$isUpdated = Repository::find($product,['name'=>'new name','description'=>'new description']);

$isDeleted = Repository::find($product);
```