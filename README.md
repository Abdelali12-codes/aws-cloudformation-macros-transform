# aws-cloudformation-macros-transform

## create the transform

1. Package the Macro CloudFormation template

```
aws cloudformation package \
    --template-file template.yaml \
    --s3-bucket <your bucket name here> \
    --output-template-file packaged.yaml
```

2. Deploy the packaged CloudFormation template to a CloudFormation stack:

```
aws cloudformation deploy \
    --stack-name Count-macro \
    --template-file packaged.yaml \
    --capabilities CAPABILITY_IAM
```

## References

1. https://aws.amazon.com/blogs/mt/deep-dive-on-aws-cloudformation-macros-to-transform-your-templates/
2. https://aws.amazon.com/blogs/mt/use-aws-cloudformation-macros-to-create-multiple-resources-from-a-single-resource-definition/
