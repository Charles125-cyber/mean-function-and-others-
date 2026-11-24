# Function 1: Calculate the sum of numbers
def total_sum(numbers):
    return sum(numbers)


# Function 2: Calculate the average (mean)
def average(numbers):
    if len(numbers) == 0:
        return 0
    return sum(numbers) / len(numbers)


# Function 3: Calculate the median and mode
def median_mode(numbers):
    from statistics import median, mode

    if len(numbers) == 0:
        return None, None

    med = median(numbers)

    try:
        mod = mode(numbers)
    except:
        mod = "No mode"

    return med, mod


# Main program
numbers = [2, 4, 4, 6, 8, 10]

print("Numbers:", numbers)
print("Sum:", total_sum(numbers))
print("Average:", average(numbers))

med, mod = median_mode(numbers)

print("Median:", med)
print("Mode:", mod)
