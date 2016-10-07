# Общее описание

[CommAI-env](https://github.com/facebookresearch/CommAI-env) (Environment for Communication-based AI) - это платформа для обучения
и тестирования ИИ как описано в статье A Roadmap towards Machine Intelligence.

В платформе представлены следующие базовые сущности:
- Ученик,
- Окружение,
- Время,
- Награда,
- Задачи.

Ученик взаимодействует с Окружением. Окружение просит Ученика решать Задачи. За каждую
успешно решенную Задачу назначается Награда.
Взаимодействие Ученика с Окружением осуществляется в определенный момент Времени.

Задачи даются Ученику в случайном порядке.

# Конфигурация CommAI

Конфигурация CommAI осуществляется через json файл:
- задается Окружение ("worlds.grid_world.GridWorld"),
- список Задач ("type": "tasks.competition.repetition.RepeatCharacterTask", "world": "gw"),
- планировщик - то в каком порядке запускать задачи ("core.scheduler.RandomTaskScheduler").

# Конфигурация Ученика

Ученик должен реализовывать следующий интерфейс:

```
from learners.base import BaseLearner

class MySmartLearner(BaseLearner):
    def reward(self, reward):
        # record receiving a reward

    def next(self, input_bit):
        # figure out what should be
        # the next bit to be spoken
        return next_bit
```

# Примеры Задач

[Задачи](https://github.com/facebookresearch/CommAI-env/blob/master/TASKS.md) разные - начиная от повторения написанного Окружением, заканчивая логическим выводом
и подсчетом количества элементов в инвентаре.

Можно придумывать и дописывать свои задачи.

Пример:

```
Moving Forward [G2][IMP]

    Description: Learner is asked to move forward.
    Instructions: You will have to move forward.
    Example:
        Teacher: Move forward.
        Learner: I move forward.
        Teacher: You moved [+1].
    Motivation: Teach the learner to move in whatever direction.
    Rewards: +1 for correct answer
    MaxTime: Len(Instructions) + 3 TIME_MOVE
    Prerequisites: repeating strings in context, "I do-X" construction
    Teacher inputs: Move forward.
```

# Впечатления

Из отрицательного (проект на стадии бета-тестирования):
- плохой консольный интерфейс,
- непонятно как взаимодействовать с Окружением (какие команды вводить),
становится понятно только после прочтения документации,
- почти нет обратной связи с Окружением при решении задачи, т.е. я ввожу неправильные
команды, а Окружение ничего не сообщает - ни ошибки, ни пояснения, ничего.
- команды сильно детерминированы, например, если забуду точку в конце, то
Окружение никак не отреагирует,
- нет отдельной сущности Учителя.

Из положительного:
- неплохой код,
- неплохая документация,
- проект развивается,
- можно расширять и дописывать (Задачи, Окружение, Ученика, ...).


