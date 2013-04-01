od_package
==========

This Drupal 7 module is used to link nodes in Drupal 7 to CKAN packages.

When a package (also known as a dataset) is updated or inserted into CKAN, 
a CKAN extension will update a simple database table in Drupal called "od_package".

When Drupal users want to comment or perform other social interactive functions
with the package, they should look for a node at "/dataset/<package ID>". This
module will search for a matching node and return it. If the node does not yet
exist, the module will automatically create one based on the package information
stored in the table "od_package". If the user attempts to go to a dataset that
does not exist in "od_package" they will be informed that the dataset does not exist.

Outstanding issues:

* need some template work to display the appropriate description on the node 
  view page. The description is not editable.
* the title field should be a translateable field. The template will need to 
  be updated as well.
* May need to redirect the first time a page is viewed.
