# Multiple vulnerabilities in Amazon Web Services

### 1st is CWE-918: Server-Side Request Forgery (SSRF).
It is possible in https://s3.console.aws.amazon.com/s3/batchOpsServlet-proxy when sending POST-request. 
Vulnerable parameter is "region"  in JSON string of POST data. 

![Request](request.png)

and request from Amazon server:

![Request from Amazon](Response.png)

(Header "x-amzn-console-xff" and ngrok account name was hidden)

We can replace valid value (us-east-1,eu-west-1 or any other) to our payload and 2 special characters for bypass concatenating other strings (".s3", ."amazonaws.com/" and name of bucket)  to our payload . We need add "@" in start of our payload and "/" in end of our payload(for example: "@example-domain.com/"). It allows us to exploiting SSRF vulnerability. 
For example 2 request for scan local ports:

![Example scan port 24 \(closed\)](Example scan port 24 \(closed\).png)
