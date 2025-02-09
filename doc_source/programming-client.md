# Creating a client<a name="programming-client"></a>

To use the [AWS SDK for Java](https://docs.aws.amazon.com/AWSJavaSDK/latest/javadoc/com/amazonaws/services/kms/package-summary.html), the [AWS SDK for \.NET](https://docs.aws.amazon.com/sdkfornet/v3/apidocs/items/KeyManagementService/NKeyManagementServiceModel.html), the [AWS SDK for Python \(Boto3\)](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/kms.html), the [AWS SDK for Ruby](https://docs.aws.amazon.com/sdk-for-ruby/v3/api/Aws/KMS/Client.html), the [AWS SDK for PHP](https://docs.aws.amazon.com/aws-sdk-php/v3/api/api-kms-2014-11-01.html), or the [AWS SDK for JavaScript in Node\.js](https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/clients/client-kms/index.html) to write code that uses the [AWS Key Management Service \(AWS KMS\) API](https://docs.aws.amazon.com/kms/latest/APIReference/), start by creating an AWS KMS client\.

The client object that you create is used in the example code in the topics that follow\.

------
#### [ Java ]

To create an AWS KMS client in Java, use the client builder\.

```
AWSKMS kmsClient = AWSKMSClientBuilder.standard().build();
```

For more information about using the Java client builder, see the following resources\.
+ [Fluent Client Builders](https://aws.amazon.com/blogs/developer/fluent-client-builders/) on the AWS Developer Blog
+ [Creating Service Clients](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/creating-clients.html) in the *AWS SDK for Java Developer Guide*
+ [AWSKMSClientBuilder](https://docs.aws.amazon.com/sdk-for-java/latest/reference/index.html?com/amazonaws/services/kms/AWSKMSClientBuilder.html) in the *AWS SDK for Java API Reference*

------
#### [ C\# ]

```
AmazonKeyManagementServiceClient kmsClient = new AmazonKeyManagementServiceClient();
```

------
#### [ Python ]

```
kms_client = boto3.client('kms')
```

------
#### [ Ruby ]

```
require 'aws-sdk-kms'  # in v2: require 'aws-sdk'

kmsClient = Aws::KMS::Client.new
```

------
#### [ PHP ]

To create an AWS KMS client in PHP, use an AWS KMS client object, and specify version `2014-11-01`\. For more information see the [KMSClient class](https://docs.aws.amazon.com/aws-sdk-php/v3/api/class-Aws.Kms.KmsClient.html) in the AWS SDK for PHP API Reference\.

```
// Create a KMSClient
$KmsClient = new Aws\Kms\KmsClient([
    'profile' => 'default',
    'version' => '2014-11-01',
    'region'  => 'us-east-1'
]);
```

------
#### [ Node\.js ]

```
const kmsClient = new AWS.KMS();
```

------