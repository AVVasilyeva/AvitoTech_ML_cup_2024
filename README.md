AvitoTech ML cup 2024
Соревнование от AvitoTech по рекомендации наиболее релевантных рекламных объявлении для пользователей.

Задача соревнования
Разработать модель, которая сможет рекомендовать пользователю наиболее релевантную рекламу на основе реальных данных после анонимизации. 
Модель должна предсказывать вероятность того, что пользователь кликнет на рекламное объявление, исходя из его характеристик и предпочтений. 

Моё решение - это усреднение выходов 5 моделей CatBoost, обучавшихся с одинаковыми параметрами, но на датасетах, по-разному сэмплированных из исходного.
Первый датасет включал только юзеров, встречающихся в тестовом датасете.
Второй только creative_id, встречающиеся в тестовом датасете.
Третий сформирован из юзеров, которые делали хотя бы 1 клик и из adv_campaign_id где есть хотя бы 1 клик.
Остальные два сформированы из всех кликов и случайно отобранных не-кликов в пропорции 1:15.
