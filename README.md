# Snowflake-Data-Streaming
Snowpipe was introduced to be utilised for automatically discovering new data files in cloud storage (e.g. Azure Blob Storage) and then load the data into a certain table.

We can easily achieve the following with it:

    Loading data files in different formats such as CSV, JSON, XML, Parquet and ORC
    Adopting and tweaking the data source for better compatibility such as stripping outer array for JSON and stripping outer element for XML
    Changing column names
    Changing column orders
    Omitting columns
    Parsing data/time string into data/time object

Therefore, for the following reasons, Streams and Tasks are needed for the rest of the data pipelining:

    Some data transformation might be necessary, such as numbers calculation and strings concatenation.
    The data source is not in typical third-norm format, so it needs to be loaded into multiple tables based on certain relations.
    The ELT jobs may not be limited to appending tables, but also include more complex requirements such as SCD (Slowly Changing Dimension) to be implemented.

Therefore, we have to involve other objects in Snowflake to complete the data pipeline.
