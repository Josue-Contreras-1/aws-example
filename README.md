gcloud builds submit --tag gcr.io/plotly-dash-378116/ploty-dash  --project=plotly-dash-378116

gcloud run deploy --image gcr.io/plotly-dash-378116/ploty-dash --platform managed  --project=git --allow-unauthenticated

gunicorn ploty:server — bind=0.0.0.0:8050
nohup gunicorn App:server — bind=0.0.0.0:3000 &

python3 -m streamlit run App.py --server.port 3000