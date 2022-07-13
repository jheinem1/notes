
Associations denote relationships between classes.

The multiplicity of an association end denotes how many objects the instance of a class can legitimately reference.

```mermaid
classDiagram
    class TarifSchedule {
        enum getZones()
        Price getPrice()
    }
    class TripLeg {
        Price price
        Zone zone
    }
    TarifSchedule "*" -- "*" TripLeg
```
^overview
## 1-to-1 Associations
```mermaid
classDiagram
    class Country {
        string name
    }
    class CapitalCity {
        string name
    }
    Country "1" -- "1" CapitalCity
```
## 1-to-Many Associations
```mermaid
classDiagram
    class Polygon {
        void draw()
    }
    class Point {
        number x
        number y
    }
    Polygon -- "*" Point
```
## Many-to-Many Associations
```mermaid
classDiagram
    StockExchange "*" -- "*" Company
    class Company {
        string tickerSymbol
    }
```