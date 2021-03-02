# [GeoSpock DB 3.0](https://geospock.com)  Enterprise Example Projects

[**GeoSpock DB**](https://geospock.com) is a unique, cloud-native database optimized for querying for real-world use cases, able to fuse multiple sources of Internet of Things (IoT) data together to unlock its full value, whilst simultaneously reducing complexity and cost. 

The example projects in this repository show how to integrate [**GeoSpock DB version 3.0**](https://geospock.com) with a range of popular tools as a starting point for common use cases. Please note that some of the examples presented here will not be applicable for use with GeoSpock DB Discovery – if you are a Discovery user and want to learn more, get in touch with us about GeoSpock DB Enterprise. For examples specific to Discovery, please refer to the examples in the [GeoSpock DB Discovery folder](discovery/).

### For Data Analysts

 * [**Tableau (with Kepler.gl visualizations)**](tableau-kepler/README.md) – A tutorial showing how to run GeoSpock DB queries on a (provided) example dataset using [Tableau](https://www.tableau.com), and visualize the results inside Tableau using the [Kepler.gl extension](https://github.com/keplergl/kepler.gl-tableau).
 * [**Apache Superset**](superset/README.md) – A tutorial showing how to run GeoSpock DB queries on a (provided) example dataset using [Apache Superset](https://superset.apache.org/), and visualize the results on Superset.

### For Data Scientists

 * [**Python in Jupyter notebooks**](jupyter/) – A tutorial demonstrating how to query and analyze a GeoSpock DB dataset with Python code in [a Jupyter notebook](https://jupyter.org), including map visualization with the [Kepler.gl Jupyter widget](https://github.com/keplergl/kepler.gl/tree/master/bindings/kepler.gl-jupyter).
 * [**Apache Spark™ in Zeppelin notebooks**](spark/) – A tutorial demonstrating how to integrate GeoSpock DB queries into an [Apache Spark™](https://spark.apache.org) analysis, inside a [Zeppelin notebook](https://zeppelin.apache.org). Example code is provided in both Python and Scala, and includes visualization with the [Zeppelin Leaflet plugin](https://github.com/myuwono/zeppelin-leaflet).
 * [**Apache Spark™ integration via Apache Hive™**](presto-hive-spark/) – A tutorial demonstrating how to export GeoSpock DB queries to an [Apache Hive™](https://hive.apache.org/) table, enabling high performance parallel querying of data in [Apache Spark™](https://spark.apache.org). 

### For Visualization Developers

 * [**Kepler.gl map visualization**](kepler/) – All the code and example data for a self-contained web app built around [Kepler.gl](https://kepler.gl) that visualizes the results of a GeoSpock DB query. Use as the starting point for interactive Kepler visualizations of your GeoSpock DB datasets.
 * [**CesiumJS 3D world simulation**](cesium/) – All the code and data for a self-contained web app that uses [CesiumJS](https://cesium.com/cesiumjs/) to create a 3D city simulation in the browser, populated with animated vehicles representing tracking data queried from GeoSpock DB. Use as the starting point for your own GeoSpock-powered 3D world simulations.
 * [**GeoSpock DB queries from JavaScript**](presto-client-browser/) – An NPM module, [`presto-client-browser`](https://www.npmjs.com/package/presto-client-browser), which you can use to run GeoSpock DB queries in your own JavaScript browser apps. For example usage, refer to the Kepler and Cesium examples above, which both use the module to query their datasets.

### Datasets (for GeoSpock DB Enterprise)

The source data for the example datasets and other large resources needed to run these projects is provided by GeoSpock in an AWS S3 bucket named `geospock-example-data`. Full instruction on how to download the files and ingest the data into your GeoSpock DB deployment, along with the necessary data source description files, can be found in the [datasets folder](datasets/).


# GeoSpock DB Discovery

GeoSpock DB Discovery provides a way to experience the power of GeoSpock DB without having to pay any license fees. You can sign up [here](https://geospock.com/en/product/geospock-db-discovery/).

Typically available for a short trial period, GeoSpock DB Discovery gives you control of your own query engine and allows you to run queries using standard ANSI SQL against a range of pre-selected datasets.

The [Python](discovery/sg_python) and [Tableau](discovery/sg_tableau) code found in [discovery](discovery/) is to be used jointly with a GeoSpock DB Discovery deployment. These examples use queries that extract insights from the Singapore smart city datasets available in GeoSpock DB Discovery and that take advantage of GeoSpock's query engine. Further documentation on how to connect to Discovery, query examples and datasets available can be found [here](https://docs.geospock.com/discovery/about/).