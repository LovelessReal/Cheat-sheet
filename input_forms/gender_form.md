| №  | Проверка                                                            | Ожидаемый результат
|----|---------------------------------------------------------------------|---------------------------------------------------------------------------
| 1  | Отображение поля на форме                                           | 🟢 Поле отображается корректно, с понятной подписью (например, «Пол») 
| 2  | Доступные значения                                                  | 🟢 Значения соответствуют требованиям (например: «М», «Ж», «Не указывать») 
| 3  | Поле обязательно для заполнения                                     | 🟡 Только если это требуется — иначе должно быть необязательным 
| 4  | Отправка без выбора значения                                        | 🟡 Допустимо, если поле необязательное; 🔴 Ошибка, если обязательное 
| 5  | Отправка с некорректным значением (например, "robot")               | 🔴 Ошибка валидации, значение отклоняется 
| 6  | Отправка валидного значения                                         | 🟢 Значение сохраняется и отображается корректно 
| 7  | Сброс значения после отправки формы                                 | 🟢 Форма сбрасывается, значение по умолчанию отсутствует 
| 8  | Корректное отображение выбранного значения при редактировании       | 🟢 Предустановленное значение отображается при повторном открытии формы 
| 9  | Поддержка локализации/переводов                                     | 🟢 Значения и подписи отображаются на нужном языке 
| 10 | Навигация с клавиатуры и доступность                                | 🟢 Возможность выбора значения с клавиатуры, поддержка screen reader 
| 11 | Поддержка табличного ввода (при наличии форм в виде таблиц)         | 🟢 Поле выбирается без багов, не сбивает другие поля 
| 12 | Возможность изменить значение после выбора                          | 🟢 Пользователь может изменить выбор до и после отправки 
| 13 | Поведение при обновлении данных с сервера                           | 🟢 Выбранное значение синхронизируется с серверными данными 
| 14 | Проверка валидации на клиенте                                       | 🟢 Ошибки отображаются корректно, если значение отсутствует при обязательности 
| 15 | Проверка валидации на сервере                                       | 🟢 Сервер обрабатывает и валидирует значение независимо от клиента 
