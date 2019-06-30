# Google storage: CORS configuration

At the bottom of your window, a shell terminal will be shown, where gcloud and gsutil are already available. Execute the command shown below. It creates a json-file which is needed to setup the cors-configuration for your bucket. This configuration will allow every domain to access your bucket using XHR-Requests in the browser

```
$ echo '[{"origin": ["*"],"responseHeader": ["Content-Type"],"method": ["GET", "HEAD"],"maxAgeSeconds": 3600}]' > cors-config.json
$ gsutil cors set cors-config.json gs://YOUR_BUCKET_NAME
# check my bucket
$ gsutil cors get gs://YOUR_BUCKET_NAME
```

[Related link](https://bitmovin.com/docs/encoding/faqs/how-do-i-set-up-cors-for-my-google-cloud-storage-bucket)


