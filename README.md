# shipping-go

## hello-api
Demo continous delivery pipeline

# Dependencies

- Go version 1.19

# Setup

gcloud iam service-accounts add-iam-policy-binding mx-sec584@appspot.gserviceaccount.com --member 	'hello-api@mx-sec584.iam.gserviceaccount.com' --role roles/iam.serviceAccountUser

gcloud iam service-accounts add-iam-policy-binding \
    mx-sec584-compute@developer.gserviceaccount.com \
    --member hello-api@mx-sec584.iam.gserviceaccount.com \
    --role roles/iam.serviceAccountUser