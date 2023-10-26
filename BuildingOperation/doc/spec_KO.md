<!-- 10-Header -->
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  

==========
<!-- 15-License -->


<!-- /15-License -->
<!-- 20-Description -->


<!-- /20-Description -->
<!-- 30-PropertiesList -->




- `alternateName[string]`: 이 항목의 대체 이름  
<!-- 35-RequiredProperties -->

- `endDate`  
<!-- 40-RequiredProperties -->

<!-- /40-RequiredProperties -->
<!-- 50-DataModelHeader -->


<!-- /50-DataModelHeader -->
<!-- 60-ModelYaml -->
<details><summary><strong>full yaml details</strong></summary>    

BuildingOperation:    
  description: Information on a given Building Operation    
  properties:    
    alternateName:    
      description: An alternative name for this item    
      type: string    
      x-ngsi:    
        type: Property    
    dataProvider:    
      description: A sequence of characters identifying the provider of the harmonised data entity    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: Entity creation timestamp. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateFinished:    
      description: The actual end date for the operation    
      format: date-time    
      type: string    
      x-ngsi:    
        model: https://schema.org/DateTime    
        type: Property    
    dateModified:    
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateStarted:    
      description: The actual start date for the operation    
      format: date-time    
      type: string    
      x-ngsi:    
        model: https://schema.org/DateTime    
        type: Property    
    description:    
      description: A description of this item    
      type: string    
      x-ngsi:    
        type: Property    
    endDate:    
      description: The planned end date for the operation    
      format: date-time    
      type: string    
      x-ngsi:    
        model: https://schema.org/DateTime    
        type: Property    
    id:    
      anyOf:    
        - description: Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
          x-ngsi:    
            type: Property    
        - description: Identifier format of any NGSI entity    
          format: uri    
          type: string    
          x-ngsi:    
            type: Property    
      description: Unique identifier of the entity    
      x-ngsi:    
        type: Property    
    name:    
      description: The name of this item    
      type: string    
      x-ngsi:    
        type: Property    
    operationSequence:    
      description: Id of the sequence of the operation when available    
      items:    
        type: string    
      type: array    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    operationType:    
      description: Type of the operation on the building    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    owner:    
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)    
      items:    
        anyOf:    
          - description: Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
            x-ngsi:    
              type: Property    
          - description: Identifier format of any NGSI entity    
            format: uri    
            type: string    
            x-ngsi:    
              type: Property    
        description: Unique identifier of the entity    
        x-ngsi:    
          type: Property    
      type: array    
      x-ngsi:    
        type: Property    
    refBuilding:    
      anyOf:    
        - description: Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
          x-ngsi:    
            type: Property    
        - description: Identifier format of any NGSI entity    
          format: uri    
          type: string    
          x-ngsi:    
            type: Property    
      description: Building reference where the operation is performed    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    refOperator:    
      anyOf:    
        - description: Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
          x-ngsi:    
            type: Property    
        - description: Identifier format of any NGSI entity    
          format: uri    
          type: string    
          x-ngsi:    
            type: Property    
      description: Reference to the Operator doing the operation on the building    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    refRelatedBuildingOperation:    
      description: Reference to other building operations when in sequence    
      items:    
        anyOf:    
          - description: Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
            x-ngsi:    
              type: Property    
          - description: Identifier format of any NGSI entity    
            format: uri    
            type: string    
            x-ngsi:    
              type: Property    
        description: Unique identifier of the entity    
        x-ngsi:    
          type: Property    
      type: array    
      x-ngsi:    
        type: Relationship    
    refRelatedDeviceOperation:    
      description: Devices related to the current operation. A list of references to an entity of type Device    
      items:    
        anyOf:    
          - description: Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
            x-ngsi:    
              type: Property    
          - description: Identifier format of any NGSI entity    
            format: uri    
            type: string    
            x-ngsi:    
              type: Property    
        description: Unique identifier of the entity    
        x-ngsi:    
          type: Property    
      type: array    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    result:    
      description: 'Result of the building operation. Enum:''ok, aborted'''    
      enum:    
        - ok    
        - aborted    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    seeAlso:    
      description: list of uri pointing to additional resources about the item    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object'    
      type: string    
      x-ngsi:    
        type: Property    
    startDate:    
      description: The planned start date for the operation    
      format: date-time    
      type: string    
      x-ngsi:    
        model: https://schema.org/DateTime    
        type: Property    
    status:    
      description: 'Status of the operation. Enum:''cancelled, finished, ongoing, planned, scheduled'' '    
      enum:    
        - cancelled    
        - finished    
        - ongoing    
        - planned    
        - scheduled    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    type:    
      description: It has to be BuildingOperation    
      enum:    
        - BuildingOperation    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - type    
    - id    
    - refBuilding    
    - startDate    
    - endDate    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.Building/blob/master/BuildingOperation/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.Building/BuildingOperation/schema.json    
  x-model-tags: ""    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->
