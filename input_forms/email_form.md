| №  | Проверка                                                       | Ожидаемый результат                             
|----|----------------------------------------------------------------|-----------------------------------------
| 1  | Пустое поле email                                              | 🔴 Сообщение о незаполненном поле email         
| 2  | Email в нижнем регистре                                        | 🟢 Значение поля принимается                    
| 3  | Email в верхнем регистре                                       | 🟢 Значение поля принимается                    
| 4  | Email с цифрами в имени пользователя                           | 🟢 Значение поля принимается                    
| 5  | Email с цифрами в доменной части                               | 🟢 Значение поля принимается                    
| 6  | Email с дефисом в имени пользователя                           | 🟢 Значение поля принимается                    
| 7  | Email с дефисом в доменной части                               | 🟢 Значение поля принимается                    
| 8  | Email с подчеркиванием в имени пользователя                    | 🟢 Значение поля принимается                    
| 9  | Email с точками в имени пользователя                           | 🟢 Значение поля принимается                    
| 10 | Email с несколькими точками в доменной части                   | 🟢 Значение поля принимается                    
| 11 | Email без точек в доменной части                               | 🔴 Сообщение о некорректном email               
| 12 | Превышение длины email (>320 символов)                         | 🔴 Сообщение о некорректном email               
| 13 | Отсутствие @ в email                                           | 🔴 Сообщение о некорректном email               
| 14 | Email с пробелами в имени пользователя                         | 🔴 Сообщение о некорректном email               
| 15 | Email с пробелами в доменной части                             | 🔴 Сообщение о некорректном email               
| 16 | Email без имени пользователя                                   | 🔴 Сообщение о некорректном email               
| 17 | Email без доменной части                                       | 🔴 Сообщение о некорректном email               
| 18 | Некорректный домен первого уровня (например, `.ruuuu`)         | 🔴 Сообщение о некорректном email               
| 19 | Email с кириллическим доменным именем (`login@домен.рф`)       | 🟢 Значение поля принимается                    
