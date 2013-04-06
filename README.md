# HyperREST Schemata

Based on [JSON Schema](http://json-schema.org), this is a series of schemata that define a way to document a HyperREST API.

# Structure

An API can be defined by

* **a host**
* a basePath
* **an entryPoint**
* resources,  
and each resource can be defined by
    * **a title**
    * **a path**
    * **identifyingRels**
    * rels,  
    and each rel can be defined by
        * operations  
        and each operation can be defined by
            * exposedSchema (accepted/patch/provided/error)
            * **method**
            * parameters
            * headers
            * schema
            * **response**
            * responses  
            and each response can be defined by
                * **httpStatuCode**
                * **httpStatusMessage**
                * subHttpCodes
                * headers
                * targetSchema

And each schema is a representation identified by a (vendor) media-type, and defined by a [JSON Hyper-Schema](http://json-schema.org/latest/json-schema-hypermedia.html).

# License

Apache 2.0
