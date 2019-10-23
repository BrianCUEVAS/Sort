# Sort

"""
Created on Wed Oct 23 11:07:42 2019
@author: briancuevas
This code uses an insertion sort to sort a list of random numbers
"""

def insertion_sort(nums):
    # Start on the second element as we assume the first element is sorted
    for i in range(1, len(nums)):
        item_to_insert = nums[i]
        # And keep a reference of the index of the previous element
        j = i - 1
        # Move all items of the sorted segment forward if they are larger than
        # the item to insert
        while j >= 0 and nums[j] > item_to_insert:
            nums[j + 1] = nums[j]
            j -= 1
        # Insert the item
        nums[j + 1] = item_to_insert


# Verify it works
Rnums = [12, 200, 45, 1, 57, 23]
insertion_sort(Rnums)
print(Rnums)
#this will just print out the new sorted list
