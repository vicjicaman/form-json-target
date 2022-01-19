# form-json-target
A React component to capture and generate form from JSON schema

## Schema helper library
- Extract default values
- Resolve $ref, oneOf, anyOf, allOf
- Extract only schema values (Useful for GraphQL output/inputs match)
- Resolve recursive schemas

## Form component
- Resolve oneOf forms
- Complex schemas
- Recursive types
- Events with previous/current values 
- Route based navigation
- Extensible simple widgets
- Support nested deep/recursive array/objects  
- Forms are NOT based on the schema
- Debounce live updates

## Widgets
- Markdown
- Richtext
- Drag&drop arrays
- Color
- Icons
- Options
- Arrays of objects and primitives


## Motivation
There are multiple json-schema form components out there that will help you to generate form from a json schema.

 - Resolve oneOf values/subforms
 - Routed based forms/subforms
 - Recursive types subform support

You have an object that has an array of objects, each object of that array can be oneOf other objects.
Those oneOf objects can contain complex schemas with array, objects or oneOf selects

I will rewrite the previous paragraph with a real life demo:

You have an Page object that have an array of Element objects, each Element can be oneOf [Code|Paragraph|Snapshot] objects.
Those oneOf [Code|Paragraph|Snapshot] can contain complex schemas with array, objects or oneOf selects (check the Page elements example)

## Brief architecture review


## Real life project impact
I started this component because I needed to capture a lot of configuration parameters derived from the feedback and feature request for the projects that I am working on, as a solo developer I try to reuse the code as much as possible, and the forms were a big pain as the project were growing.

- Shrink more than 400 form related files (route/form components/graphql schema/etc) to less than 50 json schema and form config files
- The form input validation is now exactly the same as the backend validations.
- Consistency between forms, validations, graphql, migrations and data versions
- Easier routes structure/compose 
- Migrations are considerably easier now
- Easier to reuse data definitions 
- Generate GraphQL schema (only types/input definitions)
- Same schema for frontend/backend/GraphQL input/types
- Any complex object compare made easy (with oneOf/oneOf resolved)
- All the data interactions are reduced to a single "target" type, making very easy debug complex forms schemas

## Examples

The form component is being used on the next projects, there is a live demo on the link, all the forms and controls are an instance of this component.

### TableWS
 https://table.listws.com/v2/table/editor/table-v2.listws.app/products

### LandingWS
 https://landing.listws.com/v2/landing/demo/editor/landing.listws.com/home

### ShopWS 
 https://shop.listws.com/v2/store/demo/editor/demoshop.listws.app/default


Here is a list of different forms and the more in detail functionality:

### Dynamic forms
You can create the forms based on their types and update them on the UI
https://shop.listws.com/v2/store/demo/editor/demoshop.listws.app/default/sections/3/schema/types

### Automatic Breadcrumb navigation
The breadcrumb menu is automatically updated depending on the current form
https://shop.listws.com/v2/store/demo/editor/demoshop.listws.app/default/products/0

### List of pages
List of pages that automatically syncs with the preview panel
https://shop.listws.com/v2/store/demo/editor/demoshop.listws.app/default/pages

### Page configuration capture
This form captures page configuration parameters like styles, scripts and metadata.
https://table.listws.com/v2/table/editor/table-v2.listws.app/products/config/page-config

### Type and entries capture
This example use the form component to form-build itself (with recursive types support)
https://table.listws.com/v2/table/editor/table-v2.listws.app/products/table/system/types

### Page elements
I use this component to capture the elements configuration for a page, this is being used on TableWS and LandingWS projects.
https://table.listws.com/v2/table/editor/table-v2.listws.app/products/pages/0/elements

### List configuration for TableWS
All the previous examples are using this React form component based on JSON schema, I even use the same component to create the form definitions, the next form schema was created using the types capture (listed on the previous examples)
https://table.listws.com/v2/table/editor/table-v2.listws.app/products/sections/0/schema/values


## TODO

- Create NPM component
- Create an interactive demo for the previous example forms separated from TableWS
- Create a demo for the Types and entries capture functionality, also an schema exporter
- Migrate and separate source from TableWS, LandingWS and ShopWS


