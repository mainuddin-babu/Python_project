# Enzyme Site Finder in DNA Sequence
def find_enzyme_sites(dna_sequence, enzyme_site):
"""
This function finds the positions of an enzyme's recognition site in a
DNA sequence.
Parameters:
dna_sequence (str): The DNA sequence to search.
enzyme_site (str): The recognition site of the enzyme.
Returns:
list: A list of positions where the enzyme site is found in the DNA
sequence.
"""
# Convert both inputs to uppercase to ensure case-insensitive matching
dna_sequence = dna_sequence.upper()
enzyme_site = enzyme_site.upper()
# Initialize an empty list to store the positions
positions = []
# Use a loop to find each occurrence of the enzyme site in the DNA
sequence
index = dna_sequence.find(enzyme_site)
while index != -1:
positions.append(index)
index = dna_sequence.find(enzyme_site, index + 1)
return positions
# Example usage
dna_sequence = input("Enter DNA sequence: ")
enzyme_site = input("Enter enzyme recognition site: ")
# Get the positions where the enzyme cuts
cut_positions = find_enzyme_sites(dna_sequence, enzyme_site)
# Display the results
if cut_positions:
print(f"The enzyme site '{enzyme_site}' was found at positions:
{cut_positions}")
else:
print(f"The enzyme site '{enzyme_site}' was not found in the DNA
sequence.")
