def tally(text):
 qwe = {}
 for letter in text:
 if letter in qwe:
 qwe.update({letter:qwe.get(letter)+1})
 else:
 qwe.update({letter:1})
 for key in sorted(qwe.keys()):
 print (key, '=', qwe[key],end=". ") 
 print('')
alphabet = "абвгдеёжзийклмнопрстуфхцчшщъыьэюяабвгдеёжзийклмнопрстуфхцчшщъыьэюя"
encript = input("Введите текст для шифрования: ")
key = int(input("Введите число на сколько символов шифровать от 1 до 30: "))
encript = encript.lower()
desencripted = ""
encripted = ""
for letter in encript:
 position = alphabet.find(letter)
 newPosition = position + key
 if letter in alphabet:
 encripted = encripted + alphabet[newPosition]
 else:
 encripted = encripted + letter
print("зашифрованный текст: ", encripted)
for letter in encripted:
 position = alphabet.find(letter)
 newPosition = position - key
 if letter in alphabet:
 desencripted += alphabet[newPosition]
 else:
 desencripted += letter
print("разшифрованный текст: ",desencripted)
print("символы в оригинальном тексте:")
tally(encript)
print("символы в зашифрованном тексте:")
tally(encripted)
