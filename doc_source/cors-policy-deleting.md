# Deleting a CORS Policy<a name="cors-policy-deleting"></a>

Cross\-origin resource sharing \(CORS\) defines a way for client web applications that are loaded in one domain to interact with resources in a different domain\. Deleting the CORS policy from a container removes permissions for cross\-origin requests\.

**To delete a CORS policy \(console\)**

1. Open the AWS Elemental MediaStore console at [https://console\.aws\.amazon\.com/mediastore/](https://console.aws.amazon.com/mediastore/)\.

1. On the **Containers** page, choose the name of the container that you want to delete the CORS policy for\.

   The container details page appears\. 

1. In the **Container CORS policy** section, choose **Edit CORS policy**\.

1. Clear the text from the text box, and then choose **Save**\.

**To delete a CORS policy \(AWS CLI\)**

+ In the AWS CLI, use the `delete-cors-policy` command\.

  Example:

  ```
  aws mediastore delete-cors-policy --container-name ExampleContainer --region ap-southeast-2 --endpoint https://mediastore.ap-southeast-2.amazonaws.com/
  ```

  This command has no return value\.