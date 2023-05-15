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
Teacher ->> Game : new Game
Game ->> Teacher : sendCode
Teacher ->> Students : showCode
Students ->> Game : joinGame
Game ->> Teacher : sendQuestion
Teacher ->> Students : showNextQuestion
Students ->> Game : answer
Game ->> Teacher : sendScoreboard
Teacher ->> Students : showNextQuestion
```

