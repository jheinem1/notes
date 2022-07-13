
![](/assets/images/2022-01-18-13-21-25.png)

```mermaid
classDiagram
    class Indian {
        Hair
        Dress()
        Smile()
        Sleep()
    }
    Indian *-- Face
    class Face {
        Nose
        smile()
        close_eye()
    }
    Face *-- "*" Ear
    class Ear {
        Size
        listen()
    }
    Face *-- Mouth
    class Mouth {
        NrOfTheeths
        Size
        open()
        speak()
    }
```