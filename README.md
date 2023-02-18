gcloud builds submit --tag gcr.io/plotly-dash-378116/ploty-dash  --project=plotly-dash-378116

gcloud run deploy --image gcr.io/plotly-dash-378116/ploty-dash --platform managed  --project=git --allow-unauthenticated


$ gunicorn ploty:server — bind=0.0.0.0:8050