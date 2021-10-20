# Service

This entity represents a Service. A Service is created in the course a contact. Services include subjective information provided by the patient, such as complaints, reason for visit, feelings, etc. or objective information like bio-metric measures (blood pressure, temperature, heart beat, etc.), or physical exam description, diagnosis, prescription, integration of lab reports from another healthcare party, action plan, etc. Any action performed by the healthcare party which is relevant for the healthcare element of a patient is considered a service. The services can be linked to healthcare elements or other structuring elements of the medical record

## Properties

| Property               | Type                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id *`                 | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | The Id of the Service. We encourage using either a v4 UUID or a HL7 Id.                                                                                                                                                                                                                                                                                                                       |
| `contactId`            | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | Id of the contact during which the service is provided                                                                                                                                                                                                                                                                                                                                        |
| `subContactIds`        | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | List of IDs of all sub-contacts that link the service to structural elements. Only used when the Service is emitted outside of its contact                                                                                                                                                                                                                                                    |
| `plansOfActionIds`     | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | List of IDs of all plans of actions (healthcare approaches) as a part of which the Service is provided. Only used when the Service is emitted outside of its contact                                                                                                                                                                                                                          |
| `healthElementsIds`    | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | List of IDs of all healthcare elements for which the service is provided. Only used when the Service is emitted outside of its contact                                                                                                                                                                                                                                                        |
| `formIds`              | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | List of Ids of all forms linked to the Service. Only used when the Service is emitted outside of its contact.                                                                                                                                                                                                                                                                                 |
| `secretForeignKeys`    | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | The secret patient key, encrypted in the patient document, in clear here.                                                                                                                                                                                                                                                                                                                     |
| `cryptedForeignKeys *` | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/List/README.md)        | The public patient key, encrypted here for separate Crypto Actors.                                                                                                                                                                                                                                                                                                                            |
| `delegations *`        | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/List/README.md)        | The delegations giving access to connected healthcare information.                                                                                                                                                                                                                                                                                                                            |
| `encryptionKeys *`     | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/List/README.md)        | The contact secret encryption key used to encrypt the secured properties (like services for example), encrypted for separate Crypto Actors.                                                                                                                                                                                                                                                   |
| `label *`              | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   |                                                                                                                                                                                                                                                                                                                                                                                               |
| `dataClassName`        | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   |                                                                                                                                                                                                                                                                                                                                                                                               |
| `index`                | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | format: int64.                                                                                                                                                                                                                                                                                                                                                                                |
| `content *`            | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Content/README.md)     | The type of the content recorded in the documents for the service                                                                                                                                                                                                                                                                                                                             |
| `textIndexes *`        | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)      |                                                                                                                                                                                                                                                                                                                                                                                               |
| `valueDate`            | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | format: int64.                                                                                                                                                                                                                                                                                                                                                                                |
| `openingDate`          | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | format: int64.                                                                                                                                                                                                                                                                                                                                                                                |
| `closingDate`          | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | format: int64.                                                                                                                                                                                                                                                                                                                                                                                |
| `formId`               | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   |                                                                                                                                                                                                                                                                                                                                                                                               |
| `created`              | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | The timestamp (unix epoch in ms) of creation of this entity, will be filled automatically if missing. Not enforced by the application server. format: int64.                                                                                                                                                                                                                                  |
| `modified`             | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | The date (unix epoch in ms) of the latest modification of this entity, will be filled automatically if missing. Not enforced by the application server. format: int64.                                                                                                                                                                                                                        |
| `endOfLife`            | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Long/README.md)       | Soft delete (unix epoch in ms) timestamp of the object. format: int64.                                                                                                                                                                                                                                                                                                                        |
| `author`               | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | The id of the User that has created this form, will be filled automatically if missing. Not enforced by the application server.                                                                                                                                                                                                                                                               |
| `responsible`          | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | The id of the HealthcareParty that is responsible for this form, will be filled automatically if missing. Not enforced by the application server.                                                                                                                                                                                                                                             |
| `medicalLocationId`    | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | The id of the medical location where this entity was created.                                                                                                                                                                                                                                                                                                                                 |
| `comment`              | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | Text, comments on the Service provided                                                                                                                                                                                                                                                                                                                                                        |
| `status`               | [Integer](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Integer/README.md) | format: int32.                                                                                                                                                                                                                                                                                                                                                                                |
| `invoicingCodes *`     | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)     | List of invoicing codes                                                                                                                                                                                                                                                                                                                                                                       |
| `qualifiedLinks *`     | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/Map/README.md)         | Links towards related services (possibly in other contacts)                                                                                                                                                                                                                                                                                                                                   |
| `codes *`              | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/CodeStub/README.md)   | A code is an item from a codification system that qualifies the content of this entity. SNOMED-CT, ICPC-2 or ICD-10 codifications systems can be used for codes                                                                                                                                                                                                                               |
| `tags *`               | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/CodeStub/README.md)   | A tag is an item from a codification system that qualifies an entity as being member of a certain class, whatever the value it might have taken. If the tag qualifies the content of a field, it means that whatever the content of the field, the tag will always apply. For example, the label of a field is qualified using a tag. LOINC is a codification system typically used for tags. |
| `encryptedSelf`        | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/contact/service/String/README.md)   | The base64 encoded data of this object, formatted as JSON and encrypted in AES using the random master key from encryptionKeys.                                                                                                                                                                                                                                                               |