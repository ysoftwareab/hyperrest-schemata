# HyperREST Schemata

Based on [JSON Schema](http://json-schema.org), this is a series of schemata that define a way to document a HyperREST API.

# Structure

An API ([api.json](draft-00/api.json)) can be defined by

* **a host**
* a basePath
* **an entryPoint**
* resources,  
and each resource ([api-resource.json](draft-00/api-resource.json)) can be defined by
    * **a title**
    * **a path**
    * **identifyingRels**
    * rels,  
    and each rel ([rel.json](draft-00/rel.json)) can be defined by
        * operations  
        and each operation ([operation.json](draft-00/operation.json)) can be defined by
            * exposedSchema (accepted/patch/provided/error)
            * **method**
            * parameters
            * headers ([operation-header.json](draft-00/operation-header.json))
            * schema
            * **response**
            * responses  
            and each response ([operation-response.json](draft-00/operation-response.json)) can be defined by
                * **httpStatusCode**
                * **httpStatusMessage**
                * subHttpCodes
                * headers ([operation-header.json](draft-00/operation-header.json))
                * targetSchema

And each schema is a representation ([representation.json](draft-00/representation.json)) identified by **a (vendor) media-type**,
and defined by a [JSON Hyper-Schema](http://json-schema.org/latest/json-schema-hypermedia.html).

# License

Apache 2.0
