# РЎС…РµРјР° РѕРїСЂРѕСЃР° В«РљРёРЅРѕР¶СѓР№В»

```mermaid
%%{init: {"theme": "neutral", "themeVariables": {"fontFamily": "Segoe UI"}}}%%
flowchart TD
    classDef b1 fill:#E3F2FD,stroke:#1E88E5,color:#0D47A1,stroke-width:2px
    classDef b2 fill:#E8F5E9,stroke:#2E7D32,color:#1B5E20,stroke-width:2px
    classDef b3 fill:#FFF8E1,stroke:#F9A825,color:#F57F17,stroke-width:2px
    classDef b4 fill:#F3E5F5,stroke:#6A1B9A,color:#4A148C,stroke-width:2px
    classDef b5 fill:#FFF3E0,stroke:#EF6C00,color:#E65100,stroke-width:2px
    classDef b6 fill:#ECEFF1,stroke:#455A64,color:#263238,stroke-width:2px
    classDef endNode fill:#CFD8DC,stroke:#37474F,color:#263238,font-weight:bold

    start(Старт)
    B1[  Блок 1. Общие данные
  (1) Пол — мужской / женский
  (2) Возраст — до 18, 18–25, 26–35, 35–45, 45–60, 60+
  (3) Смотрели Киножуй в прошлом месяце?]:::b1
    B2[  Блок 2. Стабильность интернета
  (4) Последний фильм (текст)
  (5) Досмотрели? — Да / Нет
  (6) Были зависания — 0 / 1 / 2–3 / 4+
  (7) Оцените стабильность — низкая / средняя / высокая]:::b2
    B3[  Блок 3. Влияние рекламы
  (8) Реклама была? — Да / Нет / Не помню
  (9) Насколько раздражала — шкала 1–5
  (10) Как повлияла реклама — прервал просмотр / раздражало / не заметил / другое]:::b3
    B4[  Блок 4. Подписки на конкурентов
  (11) Есть подписки? — Да / Нет
  (12) Какие сервисы — Фильмбокс / Иви / Кинопоиск / Netflix / другое
  (13) Преимущества конкурентов (текст)
  (14) Как часто выбираете Киножуй — чаще / поровну / реже / трудно сказать]:::b4
    B5[  Блок 5. Отношение к антисоциальному поведению
  (15–22) Нетерпимость — 8 утверждений, шкала 1–5
  (23–30) Толерантность — 8 утверждений, шкала 1–5]:::b6
    EndEarly[  Блок 6. Завершение
  (31) Получить результаты? — Да (e-mail) / Нет]:::endNode
    EndFinal[Конец анкеты]:::endNode

    class start endNode

    start --> B1
    B1 -->|Р”Р°| B2
    B1 -->|РќРµС‚| EndEarly
    B2 --> B3 --> B4 --> B5 --> B6 --> EndFinal
```
