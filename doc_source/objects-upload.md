# Uploading an Object<a name="objects-upload"></a>

You can upload objects \(up to 10 MB each\) to a container or to a folder within a container\. To upload an object to a folder, you specify the path to the folder\. If the folder already exists, AWS Elemental MediaStore stores the object in the folder\. If the folder doesn’t exist, the service creates it, and then stores the object in the folder\. For more information about folders, see [Working with Folders in AWS Elemental MediaStore](folders.md)\.

You can use the AWS Elemental MediaStore console or the AWS CLI to upload objects\. 

**Note**  
Object file names can contain only letters, numbers, periods \(\.\), underscores \(\_\), tildes \(\~\), and hyphens \(\-\)\. 

**To upload an object \(console\)**

1. Open the AWS Elemental MediaStore console at [https://console\.aws\.amazon\.com/mediastore/](https://console.aws.amazon.com/mediastore/)\.

1. On the **Containers** page, choose the name of the container\. The details panel for the container appears\.

1. Choose **Upload object**\.

1. For **Target path**, type a path for the folders\. For example, premium/canada\. If any of the folders in the path that you specify don’t exist yet, the service creates them automatically\.

1. In the **Object** section, choose **Browse**\.

1. Navigate to the appropriate folder, and choose one object to upload\.

1. Choose **Open**, and then choose **Upload**\.
**Note**  
If a file with the same name already exists in the selected folder, the service replaces the original file with the uploaded file\.

**To upload an object \(AWS CLI\)**

+ In the AWS CLI, use the **put\-object** command\.

  Example:

  ```
  aws mediastore-data --region us-west-2 put-object --endpoint=https://aaabbbcccdddee.data.mediastore.us-west-2.amazonaws.com --body=README.md --path=/test/document/README3.md
  ```

  Example return value:

  ```
  {
      "ContentSHA256": "74b5fdb517f423ed750ef214c44adfe2be36e37d861eafe9c842cbe1bf387a9d",
      "StorageClass": "TEMPORAL",
      "ETag": "af3e4731af032167a106015d1f2fe934e68b32ed1aa297a9e325f5c64979277b"
  }
  ```