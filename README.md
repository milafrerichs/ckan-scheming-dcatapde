# ckan-scheming-dcatapde

## Installation

Notwendige Plugins: 
* [ckanext-scheming](https://github.com/ckan/ckanext-scheming/)
* [ckanext-dcat](https://github.com/ckan/ckanext-dcat/)

### ckan.ini:
```
ckan.plugins = scheming_datasets dcat structured_data

scheming.dataset_schemas = path/to/dcatapde-full.yml
scheming.presets=ckanext.scheming:presets.json ckanext.dcat.schemas:presets.yaml path/to/dcatapde/preset.json

ckanext.dcat.rdf.profiles=euro_dcat_ap_3 dcatap_de
```

## preset.json

Ich musste für Harvesting die preset.json erstellen, da nicht alle Portale das Thema schon gesetzt haben, sondern über die Gruppen gingen. Und Sprache ist kein Pflichtfeld, deswegen muss dort auch ein `ignore_missing`. 
