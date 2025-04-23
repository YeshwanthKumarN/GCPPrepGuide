# GCPPrepGuide
A centralized repository for all my GCP learning materials.

17/04/2025

Deploying vault agent in cloud run https://github.com/kelseyhightower/serverless-vault-with-cloud-run
Monitor CloudRun using DynaTrace https://docs.dynatrace.com/docs/ingest-from/google-cloud-platform/gcp-integrations/cloudrun

23/04/2025
1. Deploy a local image to cloudrun
[gcloud run deploy nginx \
  --image nginx:latest \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated]

  Failed. Details: Revision 'nginx-00002-lmz' is not ready and cannot serve traffic. The user-provided container failed to start and listen on the port defined provided by the PORT=8080 environment variable within the allocated timeout. This can happen when the container port is misconfigured or if the timeout is too short. The health check timeout can be extended. Logs for this revision might contain more information. Logs URL: Open Cloud Logging  For more troubleshooting guidance, see https://cloud.google.com/run/docs/troubleshooting#container-failed-to-start 

2. Proxy a remote jfrog public repository and deploy the image to cloud run

3. Explore PSC for jfrog
   		Problem: Jfrog Docker Artifactory repo was hosted in GKE - private VPC, and the UI's exposed using Internal ALB. How to integrate/proxy JFrog using Artifact Registry Remote repo option.
   		Solution: Step 1: Understand how PSC works for managed services https://cloud.google.com/vpc/docs/private-service-connect
