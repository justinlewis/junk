# Key Concepts

## Key Concepts

### Single Source of Truth

The CGR provides a single source of truth for your data. At a high level this means you have one place (the CGR) to go to for getting or updating your data rather than different files that are in different formats and require different systems. At a lower level this means that one single data element should be represented once in hte system. For example, there should be only one instance of a specific country in the system.

### Geo-Object

The Geo-Object is the central concept in the GeoRegistry, and it is the lowest-level piece of geographic data in the system.  A Geo-Object is instance level data meaning it represents specific geographies in place and time (i.e. a health facility). If you are familiar with DHIS2, you may know this as an organization unit. Each Geo-Object directly translates into a single row in a MasterList.&#x20;

#### Geo-Object Attributes

A Geo-Object has attributes which provide meaningful descriptive data about a geography.  Geo-Objects have a set of default attributes like display label that are on all objects but additional attributes can be added to store more information about geographies.

#### Geo-Object Geometries

Geometries are a special type of attribute that are used to spatially analyze and map geographies. A Geo-Object geometry types may be one of: Multipolygon, Polygon, Point, Multipoint, Line, Multiline. This geometry type must match the geometry type defined in the Geo-Object Type.

### Geo-Object Type

Geo-Object Types define the structure of instance data (i.e. Geo-Objects) that is loaded into that Geo-Object Type. This includes all the elements that shape how instance level data is stored like geometry type, custom attributes, and more.

### Hierarchy

A hierarchy defines a formal structure of how Geo-Object Types relate geospatially.&#x20;

### Data Over Time

Tracking the changes in geography over time is important to understand how conditions in the past affect our understanding of today while planning for the future. The CGR enables all attributes and relationships to be versioned over time. This means that a health facility Geo-Object can have a record of name changes over time while still maintaining a single source of truth for that health facility.

#### How change over time is managed

To reduce complexity in managing change over time an algorithm is used to maintain a constant record from the first known point in time that a Geo-Object exists to infinity. The basic logic enforces these principles:

1. Only start dates on an attribute version can be modified resulting in end dates being auto calculated.
2. An end date is calculated as a day before the start date of a more recent attribute version or infinity in the case of the most recent version.
3. The most recent attribute version will always have an end date of infinity which essentially means most current.
4. An attributes version history can have no gaps.

### Data Curation

To maintain a high level of data integrity instance level data (Geo-Objects) are curated through an authoritative process. Registry Contributors submit change requests to suggest changes to a Geo-Object while Registry Maintainers review, modify (if necessary), and approve or reject those changes.&#x20;

#### Change Requests

Change requests are changes to a Geo-Object a Registry Contributor suggests. A change request can have one or more actions. Each action is a change to an attribute on a Geo-Object that collectively make up a change request for an entire Geo-Object.&#x20;
