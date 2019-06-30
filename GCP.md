https://bitmovin.com/docs/encoding/faqs/how-do-i-set-up-cors-for-my-google-cloud-storage-bucket

CORS configuration

echo '[{"origin": ["*"],"responseHeader": ["Content-Type"],"method": ["GET", "HEAD"],"maxAgeSeconds": 3600}]' > cors-config.json
gsutil cors set cors-config.json gs://YOUR_BUCKET_NAME

# check my bucket
gsutil cors get gs://YOUR_BUCKET_NAME
