# Auto feature generation

The script within this WhizzML package extends a given dataset
generating automatically new features. This features come from
applying unsupervised models to the dataset. Currently, the generated
fields come from:

* cluster batch centroid
* anomaly score
* topic distribution
* PCA batch projection

The user can configure the options of the generated unsupervised
models, or he can leave the inputs blank for using 1-Click
unsupervised models.

The **inputs** for the script are:

* `dataset-id`: (dataset-id) Dataset ID for the train dataset to be extended
* `test-dataset-id`: (string) **optional** Dataset ID for the test dataset to be extended (e.g. dataset/dataset/5d1c7f7adb8b1d72680002f4)
* `cluster-params`: (map) **optional** Params of the cluster model. Leave blank for default 1-Click cluster
* `anomaly-params`: (map) **optional** Params of the anomaly detector. Leave blank for default 1-Click anomaly detector
* `topic-params`: (map) **optional** Params of the topic model. Leave blank for default 1-Click topic model
* `pca-params`: (map) **optional** Params of the PCA model. Leave blank for default 1-Click PCA

The **outputs** for the script are:
* `extended-dataset-train`: (dataset-id) Dataset ID for the extended train dataset
* `extended-dataset-test`: (dataset-id) Dataset ID for the extended test dataset
