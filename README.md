# Create an iterator for range(3): small_value
small_value = iter(range(3))
# Print the values in small_value
print(next(small_value))
print(next(small_value))
print(next(small_value))
# Loop over range(3) and print the values
for num in range(3):
    print(num)
# Create an iterator for range(10 ** 100): googol
googol = iter(range(10 ** 100))
# Print the first 5 values from googol
print(next(googol))
print(next(googol))
print(next(googol))
print(next(googol))
print(next(googol))

# Create a list of strings: mutants
mutants = ['charles xavier', 'bobby drake', 'kurt wagner', 'max eisenhardt', 'kitty pryde']
# Create a list of tuples: mutant_list
mutant_list = list(enumerate(mutants))
# Print the list of tuples
print(mutant_list)
# Unpack and print the tuple pairs
for index1, value1 in enumerate(mutants):
    print(index1, value1)
# Change the start index
for index2, value2 in enumerate(mutants, start = 1):
    print(index2, value2)

# Create a list of tuples: mutant_data
mutant_data = list(zip(mutants, aliases, powers))
# Print the list of tuples
print(mutant_data)
# Create a zip object using the three lists: mutant_zip
mutant_zip = zip(mutants, aliases, powers)
# Print the zip object
print(mutant_zip)
# Unpack the zip object and print the tuple values
for value1, value2, value3 in zip(mutants, aliases, powers):
    print(value1, value2, value3)
    
# Create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)
# Print the tuples in z1 by unpacking with *
print(*z1)
# Re-create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)
# 'Unzip' the tuples in z1 by unpacking with * and zip(): result1, result2
result1, result2 = zip(*z1)
# Check if unpacked tuples are equivalent to original tuples
print(result1 == mutants)
print(result2 == powers)

# Initialize an empty dictionary: counts_dict
counts_dict = {}
# Iterate over the file chunk by chunk
for chunk in pd.read_csv('tweets.csv', chunksize= 10):
# Iterate over the column in DataFrame
   for entry in chunk['lang']:
        if entry in counts_dict.keys():
            counts_dict[entry] += 1
        else:
            counts_dict[entry] = 1
# Print the populated dictionary
print(counts_dict)

