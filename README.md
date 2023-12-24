# Max-numbers

def find_max_numbers(arr):
    first_max = float('-inf')
    second_max = float('-inf')
    third_max = float('-inf')

    for num in arr:
        if num > first_max:
            third_max = second_max
            second_max = first_max
            first_max = num
        elif num > second_max:
            third_max = second_max
            second_max = num
        elif num > third_max:
            third_max = num

    print(first_max, second_max, third_max)

if __name__ == "__main__":
    try:
        T = int(input())
        for _ in range(T):
            N = int(input())
            A = list(map(int, input().split()))
            find_max_numbers(A)
    except EOFError:
        pass
