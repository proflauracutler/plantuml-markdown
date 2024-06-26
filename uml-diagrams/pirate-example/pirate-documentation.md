# Pirate Example

## ERD:

![pirate-ERD](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/proflauracutler/plantuml-markdown/master/uml-diagrams/pirate-example/pirate-erd.plantuml)

## Mermaid flowchart with end nodes: 
```mermaid
flowchart TD
    A[Start] --> Add[Librarian adds new books to the system]
Add --> Search[Member searches for books]
Search --> Available{Is book available?}
Available -->|Yes| Borrow[Member borrows book]
Borrow --> EndAvailable(( ))
Available -->|No| EndAvailable
EndAvailable --> E[End]

```
## Mermaid flowchart: 
```mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

```


## Mermaid ERD: 
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER {
        string name
        string custNumber
        string sector
    }
    ORDER ||--|{ LINE-ITEM : contains
    ORDER {
        int orderNumber
        string deliveryAddress
    }
    LINE-ITEM {
        string productCode
        int quantity
        float pricePerUnit
    }
```

## Geo JSON
```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```

