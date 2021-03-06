# CORS Use\-case Scenarios<a name="cors-policy-use-case-scenarios"></a>

The following are example scenarios for using CORS:

+ Scenario 1: Suppose you are distributing live streaming video in an AWS Elemental MediaStore container named *LiveVideo*\. Your users load the video manifest endpoint `http://livevideo.mediastore.ap-southeast-2.amazonaws.com` from a specific origin like `www.example.com`\. You want to use a JavaScript video player to access videos that are originated from this container via unauthenticated `GET` and `PUT` requests\. A browser would typically block JavaScript from allowing those requests, but you can set a CORS policy on your container to explicitly enable these requests from `www.example.com`\.

+ Scenario 2: Suppose you want to host the same live stream as in Scenario 1 from your AWS Elemental MediaStore container, but want to allow requests from any origin\. You can configure a CORS policy to allow wildcard \(\*\) origins, so that requests from any origin can access the video\.