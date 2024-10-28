0x04. UTF-8 Validation
Create a function that checks whether a given dataset conforms to valid UTF-8 encoding.

Function Prototype:

python

def validUTF8(data):
Return Value:

Return True if the data is a valid UTF-8 encoding; otherwise, return False.
Description:
In UTF-8, a character can occupy between 1 to 4 bytes.
The dataset may contain multiple characters.
The input will be provided as a list of integers, where each integer represents a byte of data. Thus, you only need to process the 8 least significant bits of each integer.
