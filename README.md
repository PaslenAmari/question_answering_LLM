# question_answering_LLM
Вопросно-ответный поиск в промышленной отрасли

![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/ce92cee5-d5a1-4429-84f2-0a8754c4c724)


Загрузим данные для обучения 
![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/605bd233-be90-4c75-8c2c-99683ff0f44c)

![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/a76d07d0-0fb8-4318-aacc-d3c9a1f36269)

Проведем обработку данных
![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/89df5ebb-6747-4a63-92b6-9ee1a10fd2a3)


![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/486ac1e1-03f9-42a9-9109-e01e9286c3f6)

Посмотрим другие модели LLM

![image](https://github.com/PaslenAmari/question_answering_LLM/assets/106679149/774162d3-ea64-4f1f-8f5c-cddc36544f9c)



Выводы:

Предобученная модель DistilBert выдаёт готовый ответ за счет моделирование языка по маске (BERT делал это с помощью MLM и Next Sentence Prediction) и обучения с использованием тройного лосса.

*(P.S. модель Bert не рассматривалсь, т.к. DistilBERT нацелен на оптимизацию обучения за счет уменьшения размера и увеличения скорости BERT. Также, DistilBERT весит на 40% меньше, чем оригинальная BERT-модель, она на 60% быстрее ее и сохраняет 97% ее функциональности)*

Мы посмотрели применение TF-IDF и Word2Vec, где accuracy для TF-IDF была намного выше.

Тогда как минус TF-IDF в том, что он выдает похожие по контексту: алгоритм способен вычислить сходство только между вопросами и документами, в которых представлены одни и те же слова, поэтому он не может улавливать синонимы; и не может понять контекст вопроса или значение слов.

Для получения готового ответа выгоднее использовать предобученную модель DistilBert. Из возможных дальнейших шагов докрутки - это настройка ответа имён собсвтенных с заглавной буквы, как и в источнике информации, откуда берется ответ.
