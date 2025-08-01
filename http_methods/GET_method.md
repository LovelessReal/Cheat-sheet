| №  | Проверка                                                                 | Ожидаемый результат                                                                  
|----|--------------------------------------------------------------------------|------------------------------------------------------------------
| 1  | Отправка запроса методом GET по корректному URL                          | 🟢 Ответ 200 OK, данные возвращаются в ожидаемом формате                             
| 2  | GET-запрос к несуществующему ресурсу                                     | 🔴 Ответ 404 Not Found                                                               
| 3  | GET-запрос без обязательных параметров                                   | 🔴 Ответ 400 Bad Request или сообщение об ошибке в теле                              
| 4  | GET-запрос с невалидными параметрами (напр. id=abc)                      | 🔴 Ответ 400 Bad Request или валидное сообщение об ошибке                            
| 5  | GET-запрос с валидными параметрами                                       | 🟢 Ответ 200 OK, данные соответствуют переданным параметрам                          
| 6  | Повторный GET-запрос с теми же параметрами                               | 🟢 Ответ идентичен предыдущему (идемпотентность)                                     
| 7  | Ответ содержит только необходимые и разрешённые поля                     | 🟢 Нет лишних/чувствительных данных (например, паролей)                             
| 8  | Проверка формата данных в ответе (JSON/XML)                              | 🟢 Структура и формат соответствуют документации                                     
| 9  | Проверка значений полей в ответе                                         | 🟢 Типы данных и значения корректны, соответствуют документации                     
| 10 | Проверка поведения при большом объёме данных                             | 🟢 Ответ 200 OK, нет таймаута или ошибок                                             
| 11 | GET-запрос с фильтрацией (например, ?status=active)                      | 🟢 Ответ содержит только отфильтрованные данные                                     
| 12 | GET-запрос с пагинацией (?page=2&limit=10)                               | 🟢 Ответ содержит соответствующую порцию данных                                      
| 13 | GET-запрос с авторизацией (если требуется)                               | 🟢 Ответ 200 OK при валидном токене, 401/403 при отсутствии                         
| 14 | Проверка заголовков ответа (Content-Type, Cache-Control)                 | 🟢 Заголовки присутствуют и соответствуют требованиям                                
| 15 | GET-запрос на кэшируемый ресурс                                          | 🟢 Возвращаются корректные заголовки ETag или Last-Modified                          
| 16 | Попытка доступа к чужим данным (GET /users/123)                          | 🔴 Ответ 403 Forbidden или 404 Not Found (если нет доступа)                          
| 17 | Ввод SQL-инъекции в параметр (?id=1' OR '1'='1)                          | 🟢 Сервер возвращает безопасный ответ или ошибку валидации                           
| 18 | Ответ при пустом результате (например, ?search=xyz)                      | 🟡 Возвращается пустой массив или сообщение «ничего не найдено»                      
| 19 | Ответ на разных браузерах или клиентах                                   | 🟢 Одинаковое поведение и структура ответа                                           
| 20 | GET-запрос без тела                                                      | 🟢 Запрос успешно обрабатывается (GET не должен содержать body)                      
