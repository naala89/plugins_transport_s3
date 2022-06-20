# Transport S3

Transport for ApiOpenStudio output to an AWS S3 bucket

# Adding to your project

## Composer

    $ composer require apiopenstudio/transport_s3

# Configuration

Add a remote output processor to your resource, i.e.

    output:
        -
            processor: xml_remote
            id: example XML Remote output
            filename: example.xml
            transport: transport_s3
            parameters:
                key: my_aws_s3_bucket_key
                secret: my_aws_s3_bucket_secret
                bucket: my_bucket_name
                version: version
                region: my_bucket_region (optional)
        - 
            response

## Parameters

### Required

- key - AWS S3 key
- secret - AWS S3 secret
- bucket - AWS S3 bucket name
- version - latest|version

### Optional

- region - AWS S3 bucket region

# Further information

See [FlySystem documentation][flysystem-docs] and
[The League GitHub][flysystem-github] for more details.

[flysystem-github]: https://github.com/thephpleague/flysystem-aws-s3-v3

[flysystem-docs]: https://flysystem.thephpleague.com/docs/adapter/aws-s3-v3/
