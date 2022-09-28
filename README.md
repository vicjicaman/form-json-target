# form-json-target
A React component to capture and generate form from JSON schema

## Live demos
https://code.vicjicama.com/demo/app/form-schema/

## Real life functionality in live demos

Here are a couple demos that are using the component in real functionality scenario:

HTML editor
https://code.vicjicama.com/demo/app/editor/

SQL table viewer/editor
https://code.vicjicama.com/demo/app/table-viewer/


## Motivation
I wanted to reuse my backend validations easily on the frontend

## Form component
- Resolve oneOf forms
- Complex schemas
- Recursive types
- Events with previous/current values 
- Extensible widgets
- Support nested deep/recursive array/objects  

## Project improvements
 - The form validation is now exactly the same as the backend validations.
 - Consistency between forms, validations, graphql, migrations and data versions
 - DynamoDB migrations are considerably easier now
 - Generate GraphQL schema (only types/input definitions)
 - Same schema for frontend/backend/GraphQL input/types
 - Any complex object compare made easy (with oneOf/oneOf resolved)

## Schema helper library
- Extract default values
- Resolve $ref, oneOf, anyOf, allOf
- Extract only schema values (Useful for GraphQL output/inputs match)
- Resolve recursive schemas

