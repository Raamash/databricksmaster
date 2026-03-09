# databricksmaster
To teach the databricks
*************************************************************
How the file looks on managed table
ls user/hive/warehouse/catalog/schema/object
*************************************************************
1. repos present in home rather than the workspace?
Repos to Git-folders; 
seems to be intentional to land on Home instead of repos; to siply the UI.

2. threshold set - properties?
CREATE TABLE my_catalog.my_schema.my_table (
  id INT,
  name STRING
)
USING DELTA
TBLPROPERTIES (
  'delta.deletedFileRetentionDuration' = 'interval 30 days',
  'delta.logRetentionDuration'         = 'interval 30 days'
);

3. optimize why it does not affect time travel?

where zorder col logs gets stored.
*************************************************************