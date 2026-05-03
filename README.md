# parol-generator
Генератор надежных паролей на Python
Код программы:

import secrets as s
import string as st

l = int(input("Длина пароля: "))
d = input("Цифры? (y/n/д/н): ").lower() in ('y','yes','д','да')
u = input("Заглавные? (y/n/д/н): ").lower() in ('y','yes','д','да')
w = input("Строчные? (y/n/д/н): ").lower() in ('y','yes','д','да')
p = input("Символы !@#$? (y/n/д/н): ").lower() in ('y','yes','д','да')

c = ''
if d: c += st.digits
if u: c += st.ascii_uppercase
if w: c += st.ascii_lowercase
if p: c += '!@#$%'
if not c: c = st.digits + st.ascii_letters + '!@#$%'

pw = ''.join(s.choice(c) for _ in range(l))
print("\nВаш пароль:", pw)

