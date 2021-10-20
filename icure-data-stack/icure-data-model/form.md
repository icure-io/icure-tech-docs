# Form

## Properties

| Property               | Type                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                   |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id *`                 | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | the Id of the form. We encourage using either a v4 UUID or a HL7 Id.                                                                                                                                                                                                                                                                                                                          |
| `rev`                  | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | the revision of the form in the database, used for conflict management / optimistic locking.                                                                                                                                                                                                                                                                                                  |
| `created`              | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Long/README.md)       | The timestamp (unix epoch in ms) of creation of this entity, will be filled automatically if missing. Not enforced by the application server. format: int64.                                                                                                                                                                                                                                  |
| `modified`             | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Long/README.md)       | The date (unix epoch in ms) of the latest modification of this entity, will be filled automatically if missing. Not enforced by the application server. format: int64.                                                                                                                                                                                                                        |
| `author`               | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The id of the User that has created this form, will be filled automatically if missing. Not enforced by the application server.                                                                                                                                                                                                                                                               |
| `responsible`          | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The id of the HealthcareParty that is responsible for this form, will be filled automatically if missing. Not enforced by the application server.                                                                                                                                                                                                                                             |
| `medicalLocationId`    | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The id of the medical location where this entity was created.                                                                                                                                                                                                                                                                                                                                 |
| `tags *`               | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/CodeStub/README.md)   | A tag is an item from a codification system that qualifies an entity as being member of a certain class, whatever the value it might have taken. If the tag qualifies the content of a field, it means that whatever the content of the field, the tag will always apply. For example, the label of a field is qualified using a tag. LOINC is a codification system typically used for tags. |
| `codes *`              | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/CodeStub/README.md)   | A code is an item from a codification system that qualifies the content of this entity. SNOMED-CT, ICPC-2 or ICD-10 codifications systems can be used for codes                                                                                                                                                                                                                               |
| `endOfLife`            | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Long/README.md)       | Soft delete (unix epoch in ms) timestamp of the object. format: int64.                                                                                                                                                                                                                                                                                                                        |
| `deletionDate`         | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Long/README.md)       | hard delete (unix epoch in ms) timestamp of the object. Filled automatically when deletePatient is called. format: int64.                                                                                                                                                                                                                                                                     |
| `openingDate`          | [Long](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Long/README.md)       | format: int64.                                                                                                                                                                                                                                                                                                                                                                                |
| `status`               | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   |                                                                                                                                                                                                                                                                                                                                                                                               |
| `version`              | [Integer](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/Integer/README.md) | format: int32.                                                                                                                                                                                                                                                                                                                                                                                |
| `lid`                  | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   |                                                                                                                                                                                                                                                                                                                                                                                               |
| `descr`                | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | Name/basic description of the form                                                                                                                                                                                                                                                                                                                                                            |
| `formUuid`             | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | A unique external id (from another external source).                                                                                                                                                                                                                                                                                                                                          |
| `formTemplateId`       | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | Id of the form template being used to display the form                                                                                                                                                                                                                                                                                                                                        |
| `contactId`            | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | Id of the contact for which the form is being used.                                                                                                                                                                                                                                                                                                                                           |
| `healthElementId`      | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The healthcare element to which this form is attached.                                                                                                                                                                                                                                                                                                                                        |
| `planOfActionId`       | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The healthcare approach to which this form is attached.                                                                                                                                                                                                                                                                                                                                       |
| `parent`               | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The parent of this form, used to determine the forms hierarchy                                                                                                                                                                                                                                                                                                                                |
| `secretForeignKeys *`  | [List](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)     | The secretForeignKeys are filled at the to many end of a one to many relationship (for example inside Contact for the Patient -> Contacts relationship). Used when we want to find all contacts for a specific patient. These keys are in clear. You can have several to partition the medical document space.                                                                                |
| `cryptedForeignKeys *` | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/List/README.md)        | The secretForeignKeys are filled at the to many end of a one to many relationship (for example inside Contact for the Patient -> Contacts relationship). Used when we want to find the patient for a specific contact. These keys are the encrypted id (using the hcParty key for the delegate) that can be found in clear inside the patient. ids encrypted using the hcParty keys.          |
| `delegations *`        | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/List/README.md)        | When a document is created, the responsible generates a cryptographically random master key (never to be used for something else than referencing from other entities). He/she encrypts it using his own AES exchange key and stores it as a delegation. The responsible is thus always in the delegations as well                                                                            |
| `encryptionKeys *`     | [Map](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/List/README.md)        | When a document needs to be encrypted, the responsible generates a cryptographically random master key (different from the delegation key, never to appear in clear anywhere in the db. He/she encrypts it using his own AES exchange key and stores it as a delegation                                                                                                                       |
| `encryptedSelf`        | [String](https://github.com/taktik/icure-tech-docs/tree/5af8e13c187f73691c350b409b558ac754efaef8/icure-data-model/String/README.md)   | The base64 encoded data of this object, formatted as JSON and encrypted in AES using the random master key from encryptionKeys.                                                                                                                                                                                                                                                               |