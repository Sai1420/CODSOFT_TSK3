import random
import string

# Function to generate a random password
def generate_password(length):
    # Define character sets for each category
    uppercase_letters = string.ascii_uppercase
    lowercase_letters = string.ascii_lowercase
    digits = string.digits
    special_characters = string.punctuation

    # Combine character sets
    all_characters = uppercase_letters + lowercase_letters + digits + special_characters

    # Ensure the password length is at least 8 characters
    if length < 8:
        print("Password length should be at least 8 characters.")
        return None

    # Generate a random password
    password = ''.join(random.choice(all_characters) for _ in range(length))
    return password

# Main function
def main():
    print("Password Generator")
    length = int(input("Enter the desired password length: "))

    password = generate_password(length)

    if password:
        print(f"Generated Password: {password}")

if __name__ == "__main__":
    main()
