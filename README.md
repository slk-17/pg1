# pg1
def find_primes(arr):
    primes = []
    for num in arr:
        if num < 2:
            continue  
        is_prime = True
        for i in range(2, int(num ** 0.5) + 1):  
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            primes.append(num)
    return primes

arr = [10, 15, 3, 7, 19, 23, 4, 5, 11]
primes = find_primes(arr)
print(f"Prime numbers in the array: {primes}")
