- Amazon Machine Images are unique to a region.
Template can't be deployed in any other region because another region would use a different AMI ID.

- S3 naming problem (needs tto be unique)

# DO:

- Attempt to make a template so you don't explicitly define any naming.

- Allow CloudFormation to create the physical resource name rather than explicitly defining it. 

- Where possible try not to use anything regionally specific, such as key names or AMIids.

- Where possible, attempt to utilize features of CloudFormation which allow you to dynamically reference things.

Use SSM parameters 