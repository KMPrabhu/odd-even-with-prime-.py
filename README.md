print("1. Even or Odd")
print("2. Prime or Not")
print("3. Exit")
ch = int(input("Enter a choice: "))
match ch:
    case 1:
        total = int(input("enter the total numbers :"))
        for i in range(total):
            a = int(input("Enter a number: "))
            if a % 2 == 0:
                print(a, "is an Even number")
            else:
                print(a, "is an Odd number")
    case 2:
        def is_prime(num):
            if num <= 1:
                return False
            for i in range(2, int(num**0.5) + 1):
                if num % i == 0:
                    return False
            return True
        num = int(input("Enter a number: "))
        if is_prime(num):
            print(num, "is a Prime Number")
        else:
            print(num, "is Not a Prime Number")
    case 3:
        print("Exiting the program.")
    case _:
        print("Invalid Choice")
