# Анкета «Киножуй» — визуальная схема

```mermaid
%%{init: {"theme": "neutral", "themeVariables": {"fontFamily": "Segoe UI"}}}%%
flowchart TD
    classDef b1 fill:#E3F2FD,stroke:#1E88E5,color:#0D47A1,stroke-width:2px
    classDef b2 fill:#E8F5E9,stroke:#2E7D32,color:#1B5E20,stroke-width:2px
    classDef b3 fill:#FFF8E1,stroke:#F9A825,color:#F57F17,stroke-width:2px
    classDef b4 fill:#F3E5F5,stroke:#6A1B9A,color:#4A148C,stroke-width:2px
    classDef b5 fill:#FFF3E0,stroke:#EF6C00,color:#E65100,stroke-width:2px
    classDef b6 fill:#ECEFF1,stroke:#455A64,color:#263238,stroke-width:2px
    classDef end fill:#CFD8DC,stroke:#37474F,color:#263238,font-weight:bold

    start((Старт)) --> B1Q1

    subgraph B1["Блок 1. Общие данные"]
        direction TB
        B1Q1["(1) Пол — мужской / женский"]
        B1Q2["(2) Возраст — до 18, 18–25, 26–35, 35–45, 45–60, 60+"]
        B1Q3{"(3) Смотрели Киножуй<br/>за прошлый месяц?"}
    end
    class B1 b1

    B1Q1 --> B1Q2 --> B1Q3
    B1Q3 -->|Да| B2Q4
    B1Q3 -->|Нет| EndEarly[[Завершение анкеты]]

    subgraph B2["Блок 2. Стабильность интернета"]
        direction TB
        B2Q4["(4) Название последнего фильма (текст)"]
        B2Q5["(5) Досмотрели до конца? — Да / Нет"]
        B2Q6["(6) Были ли зависания — 0 / 1 / 2–3 / 4+"]
        B2Q7["(7) Стабильность интернета — низкое / среднее / высокое"]
    end
    class B2 b2

    subgraph B3["Блок 3. Влияние рекламы"]
        direction TB
        B3Q8["(8) Была реклама? — Да / Нет / Не помню"]
        B3Q9["(9) Насколько раздражала — шкала 1–5"]
        B3Q10["(10) Влияние рекламы — прервал / раздражало / не заметил / другое"]
    end
    class B3 b3

    subgraph B4["Блок 4. Подписка на конкурентов"]
        direction TB
        B4Q11["(11) Есть подписка на конкурентов? — Да / Нет"]
        B4Q12["(12) Какие сервисы — Фильмбокс / Иви / Кинопоиск / Netflix / другое"]
        B4Q13["(13) Преимущества других сервисов (текст)"]
        B4Q14["(14) Как часто выбираете Киножуй — чаще / поровну / реже / трудно сказать"]
    end
    class B4 b4

    subgraph B5["Блок 5. Отношение к антисоциальному поведению"]
        direction TB
        B5Int["(15–22) Нетерпимость — 8 утверждений, шкала 1–5"]
        B5Tol["(23–30) Толерантность — 8 утверждений, шкала 1–5"]
    end
    class B5 b5

    subgraph B6["Блок 6. Результаты"]
        direction TB
        B6Q31["(31) Получить результаты? — Да (e‑mail) / Нет"]
    end
    class B6 b6

    B2Q7 --> B3Q8
    B3Q10 --> B4Q11
    B4Q14 --> B5Int
    B5Tol --> B6Q31
    B6Q31 --> EndFinal[[Конец анкеты]]

    class EndEarly,EndFinal end
```
