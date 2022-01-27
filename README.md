# nyc_rental_price_pipeline_release

- Run the release using mlflow without any other pre-requisite.
$ mlflow run https://github.com/wink-thedeeplearner/nyc_rental_price_pipeline_release.git \
             -v 1.0.0 \
             -P hydra_options="etl.sample='sample2.csv'"
