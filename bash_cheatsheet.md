
## Loops 
### Create 20 new files in a named S3 bucket

``` bash #!/bin/bash
for i in {0..20}
do
  aws s3api put-object --bucket my_bucket_name --key another_test$i
done
```

