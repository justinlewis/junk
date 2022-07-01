# Getting Started

#### Geo-Object Geometries dsalfjlasdjflsj

Geometries are a special type of attribute that are used to spatially analyze and map geographies. A Geo-Object geometry types may be one of: Multipolygon, Polygon, Point, Multipoint, Line, Multiline. This geometry type must match the geometry type defined in the Geo-Object Type.

### Geo-Object Type

Geo-Object Types define the structure of instance data (i.e. Geo-Objects) that is loaded into that Geo-Object Type. This includes all the elements that shape how instance level data is stored like geometry type, custom attributes, and more.

### Hierarchy

A hierarchy defines a formal structure of how Geo-Object Types relate geospatially.

### Data Over Time

Tracking the changes in geography over time is important to understand how conditions in the past affect our understanding of today while planning for the future. The CGR enables all attributes and relationships to be versioned over time. This means that a health facility Geo-Object can have a record of name changes over time while still maintaining a single source of truth for that health facility.

#### How change over time is managed

To reduce complexity in managing change over time an algorithm is used to maintain a constant record from the first known point in time that a Geo-Object exists to infinity. The basic logic enforces these principles:

1. Only start dates on an attribute version can be modified resulting in end dates being auto calculated.
2. An end date is calculated as a day before the start date of a more recent attribute version or infinity in the case of the most recent version.
3. The most recent attribute version will always have an end date of infinity which essentially means most current.
4. An attributes version history can have no gaps.

### Data Curation

To maintain a high level of data integrity instance level data (Geo-Objects) are curated through an authoritative process. Registry Contributors submit change requests to suggest changes to a Geo-Object while Registry Maintainers review, modify (if necessary), and approve or reject those changes.

#### Change Requests

Change requests are changes to a Geo-Object a Registry Contributor suggests. A change request can have one or more actions. Each action is a change to an attribute on a Geo-Object that collectively make up a change request for an entire Geo-Object.

## Key Components

The CGR includes a collection of tools used to accomplish tasks.

### Geo-Objects and Hierarchies <a href="#geo-objects-and-hierarchies" id="geo-objects-and-hierarchies"></a>

This widget is used to define the structure of data being managed in the system.

### Lists <a href="#lists" id="lists"></a>

This widget is used to publish and explore lists as well as making modifications to Geo-Objects from those lists.

### Change Requests <a href="#change-requests" id="change-requests"></a>

This widget is used to manage change requests that Registry Contributors have submitted.

### Upload and Download <a href="#upload-and-download" id="upload-and-download"></a>

This widget is used to upload instance data (i.e. Geo-Objects) to the system.

### Explorer <a href="#explorer" id="explorer"></a>

This widget is used to explore and manage Geo-Objects with a more map centric user experience.
