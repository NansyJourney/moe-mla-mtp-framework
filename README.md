# Проект

Данный проект выполнен в рамках курса «Анализ текстов. Генеративные модели» и посвящён реализации и исследованию трёх современных алгоритмов:
* **MLA (Multi-Head Latent Attention)**
* **MoE (Mixture of Experts с Noisy Top-K Gate Feed-Forward)** — включает обучение с добавлением шума
* **MTP (Multi-Token Prediction)**

## Постановка задачи
В качестве основы для проекта был предоставлен базовый пример, ориентированный на применение перечисленных алгоритмов к задаче **символьной языковой модели (character-level language model).**

Модель обучается на корпусе имён и фамилий.

**Вход**: начальный текст (например, «Красотка» — имя или фрагмент фамилии).
**Задача**: продолжить последовательность символов, генерируя имя или фамилию до тех пор, пока не будет сгенерирован символ конца последовательности либо не будет достигнута максимальная длина.

## Реализованные модели
В ходе выполнения проекта были реализованы следующие варианты GPT-подобных моделей:
1. GPT с MoE Noisy Top-K Gate Feed-Forward
2. GPT с RoPE и Multi-Head Latent Attention
3. GPT с Multi-Token Prediction (MTP)

## Структура проекта
Рекомендуется изучать ноутбуки в порядке, в котором они представлены в списке выше.

Первые два ноутбука приводят к следующей архитектуре модели:
![68747470733a2f2f73656261737469616e72617363686b612e636f6d2f696d616765732f4c4c4d732d66726f6d2d736372617463682d696d616765732f626f6e75732f6d6f652d6d656d6f72792f312e77656270](https://github.com/user-attachments/assets/b4c576b9-46f8-4d2e-b54d-3d0722feecfa)
![68747470733a2f2f73656261737469616e72617363686b612e636f6d2f696d616765732f4c4c4d732d66726f6d2d736372617463682d696d616765732f626f6e75732f6d6c612d6d656d6f72792f312e77656270](https://github.com/user-attachments/assets/77a6e37d-ac8d-4de6-9336-5572c1943c14)

Для реализации модели **GPT с Multi-Token Prediction** потребовалось воспроизвести следующую архитектуру:
<img width="623" height="298" alt="image" src="https://github.com/user-attachments/assets/d8c1f93b-42e3-41b5-841d-20e1282dd0c7" />

## Используемые ресурсы
Все архитектуры основаны на идеях и решениях, применяемых в модели DeepSeek, и требовали их воспроизведения и адаптации. В работе использовались следующие источники:
1. https://github.com/rasbt/LLMs-from-scratch/tree/main/ch04/05_mla
2. https://github.com/rasbt/LLMs-from-scratch/tree/main/ch04/07_moe
3. https://llmstudio.ru/blog/mixture-of-experts-moe
4. https://arxiv.org/pdf/2412.19437
5. https://github.com/Mayankpratapsingh022/DeepSeek-from-Scratch/blob/main/notebooks/Multi_Token_Prediction_from_Scratch.ipynb
