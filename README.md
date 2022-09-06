# AA_and_AB_tests
1.AA-тест проведен для корректности работы системы сплитирования.  А также чтобы убедиться в том, что ключевая метрика не отличается между 0 и 1 группой не только в АА-тесте, но и в целом для всех данных

2.AB-тест 1 проведен для сравнения групп 1 и 2 после проведения эксперимента. В группе 2 был использован один из новых алгоритмов рекомендации постов, группа 1 использовалась в качестве контроля

3.AB-тест 2 проведен для сравнения групп (1 и 2) и (0 и 3) после проведения эксперимента. В группах 2 и 3 был использован один из новых алгоритмов рекомендации постов, группы 1 и 0 использовались в качестве контроля.  
В отличии от теста 1 была использована метрика линеаризованные лайки:
 Считаем общий CTR в контрольной группе 𝐶𝑇𝑅𝑐𝑜𝑛𝑡𝑟𝑜𝑙=𝑠𝑢𝑚(𝑙𝑖𝑘𝑒𝑠)/𝑠𝑢𝑚(𝑣𝑖𝑒𝑤𝑠).
 Посчитаем в обеих группах поюзерную метрику 𝑙𝑖𝑛𝑒𝑎𝑟𝑖𝑧𝑒𝑑_𝑙𝑖𝑘𝑒𝑠=𝑙𝑖𝑘𝑒𝑠−𝐶𝑇𝑅𝑐𝑜𝑛𝑡𝑟𝑜𝑙∗𝑣𝑖𝑒𝑤𝑠.  
 После чего сравним t-тестом отличия в группах по метрике 𝑙𝑖𝑛𝑒𝑎𝑟𝑖𝑧𝑒𝑑_𝑙𝑖𝑘𝑒𝑠.
Метод использовался для увеличения чувствительности метрики. 

