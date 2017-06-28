Overview
========

Here you will find links to datasets for `M001: MongoDB Basics <https://university.mongodb.com/courses/M001/about>`_.

Datasets
========

All datasets are provided in Amazon S3 in a single zip file (243 MB zipped; 1.5 GB unzipped). The files were created with the `mongodump <https://docs.mongodb.com/manual/reference/program/mongodump/>`_ command. They may be imported into your MongoDB deployment using `mongorestore <https://docs.mongodb.com/manual/reference/program/mongorestore/>`_. Note that these datasets include the indexes necessary to support example queries and labs used in M001. The datasets included are as follows.

- **100YWeatherSmall** (403 MB) - readings from weather stations throughout the world.
- **city** (3.2 MB) - geospatial representations of neighborhoods in New York City.
- **citibike** (835 MB) - details for trips taken using `Citibikes <https://www.citibikenyc.com/>`_.
- **ships** (3.6 MB) - data on shipwrecks around the world, including geospatial coordinates.
- **video** (303 MB) - summary data on movies.


Importing Data Locally
======================

These instructions will help you load the M001 datasets into a local MongoDB instance (e.g., MongoDB running on your laptop).

1. Download the `m001-datasets.zip <https://s3.amazonaws.com/edu-static.mongodb.com/data/M001/m001-datasets.zip>`_ file from S3.

2. Ensure you have a running MongoDB instance. For instructions on installation and setup, see the `MongoDB installation documentation <https://docs.mongodb.com/manual/installation/>`_. Installation tutorials for all platforms include instructions for running MongoDB (the mongod daemon).

3. Once you have a ``mongod`` instance running, you may import the datasets using `mongorestore <https://docs.mongodb.com/manual/reference/program/mongorestore/>`_.

   a. Open a command shell (e.g., bash, powershell, or cmd).
   b. Change directory (e.g., ``cd``) to where you downloaded m001-datasets.zip.
   c. Assuming you are running ``mongod`` on the default port, you may restore the datasets with the command, ``mongorestore --gzip --archive=m001-datasets.zip``.
