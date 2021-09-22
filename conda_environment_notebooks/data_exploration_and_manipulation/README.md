Data Exploration and Manipulation Conda Environment Family Notebooks
====================================================================

The [Data Exploration and Manipulation conda environment family](https://docs.oracle.com/en-us/iaas/data-science/using/conda-dem-fam.htm) gives you the tools that you need to perform exploratory data analysis and develop a deeper understanding of the data that you are working with.
This [conda environment family](https://docs.cloud.oracle.com/en-us/iaas/data-science/using/use-notebook-sessions.htm#conda_understand_environments) contains packages for data exploration, manipulation, and visualization. Included within this conda environment are `pandas`, `numpy`, and `ads` to explore and transform your datasets. Use `matplotlib`, `seaborn`, `plotly`, and `bokeh` to construct visualizations. The Oracle Accelerated Data Science (`ADS`) library offers a variety of useful data access, profiling, transformation features along with power feature type management tools.

The notebooks in this folder are meant to be run in the [Data Exploration and Manipulation conda environment family](https://docs.oracle.com/en-us/iaas/data-science/using/conda-dem-fam.htm) conda environments.

# Notebook Descriptions

* `ads_feature_type.ipynb`: There is a distinction between the data type of a feature and the nature of data that it represents. The data type represents the form of the data that the computer understands. ADS uses the term "feature type" to refer to the nature of the data. For example, a medical record id could be represented as an integer, its data type, but the feature type would be "medical record id". The feature type represents the data the way the data scientist understands it. ADS provides the feature type module on top of your pandas dataframes and series to manage and use the typing information to better understand your data. This notebook summarizes the key concepts and advantages of using feature types to speed up your EDA.
* `ads_feature_type_EDA.ipynb`: In exploratory data analysis (EDA) the data scientist uses plots and statistics to summarize the characteristics of the data. The feature type system, in the ADS library, has been designed to speed up this process. The feature type system allows data scientists to separate the concept of how data is represented physically from what the data actually measures. The data can have feature types that classify the data based on what it represents and not how the data is stored in memory. In doing so, a feature type can have a set of built-in summary statistics and a plot. This notebook demonstrates how to use feature type plots and summary statistics in your EDA.
* `ads_feature_type_custom.ipynb`: The feature type system allows data scientists to separate the concept of how data is represented physically from what the data actually measures. The data can have feature types that classify the data based on what it represents and not how the data is stored in memory. Each set of data can have multiple feature types through a system of multiple inheritances. While ADS comes with a collection of common feature types, the power of the system is that an organization can create custom feature types for their data. This notebook provides an overview of how to create custom feature types.
* `ads_feature_type_handler.ipynb`: Feature types are a powerful way to abstract the nature of the data from the way that is it represented on the computer. Feature type handlers are a flexible way to improve and speed up your data validation process. It allows a feature type to be dynamically extended such that the data validation process can be reproducible and shared across projects. `ADS` comes with various validation routines. However, the system is designed for you to create your own validation routines to use on your organization's feature types. This notebook shows you how to create feature type handlers.
* `ads_feature_type_manager.ipynb`: The feature type system allows data scientists to separate the concept of how data is represented physically from what the data actually measures. The data can have feature types that classify the data based on what it represents and not how the data is stored in memory. Each set of data can have multiple feature types through a system of multiple inheritances. Feature type warnings are used for rapid validation of the data. The feature type handlers are a set of methods that return a boolean pandas series that indicates what values meet the validation criteria. The feature type manager provides the tools to manage the handlers that are used to drive this system. The system works by creating functions that are then registered as feature type validators or warnings. The role of the `feature_type_manager` is to provide the interface to manage these handlers
* `ads_feature_type_warnings.ipynb`: The feature type warning system works across an entire feature. For example, you can check for the number of missing values and set a threshold on what is the permitted upper limit. This can be a count, percentage, or some other metric. You can also create mechanisms where you check to ensure that the data has the distribution that is assumed by the model class that you want to use. For example, linear regression assumes that the data is normally distributed. Therefore, the feature type warning might have a Shapiro-Wilk test and a threshold for what is an expected value. Each feature can have as many feature type warnings as you want. Also, the multiple inheritance nature of the feature type system allows you to write-only the feature type warnings that are relevant for that specific feature type because the warnings for all inherited feature types to be checked. This feature reduces the amount of code duplication and speeds up your EDA. This notebook demonstrates how to use the feature type warning system to validate your data and create custom warnings.
* `adsdataset.ipynb`: One of the most important elements of any data science project is the data itself. This notebook demonstrates how to work with the `ADSDataset` class.
* `data_visualizations.ipynb`: This notebook provides an overview of the data visualizations that you can perform with ADS. It will focus on smart data visualization technology that uses the column types and other settings to atomically create an intuitive plot for your data.

