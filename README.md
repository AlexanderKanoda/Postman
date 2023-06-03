# Postman
## HW_1 Postman
### Создать запросы в Postman:
### **Protocol: http**
### **IP: 162.55.220.72**
### **Port: 5005**
___

#### *EP_1*
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
] 
___

#### *EP_2*
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
___

#### *EP_3*
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
___

#### *EP_4*
Method: GET
EndPoint: /object_info_2
request url params: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
___

#### *EP_5*
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
___

#### *EP_6*
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
___

#### *EP_7*
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
___

## HW_2 Postman

*http://162.55.220.72:5005/first*

1. Отправить запрос.
2. Статус код 200
3. Проверить, что в body приходит правильный string.
___

*http://162.55.220.72:5005/user_info_3*

4. Отправить запрос.
5. Статус код 200
6. Спарсить response body в json.
7. Проверить, что name в ответе равно name s request (name вбить руками.)
8. Проверить, что age в ответе равно age s request (age вбить руками.)
9. Проверить, что salary в ответе равно salary s request (salary вбить руками.)
10. Спарсить request.
11. Проверить, что name в ответе равно name s request (name забрать из request.)
12. Проверить, что age в ответе равно age s request (age забрать из request.)
13. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
14. Вывести в консоль параметр family из response.
15. Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)
___

*http://162.55.220.72:5005/object_info_3*

16.  Отправить запрос.
17.  Статус код 200
18. Спарсить response body в json.
19. Спарсить request.
20. Проверить, что name в ответе равно name s request (name забрать из request.)
21. Проверить, что age в ответе равно age s request (age забрать из request.)
22. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
23. Вывести в консоль параметр family из response.
24. Проверить, что у параметра dog есть параметры name.
25. Проверить, что у параметра dog есть параметры age.
26. Проверить, что параметр name имеет значение Luky.
27. Проверить, что параметр age имеет значение 4.
___

*http://162.55.220.72:5005/object_info_4*

28. Отправить запрос.
29. Статус код 200
30. Спарсить response body в json.
31. Спарсить request.
32. Проверить, что name в ответе равно name s request (name забрать из request.)
33. Проверить, что age в ответе равно age из request (age забрать из request.)
34. Вывести в консоль параметр salary из request.
35. Вывести в консоль параметр salary из response.
36. Вывести в консоль 0-й элемент параметра salary из response.
37. Вывести в консоль 1-й элемент параметра salary параметр salary из response.
38. Вывести в консоль 2-й элемент параметра salary параметр salary из response.
39. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)
40. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)
41. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)
42. Создать в окружении переменную name
43. Создать в окружении переменную age
44. Создать в окружении переменную salary
45. Передать в окружение переменную name
46. Передать в окружение переменную age
47. Передать в окружение переменную salary
48. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.
___
*http://162.55.220.72:5005/user_info_2*

49.  Вставить параметр salary из окружения в request.
50.  Вставить параметр age из окружения в age
51. Вставить параметр name из окружения в name
52. Отправить запрос.
53. Статус код 200
54. Спарсить response body в json.
55. Спарсить request.
56. Проверить, что json response имеет параметр start_qa_salary
57. Проверить, что json response имеет параметр qa_salary_after_6_months
58. Проверить, что json response имеет параметр qa_salary_after_12_months
59. Проверить, что json response имеет параметр qa_salary_after_1.5_year
60. Проверить, что json response имеет параметр qa_salary_after_3.5_years
61. Проверить, что json response имеет параметр person
62. Проверить, что параметр start_qa_salary равен salary из request (salary забрать из request.)
63. Проверить, что параметр qa_salary_after_6_months равен salary*2 из request (salary забрать из request.)
64. Проверить, что параметр qa_salary_after_12_months равен salary*2.7 из request (salary забрать из request.)
65. Проверить, что параметр qa_salary_after_1.5_year равен salary*3.3 из request (salary забрать из request.)
66. Проверить, что параметр qa_salary_after_3.5_years равен salary*3.8 из request (salary забрать из request.)
67. Проверить, что в параметре person, 1-й элемент из u_name равен salary из request (salary забрать из request.)
68. Проверить, что что параметр u_age равен age из request (age забрать из request.)
69. Проверить, что параметр u_salary_5_years равен salary*4.2 из request (salary забрать из request.)