I created a caesar cipher in python to encrypt text that was input into the code

plainText = input("What is your plaintext? ")
shift = int(input("What is your shift? "))

def caesar(plainText, shift): 
  cipherText = ""
  for ch in plainText:
    if ch.isalpha():
      stayInAlphabet = ord(ch) + shift 
      if stayInAlphabet > ord('z'):
        stayInAlphabet -= 26
      finalLetter = chr(stayInAlphabet)
      cipherText += finalLetter
  print ("Your ciphertext is: ", cipherText)
  return cipherText


caesar(plainText, shift)


it works by answering  "What is your plaintext?"
then answering "What is your shift"
the code will then encrypt whatever you answered for plaintext
