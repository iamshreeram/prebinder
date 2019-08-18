# prebinder
A workflow engine to create runnable documentation

## About 
`prebind` is a workflow engine and controller that is powered by Azure for creating runnable documentation. 

## Current setup
![Earlier architecuture](./static/before.png)

## Workflow engine 
1. As soon as the user code gets merged in `github`, a webhook to work flow engine is triggered 
2. WFlow kicks in the process of checking the difference in `markdown` files
3. Based on delta, WFlow triggers the process to parse the `markdown` and create `jupyter notebook`  
4. Once the `notebook` is created, Controller checks with user / `wflow.yml` to spin a binder instance in `GCP` or `Azure`

![Next Gen Architecture](./static/after.png)

## Output of `prebinder`
* Getting Started with pandas in 10 minutes
    * [Azure](https://prebinders-iamshreeram.notebooks.azure.com/j/notebooks/10min.ipynb)
    * [Binder](https://hub-binder.mybinder.ovh/user/iamshreeram-pandas-binder-s2i014jv/notebooks/build/jupyter/getting_started/10min.ipynb)