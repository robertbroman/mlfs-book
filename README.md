# Lab 1
We have implemented a pipeline for predicting the levels of PM2.5 in the air in Trondheim Norway. This using public available particle sensor data and weather data. It runs daily by fetching new weather forecasts to predict the PM2.5 levels and creates both a forecast and a hindcast plot. Each particle sensor in the city has its own trained model.

To run the pipeline, first one needs to manually run the feature backfill notebook (1_air_quality_feature_backfill.ipynb) using historical particle sensor data downloaded from https://aqicn.org/. Then one has to run the training pipeline (3_air_quality_training_pipeline.ipynb) manually for that same location. Lastly add all the used locations to locations.json and the Github Actions will automatically run the feature pipeline and batch inference daily.

The dashboard is available at https://robertbroman.github.io/mlfs-book/air-quality/