<!-- 70-MiddleNotes -->
<!-- /70-MiddleNotes -->
<!-- 80-Examples -->



<details><summary><strong>show/hide example</strong></summary>    


  "id": "57b912ab-eb47-4cd5-bc9d-73abece1f1b3",  
  "type": "BuildingOperation",  
  "dateCreated": "2016-08-08T10:18:16Z",  
  "dateModified": "2016-08-08T10:18:16Z",  
  "source": "http://www.example.com",  
  "dataProvider": "OperatorA",  
  "refBuilding": "building-a85e3da145c1",  
  "operationType": "airConditioning",  
  "description": "Air conditioning levels reduced due to out of hours",  
  "result": "ok",  
  "startDate": "2016-08-08T10:18:16Z",  
  "endDate": "2016-08-20T10:18:16Z",  
  "dateStarted": "2016-08-08T10:18:16Z",  
  "dateFinished": "2016-08-20T10:18:16Z",  
  "status": "finished",  
  "operationSequence": ["fan_power%3D0", "set_temperature%3D24"],  
  "refRelatedBuildingOperation": [  
    "b4fb8bff-1a8f-455f-8cc0-ca43c069f865",  
    "55c24793-3437-4157-9bda-667c9e1531fc"  
  ],  
  "refRelatedDeviceOperation": [  
    "36744245-6716-4a28-84c7-0e3d7520f143",  
    "33b2b713-9223-40a5-87a0-3f80a1264a6c"  
  ]  
}  
```  
</details>  


<details><summary><strong>show/hide example</strong></summary>    


  "id": "57b912ab-eb47-4cd5-bc9d-73abece1f1b3",  
  "type": "BuildingOperation",  
  "status": {  
    "type": "Text",  
    "value": "finished"  
  },  
  "startDate": {  
    "type": "DateTime",  
    "value": "2016-08-08T10:18:16Z"  
  },  
  "operationSequence": {  
    "type": "array",  
    "value": [  
      "fan_power%3D0",  
      "set_temperature%3D24"  
    ]  
  },  
  "endDate": {  
    "type": "DateTime",  
    "value": "2016-08-20T10:18:16Z"  
  },  
  "description": {  
    "type": "Text",  
    "value": "Air conditioning levels reduced due to out of hours"  
  },  
  "refRelatedDeviceOperation": {  
    "type": "array",  
    "value": [  
      "36744245-6716-4a28-84c7-0e3d7520f143",  
      "33b2b713-9223-40a5-87a0-3f80a1264a6c"  
    ]  
  },  
  "dateCreated": {  
    "type": "DateTime",  
    "value": "2016-08-08T10:18:16Z"  
  },  
  "dateModified": {  
    "type": "DateTime",  
    "value": "2016-08-08T10:18:16Z"  
  },  
  "refRelatedBuildingOperation": {  
    "type": "array",  
    "value": [  
      "b4fb8bff-1a8f-455f-8cc0-ca43c069f865",  
      "55c24793-3437-4157-9bda-667c9e1531fc"  
    ]  
  },  
  "source": {  
    "type": "URL",  
    "value": "http://www.example.com"  
  },  
  "refBuilding": {  
    "type": "URI",  
    "value": "building-a85e3da145c1"  
  },  
  "result": {  
    "type": "Text",  
    "value": "ok"  
  },  
  "operationType": {  
    "type": "Text",  
    "value": "airConditioning"  
  },  
  "dateStarted": {  
    "type": "DateTime",  
    "value": "2016-08-08T10:18:16Z"  
  },  
  "dateFinished": {  
    "type": "DateTime",  
    "value": "2016-08-20T10:18:16Z"  
  },  
  "dataProvider": {  
    "type": "Text",  
    "value": "OperatorA"  
  }  
}  
```  
</details>  


