# AutoML NLP payload generator

This notebook helps automate the entity extraction payload for AutoML NLP, see https://cloud.google.com/natural-language/automl/docs/prepare#entity-extraction for more details.  

The goal of the script is to take a series of un-annotated PDFs, generate the required jsonl files, and generate the payload CSV.  From there, you need to create a new dataset within AutoML NLP for Entity Extraction, and import the CSV from the cloud storage bucket.

Because these are for un-annotated PDFs, you'll need to do the annotation step via the UI to generate the labels and associated annotated document sections, see https://cloud.google.com/natural-language/automl/docs/datasets#label-items for more information.

This is designed to run in an AI platform notebook with a service account that has permissions to the GCS bucket that contains the files you wish to annotate.  Please note: right now the GCS bucket needs to be regional and in us-central1 for AutoML NLP.
