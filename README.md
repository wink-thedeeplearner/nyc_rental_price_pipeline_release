# Release of ML Pipeline for Short-Term Rental Prices in NYC

## Project Overview
You are working for a property management company renting rooms and properties for short periods of time on various rental platforms. 

- `Objective`: To estimate the typical price for a given property based  on the price of similar properties. 
- `Requirements`: Your company receives new data in bulk every week. The model needs to be retrained with the same cadence, necessitating an end-to-end pipeline that can be reused.

For in-depth explanations and step-by-step rationales on building the ML Pipeline before this release, refer to the following repo:
https://github.com/wink-thedeeplearner/udacity_ml_devops/tree/main/project_2_reproducible_model_workflow/MLPipeline_NYC_Rental_Price_Predictor

## Instructions 
Run the release using mlflow without any other pre-requisite. 

To train the model on a new sample of data (`new_sample_data.csv`) that your company received, place the new sample data in the following directory:
`components/get_data/data/`
> mlflow run https://github.com/wink-thedeeplearner/nyc_rental_price_pipeline_release.git \
             -v [the version you want to use, like 1.0.0] \
             -P hydra_options="etl.sample='new_sample_data.csv'"

In this pipeline release, a new sample of data (`sample2.csv`) is already in `components/get_data/data/`.
To train the model on this new data, run the following command:
```
mlflow run https://github.com/wink-thedeeplearner/nyc_rental_price_pipeline_release.git \
             -v 1.0.0 \
             -P hydra_options="etl.sample='sample2.csv'"
```

