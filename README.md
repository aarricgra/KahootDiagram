# KahootDiagram

## Class Diagram
```mermaid
classDiagram

class Teacher{
    void showCode()
    void showNextQuestion()
    void showScoreboard()
}

class Game{
    +List<Player> Players
    +List<Question> Questions
    +int Code

    void addPlayer()
    Preguntas sendNewQuestion()
    void asignPoints(int points)
    List<String> sendScoreboard()
}

Game o-- Player
Game o-- Question

class Player{
    +String Name
    +int Points

    void joinGame(int code)
    void answer()
    void addPoints(int points)
}

class Question{
    +List<String> IncorrectAnswers
    +String CorrectAnswer
    +String Statement

    void showQuestion()
}
```
## Sequence Diagram

```uml-sequence-diagram
Title: Hello world example
Bob->Alice: Hello
Alice-->Bob: How are you?
Note left of Bob: Bob thinks
Bob->>Alice: I'm good, thanks! How about you?
Alice-->Bob: I'm doing great, thank you!
```

