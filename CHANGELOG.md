# Changelog

# Version 2.5.4 (2021-04-22)
## Added
* User management
    * Query for remaining invites and users available to an organization
    * Set and update organization roles
    * Set / update / revoke project role
    * Delete users from organization
    * Example notebook added under examples/basics
* Issues and comments export
    * Bulk export issues and comments. See `Project.export_labels`
* MAL on Tiled Imagery
    * Example notebook added under examples/model_assisted_labeling
    * `Dataset.create_data_rows` now allows users to upload tms imagery

# Version 2.5.3 (2021-04-01)
## Added
* Cleanup and add additional example notebooks
* Improved README for SDK and examples
* Easier to retrieve per annotation `BulkImportRequest` status, errors, and inputs
    * See `BulkImportRequest.errors`, `BulkImportRequest.statuses`, `BulkImportRequest.inputs` for more information

# Version 2.5.2 (2021-03-25)
## Fix
* Ontology builder defaults to None for missing fields instead of empty lists
* MAL validation added extra fields to subclasses 

### Added
* Example notebooks

## Version 2.5.1 (2021-03-15)
### Fix
* `Dataset.data_row_for_external_id` No longer throws `ResourceNotFoundError` when there are duplicates
*  Improved doc strings

### Added
* OntologyBuilder for making project setup easier
* Now supports `IMAGE_OVERLAY` metadata
* Webhooks for review topics added
* Upload project instructions with `Project.upsert_instructions`
* User input validation 
    * MAL validity is now checked client side for faster feedback
    * type and value checks added in a few places

## Version 2.4.11 (2021-03-07)
### Fix
* Increase query timeout
* Retry 502s

## Version 2.4.10 (2021-02-05)
### Added 
* SDK version added to request headers

## Version 2.4.9 (2020-11-09)
### Fix
* 2.4.8 was broken for > Python 3.6
### Added
* include new `Project.enable_model_assisted_labeling` method for turning on [model-assisted labeling](https://labelbox.com/docs/automation/model-assisted-labeling)

## Version 2.4.8 (2020-11-06)
### Fix
* fix failing `next` call https://github.com/Labelbox/labelbox-python/issues/74

## Version 2.4.7 (2020-09-10)
### Added
* `Ontology` schema for interacting with ontologies and their schema nodes

## Version 2.4.6 (2020-09-03)
### Fix
* fix failing `create_metadata` calls

## Version 2.4.5 (2020-09-01)
### Added
* retry capabilities for common flaky API failures
* protection against improper types passed into `Project.upload_anntations`
* pass thru API error messages when possible

## Version 2.4.3 (2020-08-04)

### Added
* `BulkImportRequest` data type
* `Project.upload_annotation` supports uploading via a local ndjson file, url, or a iterable of annotations

## Version 2.4.2 (2020-08-01)
### Fixed
* `Client.upload_data` will now pass the correct `content-length` when uploading data.

## Version 2.4.1 (2020-07-22)
### Fixed
* `Dataset.create_data_row` and `Dataset.create_data_rows` will now upload with content type to ensure the Labelbox editor can show videos.

## Version 2.4 (2020-01-30)

### Added
* `Prediction` and `PredictionModel` data types.

## Version 2.3 (2019-11-12)

### Changed
* `Client.execute` now automatically extracts the 'data' value from the
returned `dict`. This *breaks* existing code that directly uses the
`Client.execute` method.
* Major code reorganization, naming and test improvements.
* `Label.seconds_to_label` field value is now optional when creating
a `Label`. Default value is 0.0.

### Added
* `Project.upsert_review_queue` method.
* `Project.extend_reservations` method.
* `Label.created_by` relationship (To-One User).
* Changelog.

### Fixed
* `Dataset.create_data_row` upload of local file data.

## Version 2.2 (2019-10-18)
Changelog not maintained before version 2.2.