<details><summary><strong>show/hide example</strong></summary>    


    "id": "urn:ngsi-ld:BuildingOperation:57b912ab-eb47-4cd5-bc9d-73abece1f1b3",  
    "type": "BuildingOperation",  
    "createdAt": "2016-08-08T10:18:16Z",  
    "dataProvider": "OperatorA",  
    "dateFinished": {  
        "@type": "DateTime",  
        "@value": "2016-08-20T10:18:16Z"  
    },  
    "dateStarted": {  
        "@type": "DateTime",  
        "@value": "2016-08-08T10:18:16Z"  
    },  
    "description": "Air conditioning levels reduced due to out of hours",  
    "endDate": {  
        "@type": "DateTime",  
        "@value": "2016-08-20T10:18:16Z"  
    },  
    "modifiedAt": "2016-08-08T10:18:16Z",  
    "operationSequence": [  
        "fan_power%3D0",  
        "set_temperature%3D24"  
    ],  
    "operationType": "airConditioning",  
    "refBuilding": "urn:ngsi-ld:Building:building-a85e3da145c1",  
    "refRelatedBuildingOperation": [  
        "urn:ngsi-ld:BuildingOperation:b4fb8bff-1a8f-455f-8cc0-ca43c069f865",  
        "urn:ngsi-ld:BuildingOperation:55c24793-3437-4157-9bda-667c9e1531fc"  
    ],  
    "refRelatedDeviceOperation": [  
        "urn:ngsi-ld:DeviceOperation:36744245-6716-4a28-84c7-0e3d7520f143",  
        "urn:ngsi-ld:DeviceOperation:33b2b713-9223-40a5-87a0-3f80a1264a6c"  
    ],  
    "result": "ok",  
    "source": "http://www.example.com",  
    "startDate": {  
        "@type": "DateTime",  
        "@value": "2016-08-08T10:18:16Z"  
    },  
    "status": "finished",  
    "@context": [  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.Building/master/context.jsonld"  
    ]  
}  
```  
</details>  


<details><summary><strong>show/hide example</strong></summary>    


  "id": "urn:ngsi-ld:BuildingOperation:57b912ab-eb47-4cd5-bc9d-73abece1f1b3",  
  "type": "BuildingOperation",  
  "createdAt": "2016-08-08T10:18:16Z",  
  "dataProvider": {  
    "type": "Property",  
    "value": "OperatorA"  
  },  
  "dateFinished": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2016-08-20T10:18:16Z"  
    }  
  },  
  "dateStarted": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2016-08-08T10:18:16Z"  
    }  
  },  
  "description": {  
    "type": "Property",  
    "value": "Air conditioning levels reduced due to out of hours"  
  },  
  "endDate": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2016-08-20T10:18:16Z"  
    }  
  },  
  "modifiedAt": "2016-08-08T10:18:16Z",  
  "operationSequence": {  
    "type": "Property",  
    "value": [  
      "fan_power%3D0",  
      "set_temperature%3D24"  
    ]  
  },  
  "operationType": {  
    "type": "Property",  
    "value": "airConditioning"  
  },  
  "refBuilding": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:Building:building-a85e3da145c1"  
  },  
  "refRelatedBuildingOperation": {  
    "type": "Relationship",  
    "object": [  
      "urn:ngsi-ld:BuildingOperation:b4fb8bff-1a8f-455f-8cc0-ca43c069f865",  
      "urn:ngsi-ld:BuildingOperation:55c24793-3437-4157-9bda-667c9e1531fc"  
    ]  
  },  
  "refRelatedDeviceOperation": {  
    "type": "Relationship",  
    "object": [  
      "urn:ngsi-ld:DeviceOperation:36744245-6716-4a28-84c7-0e3d7520f143",  
      "urn:ngsi-ld:DeviceOperation:33b2b713-9223-40a5-87a0-3f80a1264a6c"  
    ]  
  },  
  "result": {  
    "type": "Property",  
    "value": "ok"  
  },  
  "source": {  
    "type": "Property",  
    "value": "http://www.example.com"  
  },  
  "startDate": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2016-08-08T10:18:16Z"  
    }  
  },  
  "status": {  
    "type": "Property",  
    "value": "finished"  
  },  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/dataModel.Building/master/context.jsonld"  
  ]  
}  
```  
</details><!-- /80-Examples -->
<!-- 90-FooterNotes -->
<!-- /90-FooterNotes -->
<!-- 95-Units -->

<!-- /95-Units -->
<!-- 97-LastFooter -->
---  
