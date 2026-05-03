# parol-generator
Генератор надежных паролей на Python
### Шаг 1. Запустите скрипт (например на сайте: https://www.online-python.com/ )
### шаг 2. Введите желаемую длину пароля
### шаг 3. ответьте на вопросы 
### Шаг 4. Получите готовый пароль
### Шаг 5. Сохрани
### Шаг 6. Готово!

Код программы:
#### import secrets as s
#### import string as st
####
#### l = int(input("Длина пароля: "))
#### d = input("Цифры? (y/n/д/н): ").lower() in ('y','yes','д','да')
#### u = input("Заглавные? (y/n/д/н): ").lower() in ('y','yes','д','да')
#### w = input("Строчные? (y/n/д/н): ").lower() in ('y','yes','д','да')
#### p = input("Символы !@#$? (y/n/д/н): ").lower() in ('y','yes','д','да')
####
#### c = ''
#### if d: c += st.digits
#### if u: c += st.ascii_uppercase
#### if w: c += st.ascii_lowercase
#### if p: c += '!@#$%'
#### if not c: c = st.digits + st.ascii_letters + '!@#$%'
####
#### pw = ''.join(s.choice(c) for _ in range(l))
#### print("\nВаш пароль:", pw)
