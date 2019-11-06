# Quality metrics

https://github.com/EduardoVernier/dynamic-projections/blob/master/Metrics/template.ipynb

The code for the metrics is located in a notebook called `template.ipynb`. For each dataset we use a tool called Papermill to instantiate a new notebook from the template. The two parameters that are needed are the output notebook path (remember to change name to dataset_id) and the list of output/projection files we want to analyse. This is the code that generates the analysis for the gaussians dataset:
```
papermill Metrics/template.ipynb ./Metrics/gaussians.ipynb --log-output -p projection_paths 'Output/gaussians-AE_10f_10f_2f_20ep.csv Output/gaussians-AE_10f_2f_20ep.csv Output/gaussians-tsne_s1_70p.csv Output/gaussians-tsne_s4_70p.csv Output/gaussians-dtsne_70p_0-1l.csv Output/gaussians-pca_s1.csv Output/gaussians-pca_s4.csv'
```
The results are written in a csv file that goes into the https://github.com/EduardoVernier/dynamic-projections/tree/master/Metrics/results.
