# Password-Generator
import random
import string
def generate_password(length):
  charcters = string.ascii_letters + string.digits + string.punctuation
  password = ''.join(random.choice(charcters) 
for i in range(length))
  return password
def main():
  print("Welcome to the Password Generator")
  try:
    length = int(input("Enter the length of password:"))
    if length < 1:
      print("Password length should be atleast 1")
    else:
      password = generate_password(length)
      print(f"Generated Password: {password}")
  except ValueError:
    print("Invalid input! Please enter a valid number")
if __name__ == "__main__":
    main()
